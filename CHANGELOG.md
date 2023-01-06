# Changelog

## [0.6.1](https://github.com/kurtosis-tech/datastore-army-package/compare/0.6.0...0.6.1) (2023-01-06)


### Refactors

* Update `add_service` to use `ServiceConfig` for its `config` arg ([#53](https://github.com/kurtosis-tech/datastore-army-package/issues/53)) ([bea66e0](https://github.com/kurtosis-tech/datastore-army-package/commit/bea66e0b14b78bba08433cdee5fdeb7d8d4da77f))


### Miscellaneous

* Release please adds a changelog entry for every PRs ([#54](https://github.com/kurtosis-tech/datastore-army-package/issues/54)) ([4a3ea98](https://github.com/kurtosis-tech/datastore-army-package/commit/4a3ea98634066959cdbca2e7d7ae942acf906815))

## [0.6.0](https://github.com/kurtosis-tech/datastore-army-package/compare/0.5.0...0.6.0) (2022-12-20)


### ⚠ BREAKING CHANGES

* We use the `plan` object now in datastore-army-package. Users must upgrade to Kurtosis >= 0.63 and restart the engine for this to work.

### Bug Fixes

* Make the package work with the plan object ([#51](https://github.com/kurtosis-tech/datastore-army-package/issues/51)) ([19e4246](https://github.com/kurtosis-tech/datastore-army-package/commit/19e42467d2162c2a4a26e276c039431c39d0cf82))

## 0.5.0

### Breaking changes
- Updated `protocol` to `transport protocol` in PortSpec constructor to create port definitions 

## 0.4.0

### Breaking changes
- Updated `struct` to `PortSpec` for declaring port definitions 

### Changes
- Updated `run(input_args)` to `run(args)`
- Changed `datastore-army-module` to `datastore-army-package`
- Removed `print(output)` at the end as it is now printed by the framework
- Use the `args` argument instead of flags

## 0.3.2
### Changes
- Renamed `kurtosis.mod` file to the new `kurtosis.yml` file format
- Removed 'module' key in the 'kurtosis.yml' file

## 0.3.1

### Changes 
- Renamed `kurtosis.mod` file to the new `kurtosis.yml` file format
- Remove protobuf. Package input and output types does not rely on protobuf schema anymore

## 0.3.0

### Removals
- Removed the `scripts` folder, uses should use `kurtosis run` instead

### Changes
- Replace `load()` with `import_module`
- Replaced the old `main` with `run` in main.star

### Fix
- Fix CI following the removal of `startosis` in `kurtosis startosis exec ...`
- Fix CI following the change of `run` in `kurtosis run ...`

### Breaking changes
- Switch module to be 100% implemented in Startosis.

### Features
- Add a Startosis script "replacing" the module. One thing still missing is the ability to pass parameters to the 
Startosis script (for the Go module, we can pass the number of datastore nodes).
- Uses the new syntax for parts of add_service

## 0.2.14

### Changes
- Upgrade to module-api-lib 0.23.0
- Uses core from the new `kurtosis-sdk` over `kurtosis-core-api-lib`

## 0.2.13

### Changes
- Upgrade to core 1.59.0
- Upgrade to module-api-lib 0.22.0

## 0.2.12

### Changes
- Upgrade to core 1.58.3
- Upgrade to module-api-lib 0.21.2

## 0.2.11
### Changes
- Upgrade to core 1.58.1
- Upgrade to module-api-lib 0.21.1

## 0.2.10
### Changes
- Upgrade to module-api-lib to 0.21.0
- Upgraded core to 1.58.0

## 0.2.9
### Changes
- Downgrade Kurtosis dependencies core to 1.57.0 and module-api-lib to 0.18.0 due the incompatibility with the latest Kurtosis CLI release
- Upgrade core to 1.57.6
- Upgrade module-api-lib 0.20.0

## 0.2.8
### Changes 
- Upgrade to core 1.57.3
- Upgrade to module-api-lib 0.19.0

## 0.2.7

## 0.2.6
### Features
- Added CircleCi workflow for running a scheduled pipeline every day to control successful module execution
- Added slack orb in the CircleCi config file to notify when the `check_module_execution` job fails

## 0.2.5
### Changes
- Migrate repo to use internal cli tool `kudet`, for updating release workflow
- Upgrade to module-api-lib 0.18.0
- Upgrade to core 1.57.0

## 0.2.4
### Changes
- Upgrade to module-api-lib 0.17.0
- Upgrade to core 1.55.2

## 0.2.3
### Changes
- Upgrade to module-api-lib 0.16.0 and core 1.54.1

## 0.2.2
### Changes
- Upgrade to module-api-lib 0.15.0

## 0.2.1
### Changes
- Upgrade to module-api-lib 0.14.1

## 0.2.0
### Changes
- Upgrade to module-api-lib 0.12.2 which supports the latest Kurt Core

### Breaking Changes
- The returned object now contains a mapping of `datastore_service_id` -> `datastore_port_id`, so the user can retrieve or public or private ports as they please
    - Users should swap the old `createdServiceIdPorts` property -> `createdServiceIdsToPortIds`

## 0.1.5
### Changes
- Replaced `kurtosistech/example-microservices_datastore` with the newest `kurtosistech/example-datastore-server` datastore image which implements GRPC

## 0.1.4
### Fixes
- Correct README link

## 0.1.3
### Fixes
- Fixed bug that occurred with calling execute multiple times, where the IDs wouldn't be updated

## 0.1.2
### Fixes
- Add `kurtosistech` org name to image so that CI can publish it to Dockerhub

## 0.1.1
### Features
- Adding CI

## 0.1.0
- Initial tagged commit
