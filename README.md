<div align=center>

# WorldGuard "PATCHED"

[![WorldGuard Logo](https://github.com/EngineHub/WorldGuard/blob/master/worldguard-logo.png?raw=true)](https://github.com/EngineHub/WorldGuard)

This is a patched version of WorldGuard that has many changes from the original version.

[![Current WorldGuard Patched](https://badgen.net/badge/Current%20WorldGuard%20Patch/v7.0.14-SNAPSHOT-98b5220/blue?icon=github)](https://github.com/EngineHub/WorldGuard/tree/98b52206a0e9c2a13cf7efc5fc2b3c81d71aa658) [![Official WorldGuard version](https://badgen.net/github/tag/EngineHub/WorldGuard?label=Official%20WorldGuard%20Version&icon=github&color=blue)](https://github.com/EngineHub/WorldGuard/tags)
</div>

### Changes

- [x] Disabled General commands: [`/god, /ungod, /heal, /slay, /locate, /stack`]

--- 

## Getting started

1. Clone the repository
2. Run `git submodule update --init --recursive` to get the submodules
3. Apply patches ([see below](#how-to-apply-patches))

#### (For developer) If you want to create a patch

1. Go inside the submodule folder `work/WorldGuard/`
2. Type `git add .`
3. Now commit your changes with `git commit -m "your message"` (push is not needed)
4. Now create a patch ([see below](#how-to-create-a-patch-from-last-commit))

#### If you want to compile

1. Follow the "[Getting started steps](#getting-started)"
2. Go inside the submodule folder `work/WorldGuard/`
3. Now you can run the compile commands ([see below](#how-to-build))

#### If you want to update the submodules to the last version

1. Be sure to save the current patches before to continue
2. In project root folder type `git submodule update --remote --force`
3. Now you can applay again the patches ([see below](#how-to-apply-patches))

---
<br/>
<br/>

## How to create a patch from last commit

run the following command in the folder `work/WorldGuard/`

```shell
git format-patch -1 -o ../../patches/ --start-number ((dir ../../patches/).Count + 1)
```

## How to apply patches

run the following command in the folder `work/WorldGuard/` directory of the project (use PowerShell)

```shell
git am (dir ../../patches/*.patch) --3way
```

## How to remove patches

run the following command in the root directory of the project

```shell
git restore . --recurse-submodules
```
<br/>
<br/>

## How to Build?

Be sure to follow the "[Getting started steps](#getting-started)" first

> ⚠ Required Java **21** (only)!

Run the following command in the folder `work/WorldGuard/`

```shell
gradlew build -S
```

You will find WorldGuard for Bukkit in the folder `build` or follow the instructions
inside `work/WorldGuard/COMPILING.md`

(The `-dist` version includes WorldGuard + necessary libraries.)
