# OrbusNoCombatSprint

Disables combat sprint.


## What it changes

In combat the client only lets the player move at full speed while a controller is gripping, and that drains stamina. Without a grip, combat movement is scaled down to 25%. This plugin makes the client treat grip as not held for that check, so:

* Holding grip while moving in combat gives no speed boost.
* Holding grip no longer uses stamina.
* Movement in combat stays at the normal non-sprint rate.

Nothing else that uses grip should be touched.

## Checking that it loaded

The BepInEx log should say `Combat sprint disabled (patched 2 grip checks).` If it warns about a different number something is very wrong.


## Why there is only a dll

I want to be able to reliably share this but the source code could be miss used if modified 