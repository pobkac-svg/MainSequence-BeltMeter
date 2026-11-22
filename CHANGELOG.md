# Changelog

## 0.3.3 ? 2026-11-22

- Count arrivals on Mk. 1, Mk. 2, Mk. 3 and large belts; the old hook covered only the Mk. 1 override.
- Retain the bounded eight-belt, 60-second rolling sample and remove temporary diagnostic logging.
- Require Framework 0.3.6; update Walk Through Logistics to 0.3.2 as well if installed.

## 0.3.2

- Remove full-factory scans, bound history to eight recently viewed belts, reject unrelated events early, and avoid redundant text updates.
- User reports smooth operation in the isolated three-mod test.
- Promoted to stable; runtime files are identical to the performance-test build.

## 0.3.1

- Fix MSCore Manager rejection by matching dependency metadata in manifest.txt and mscore.mod.
- Requires corrected Framework 0.3.4.
- Packaging/metadata correction; gameplay is unchanged.

## 0.3.0

- MSCore-backed release.
- Preserves existing tested gameplay.
- Includes MIT licence and Manager metadata.
