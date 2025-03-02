# Changelog

## 1.19.0 (2022-06-16)

- Return ethers transaction response with `proposeUpgrade`. ([#554](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/554))

## 1.18.3 (2022-06-14)

- Fix dependency on hardhat-etherscan.

## 1.18.2 (2022-06-14)

- Update `verify` to be compatible with latest version of hardhat-etherscan. ([#592](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/592))

## 1.18.1 (2022-06-03)

- Fix task redefinition error with hardhat-etherscan. ([#586](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/586))

## 1.18.0 (2022-05-31)

- Support verifying a proxy on Etherscan using Hardhat. ([#579](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/579))

## 1.17.0 (2022-03-29)

- Support specifying proxy kind for `forceImport`, fix importing UUPS proxy with admin ([#550](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/550))

## 1.16.1 (2022-03-15)

- Fix lock file issue with validations cache when compiling a large number of contracts ([#537](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/537))

## 1.16.0 (2022-03-08)

- Use a lockfile when reading validations cache to avoid problems with parallel compilation in Hardhat 2.9.0. ([#530](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/530))
- Add an option `unsafeSkipStorageCheck` to skip storage layout compatibility check during upgrades. ([#495](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/495))

## 1.15.0 (2022-03-01)

- Add `forceImport` function to import an existing proxy or beacon. ([#517](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/517))
- Extract and store more detailed information about storage layout. ([#519](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/519))

## 1.14.0 (2022-01-31)

- Add options `timeout` and `pollingInterval`. ([#55](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/55))

## 1.13.0 (2022-01-12)

- Add support for beacon proxies. ([#342](https://github.com/OpenZeppelin/openzeppelin-upgrades/issues/342))

## 1.12.1 (2022-01-06)

- Fix issues when deploying to Polygon Mumbai testnet. ([#487](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/487))

## 1.12.0 (2021-10-28)

- Add support for `upgradeToAndCall` to batch a function call into the upgrade transaction. ([#443](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/443))

## 1.11.0 (2021-10-22)

- Infer whether a proxy should be UUPS or Transparent. ([#441](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/441))
- Add implementation constructor arguments to initialize immutable variables. ([#433](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/433))

## 1.10.0 (2021-08-25)

- Add `erc1967` module. ([#413](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/413))

## 1.9.0 (2021-06-29)

- Add option `unsafeAllowRenames` to configure storage layout check to allow variable renaming.

## 1.8.2 (2021-05-13)

- Simplify `deployTransaction` assignment in `deployProxy` as a fix for congested networks.

## 1.8.1 (2021-05-13)

- Simplify `deployTransaction` assignment in `upgradeProxy`.

## 1.8.0 (2021-05-12)

- Support passing contract instance to `upgradeProxy` and `prepareUpgrade`.
- Enable awaiting until a proxy upgrade is mined:

```
const v2 = await upgrades.upgradeProxy(proxy, ContractV2);
await v2.deployed();
```

## 1.7.0 (2021-04-29)

- Add support for UUPS proxies. ([#315](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/315))

## 1.6.0 (2021-01-27)

- Add support for structs and enums. ([#261](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/261))

## 1.5.0 (2021-01-15)

- Add `upgrades.admin.getInstance()` to retrieve the instance of `ProxyAdmin` that is in use. ([#274](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/274))

## 1.4.3 (2020-12-16)

- Fix an error in the `unsafeAllowCustomTypes` flag that would cause other storage layout incompatibilities to be ignored. ([#259](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/259))

Users of this flag are advised to update to this version.

## 1.4.2 (2020-12-04)

- Fix a bug that prevented some solc errors from reaching the console. ([#253](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/253))

## 1.4.1 (2020-11-30)

- Add `admin` to the TypeScript type for `hre.upgrades`.

## 1.4.0 (2020-11-24)

- Add `silenceWarnings` to emit a single warning and silence all subsequent ones. ([#228](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/228))

## 1.3.1 (2020-11-18)

- Allow ommitting `args` in `deployProxy` when it's an empty array.

## 1.3.0 (2020-11-13)

- Migrate plugin to Hardhat. ([#214](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/214))

## 1.2.1 (2020-10-21)

- Add ability to disable proxy initialization by specifying `initializer: false`. ([#204](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/204))

## 1.2.0 (2020-10-16)

- Add new flag `unsafeAllowLinkedLibraries` to allow deployment of contracts with linked libraries. ([#182](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/182))

## 1.1.1 (2020-10-08)

- Add prepareUpgrade to Buidler type extensions. ([#184](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/184))
- Fix OpenZeppelin CLI migration for projects that were initialized with ZeppelinOS. ([#193](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/193))

## 1.1.0 (2020-09-18)

- Add a script to migrate from OpenZeppelin CLI. ([#143](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/143))

## 1.0.2 (2020-09-01)

- Include `src` directory in npm packages. ([#150](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/150))

## 1.0.1 (2020-08-20)

- Store transaction hash in contract instances returned by `deployProxy`. ([#129](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/129), [#133](https://github.com/OpenZeppelin/openzeppelin-upgrades/pull/133))
