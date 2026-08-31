# TODO

## Support MSP advanced configuration (linked `inVMAccessControlProfiles`)

Only inline `mode` is supported today, and inline configurations cannot be customised.
The effective in-guest rules are `defaultAccess=Allow` with no privileges or identities,
so `Enforce` does not restrict *which* processes may call IMDS - verified on a deployed
VM, where an unprivileged user still gets a managed-identity token. WireServer is already
covered, because `Enforce` implicitly requires root/Administrator there.

Closing that gap means linking an `inVMAccessControlProfile` version instead of a mode.

### To add

1. `variables.tf` - `virtual_machine_properties.proxy_agent`:
   - add `in_vm_access_control_profile_reference_id = optional(string)` to both `imds`
     and `wire_server`;
   - drop the `"Audit"` default on `mode` so "set" and "defaulted" are distinguishable,
     and resolve the default in `locals.tf` instead (no behaviour change for callers);
   - make the existing mode validations null-tolerant;
   - add a validation that `mode` and `in_vm_access_control_profile_reference_id` are
     mutually exclusive per endpoint - the API rejects both.
2. ~~`locals.tf` - build the `proxyAgentSettings` body once~~ - done. The body lives in
   `local.virtual_machine_azapi_properties` and both `azapi_update_resource.*_vm_properties`
   reference it, so the new fields only need adding in one place.
3. `README.md` - document the linked option and the mutual exclusivity.
4. `examples/windows-advanced` - show `in_vm_access_control_profile_reference_id`
   (`linux-advanced` already shows inline `Enforce`).

No provider or API version change needed: `Microsoft.Compute/virtualMachines@2024-11-01`
already exceeds the `2024-03-01` minimum for profile linking, and `azapi >= 2.0` is
already required.

### Out of scope for this module

Creating the profile itself. `Microsoft.Compute/galleries/inVMAccessControlProfiles/versions`
is a gallery-level resource authored once and linked from many VMs; creating it per VM
would have N VMs fighting over one profile. Consumers create it with `azapi_resource`
and pass the ID in.

### Related

- `Taskfile.yml` wires up `terraform test`, but there are no `*.tftest.hcl` files in the
  repo, so CI cannot catch a malformed `virtual_machine_properties` body. The new mutual-exclusion
  validation is a good first test case.

Docs: https://learn.microsoft.com/en-us/azure/virtual-machines/metadata-security-protocol/advanced-configuration
