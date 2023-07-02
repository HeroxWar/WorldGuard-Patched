<center>

# WorldGuard "PATCHED"

![WorldGuard Logo](https://github.com/EngineHub/WorldGuard/blob/master/worldguard-logo.png?raw=true)

This is a patched version of WorldGuard that has many changes from the original version.
</center>

[![Current WorldGuard version](https://badgen.net/badge/Current%20WorldGuard/v7.0.9-SNAPSHOT/blue?icon=github)](https://github.com/EngineHub/WorldGuard/tree/version/7.0.x) [![Official WorldGuard version](https://badgen.net/github/tag/EngineHub/WorldGuard?label=Official%20WorldGuard%20Version&icon=github&color=blue)](https://github.com/EngineHub/WorldGuard/tags)

### Changes

- [x] Disabled General commands: [/god, /ungod, /heal, /slay, /locate, /stack]

--- 

## How to create a patch from last commit

run the following command in the folder work/WorldGuard/

```shell
git format-patch -1 -o ../../patches/
```

## How to Apply Patches

run the following command in the root directory of the project (Powershell)

```shell
git apply --directory work/WorldGuard/ --ignore-whitespace (dir patches/*.patch)
```

## How to Remove Patches

run the following command in the root directory of the project

```shell
git restore . --recurse-submodules
```

## How to check DIFF

run the following command in the root directory of the project

```shell
git diff --submodule=diff work/WorldGuard/
```
