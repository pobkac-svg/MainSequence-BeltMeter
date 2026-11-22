# MainSequence-BeltMeter

Measure actual belt throughput per minute.

## Requirements

Main Sequence, single-player only. Requires [MSCore 0.8.13](https://github.com/xxalex3xx97/MSCore/releases/tag/v0.8.13), a compatible UE4SS installation and [MainSequence-Framework 0.3.6](https://github.com/pobkac-svg/MainSequence-Framework). Tested with UE4SS 4.0.0 and the user's current installed game update; other builds and multiplayer are not verified.

## Installation and updates

Install Framework first, then add `pobkac-svg/MainSequence-BeltMeter` in MSCore Manager. Save and fully restart after installation or updates. Do not enable the old standalone copy alongside this addon. The release ZIP and checksummed manifest use the MSCore Manager format.

## Use

Look at a belt to start measuring actual items/min. The readout warms up over a 60-second rolling window; it measures arrivals, not theoretical capacity. Up to eight recently viewed belts retain their history for 90 seconds away. The mod no longer pre-samples every belt in the factory.

## Removal and troubleshooting

Close the game before removing this addon through Manager. Removing an addon stops its features; it does not undo completed construction, recipes or grants. Keep native saves, Designs and underground companion files. Logs: `ue4ss/UE4SS.log` and `Mods/MSCore/selfcheck.log`.

## Compatibility and verification

Version 0.3.3: the user confirmed the clean combined build on 22 November 2026. Fifteen relevant automated suites passed. Tested with UE4SS 4.0.0; other loader versions remain unverified. No game assets, saves or private crash data are included. Severe large-save FPS drops remain a separate investigation.

## Credits and licence

Our code is MIT-licensed; see LICENSE. Developed with OpenAI Codex. MSCore by xxalex3xx97 and UE4SS are external dependencies under their own terms. This licence excludes game assets and third-party components. Unofficial; not affiliated with the game developer. This repository holds release documentation; packaged runtime downloads are attached to releases.

## Manager dependency metadata correction

Release 0.3.1 fixes matching `requires` fields in the download manifest and installed `mscore.mod`. Gameplay is unchanged. Requires the corrected Framework 0.3.5.

## Performance update

Release 0.3.2: Remove full-factory belt discovery. Track at most eight recently viewed belts, expire idle history, filter unrelated item events before resolving the world, and avoid resetting unchanged UI text. Tested by the user with only MSCore, Framework and Belt Meter enabled, with no observed slowdowns. The originally affected friend PC has not retested.

## 0.3.3 update

- Count arrivals on Mk. 1, Mk. 2, Mk. 3 and large belts; the old hook covered only the Mk. 1 override.
- Retain the bounded eight-belt, 60-second rolling sample and remove temporary diagnostic logging.
- Require Framework 0.3.6; update Walk Through Logistics to 0.3.2 as well if installed.

Save, fully close the game and update Framework first, then the installed feature addons. Fully restart after updating.
