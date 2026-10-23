# OrbusNoCombatSprint

Disables combat sprint.

## Installing a patch

* Install the latest version of [BepInEx](https://github.com/BepInEx/BepInEx/releases) into your OrbusVR game directory.
* Download the `.dll` for the patch from the [Releases](https://github.com/Cnidocyte-embrace/OrbusNoCombatSprint/releases) page.
* Place the `.dll` in: `BepInEx/plugins/` directory (Note: You might need to launch the game once for this folder to generate)

## Linux / Proton

If you are running through proton, add this to the games launch options:
`WINEDLLOVERRIDES="winhttp.dll=n,b" %command%`

## What it changes

In combat the client only lets the player move at full speed while a controller is gripping, and that drains stamina. Without a grip, combat movement is scaled down to 25%. This plugin makes the client treat grip as not held for that check, so:

* Holding grip while moving in combat gives no speed boost.
* Holding grip no longer uses stamina.

Nothing else that uses grip should be touched.

## Checking that it loaded

The BepInEx log should say `Combat sprint disabled (patched 2 grip checks).` If it warns about a different number something is very wrong.


## Why there is only a dll

I want to be able to reliably share this but the source code could be miss used if modified 
