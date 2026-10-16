# Sight Reading Trainer Soundfonts

This repository is the managed soundfont asset source for **Sight Reading Trainer**, a music-reading application by MAPL.

## Source library

The repository retains the complete **FluidR3_GM** pre-rendered soundfont collection inherited from Benjamin Gleitzman's `midi-js-soundfonts` project. The original `FluidR3_GM/` directory is intentionally kept intact for source traceability and future expansion.

Upstream project:
https://github.com/gleitz/midi-js-soundfonts

FluidR3_GM is identified by the upstream project as being released under the **Creative Commons Attribution 3.0 (CC BY 3.0)** license.

License:
https://creativecommons.org/licenses/by/3.0/

See `LICENSE-NOTICE.md` and the files under `LICENSES/` for attribution and licensing information.

## Sight Reading Trainer catalog

Sight Reading Trainer initially exposes a curated catalog of 48 FluidR3_GM instruments. Eight are intended to ship with the application and the remaining forty are intended to be downloadable. All are free during Round 13; the catalog format is designed so future entitlement rules can be added without changing stable instrument IDs.

The repository may contain additional FluidR3_GM instruments that are not currently exposed in the app. They are retained intentionally for future use.

## Asset layout

- `FluidR3_GM/` - original retained pre-rendered FluidR3_GM assets.
- `distribution/` - generated app-facing per-note audio assets. This directory will allow Sight Reading Trainer to download only the pitches it currently requires while retaining the complete source library.
- `manifest.json` - app-facing catalog and version metadata. Added after the per-note distribution files are generated and verified.
- `LICENSES/` - retained license notices.

The original FluidR3_GM files should not be destructively reorganized merely to match the mobile application's current pitch range.

## Current application strategy

The source repository retains all available notes for retained instruments. The mobile app downloads/caches only the note samples needed by its current supported range. If the app's pitch range expands later, it can download the additional samples without replacing the source library.

## Attribution

The pre-rendered soundfont packaging originates from Benjamin Gleitzman's `midi-js-soundfonts` project. FluidR3_GM attribution and licensing remain applicable to the soundfont/audio assets. Sight Reading Trainer/MAPL does not claim authorship of those third-party soundfont samples.
