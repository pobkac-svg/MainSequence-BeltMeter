# MainSequence-BeltMeter

Measure actual belt throughput per minute.

## Requirements

Main Sequence, single-player only. Requires [MSCore 0.8.13](https://github.com/xxalex3xx97/MSCore/releases/tag/v0.8.13), a compatible UE4SS installation and [MainSequence-Framework 0.3.5](https://github.com/pobkac-svg/MainSequence-Framework). Tested with UE4SS 4.0.0 and the user's current installed game update; other builds and multiplayer are not verified.

## Installation and updates

Install Framework first, then add `pobkac-svg/MainSequence-BeltMeter` in MSCore Manager. Save and fully restart after installation or updates. Do not enable the old standalone copy alongside this addon. The release ZIP and checksummed manifest use the MSCore Manager format.

## Use

Look at a belt to start measuring actual items/min. The readout warms up over a 60-second rolling window; it measures arrivals, not theoretical capacity. Up to eight recently viewed belts retain their history for 90 seconds away. The mod no longer pre-samples every belt in the factory.

## Removal and troubleshooting

Close the game before removing this addon through Manager. Removing an addon stops its features; it does not undo completed construction, recipes or grants. Keep native saves, Designs and underground companion files. Logs: `ue4ss/UE4SS.log` and `Mods/MSCore/selfcheck.log`.

## Compatibility and verification

Version 0.3.2: existing gameplay confirmed by the user after MSCore migration. Manager testing was confirmed by the user; Framework and Recipe Clipboard public downloads were additionally tested through Manager. No extracted game data, user saves or private development history are included here.

## Credits and licence

Our code is MIT-licensed; see LICENSE. Developed with OpenAI Codex. MSCore by xxalex3xx97 and UE4SS are external dependencies under their own terms. This licence excludes game assets and third-party components. Unofficial; not affiliated with the game developer. This repository holds release documentation; packaged runtime downloads are attached to releases.

## Manager dependency metadata correction

Release 0.3.1 fixes matching `requires` fields in the download manifest and installed `mscore.mod`. Gameplay is unchanged. Requires the corrected Framework 0.3.5.

## Performance update

Release 0.3.2: Remove full-factory belt discovery. Track at most eight recently viewed belts, expire idle history, filter unrelated item events before resolving the world, and avoid resetting unchanged UI text. Tested by the user with only MSCore, Framework and Belt Meter enabled, with no observed slowdowns. The originally affected friend PC has not retested.
