# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.3](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v1.0.2...v1.0.3) (2026-08-04)


### 🐛 Fixes

* added missing tags that caused drift on every run ([fe0dc64](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/fe0dc6490f05719ac36f96a62cbee6823f8d2ae2))
* added missing tags that caused drift on every run ([#7](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/issues/7)) ([fe0dc64](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/fe0dc6490f05719ac36f96a62cbee6823f8d2ae2))
* migrate MCAF module sources ([#6](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/issues/6)) ([7b93a9e](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/7b93a9ec247a0a32ce519af9d845e36f6cf85a5d))

## [1.0.2](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v1.0.1...v1.0.2) (2026-07-08)


### 🐛 Fixes

* add lifecycle ignore for these extensions ([#4](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/issues/4)) ([a29f147](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/a29f1472afd3626c9973f743aa446200bb984ba3))

## [1.0.1](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v1.0.0...v1.0.1) (2026-06-24)


### 🐛 Fixes

* Only set zone on disk when disk is not ZRS ([#2](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/issues/2)) ([983d95f](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/983d95fc8d061065388dfba40654e49c1d6f7719))

## [1.0.0](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.5.0...v1.0.0) (2025-07-28)

## [0.5.0](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.4.0...v0.5.0) (2025-05-27)


### 🚀 Features

* adding the guest attestation agent ([#9](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/9)) ([598486f](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/598486f4ab39c5654fb4ab69d0af201732da01e3))

## [0.4.0](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.3.1...v0.4.0) (2025-05-15)


### 🚀 Features

* Test replace data block ([#8](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/8)) ([1dd027c](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/1dd027c8c442fb40b640f0114cdba2023d72e136))

## [0.3.1](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.3.0...v0.3.1) (2025-02-28)


### 🐛 Fixes

* bug: change data block ([#7](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/7)) ([09860e1](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/09860e1b27ef7eeb36a9b9362096c3676b859c4d))

## [0.3.0](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.2.1...v0.3.0) (2025-01-31)


### 🚀 Features

* enhancement: adding the guest_configuration_extension ([#6](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/6)) ([77d08ac](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/77d08acf68a2550778bba8dc6de368db397a507d))

## [0.2.1](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.2.0...v0.2.1) (2025-01-15)


### 🚀 Features

* enhancement: do not redeploy on custom data changes ([#5](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/5)) ([be13ff3](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/be13ff34728c4e05dfaa11322dfb510170a75645))

## [0.2.0](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.1.1...v0.2.0) (2024-12-19)


### 🚀 Features

* enhancement: disk public access to false, as default ([#4](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/4)) ([aa2524f](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/aa2524f2b82883b3dde3306f775806eb69e97bcd))

## [0.1.1](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/compare/v0.1.0...v0.1.1) (2024-12-12)


### 🚀 Features

* enhancement: change two defaults ([#3](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/3)) ([68058d9](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/68058d93ed2bac326097ab139742a26eca5abf01))

## 0.1.0 (2024-12-03)


### 🚀 Features

* Firstversion ([#1](https://github.com/schubergphilis/terraform-azure-mcaf-virtualmachine/pull/1)) ([0e97a04](https://github.com/schubergphilis-ep/terraform-azure-mcaf-virtualmachine/commit/0e97a04851b2da6e994211d22e9606a2fe80a3cd))
