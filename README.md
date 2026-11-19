# Astra Emulator — Stage 1

This branch contains the Stage 1 patch package and an import workflow for bringing the complete upstream Lemon Project source into this repository.

## Import all source files

Open **Actions → Import full Lemon source into Astra → Run workflow** on branch `astra-stage1`.

The workflow downloads the public upstream source archive, copies its repository tree, preserves this workflow, applies `ASTRA_STAGE1_MALI.patch`, and commits the complete source tree to this branch.

## Stage 1 changes

- Vulkan presentation-pool policy for ARM Mali when frame generation is disabled.
- `src/video_core/vulkan_common/vulkan_device.cpp` is intentionally unchanged by the patch.
- `assets/astra-logo.svg` — Astra identity mark.
- `Astra-Emulator-Stage1-Changelog.md` — notes and validation status.

## Build

Review the imported upstream build instructions and run the Android build. No APK build has been verified by this repository update.
