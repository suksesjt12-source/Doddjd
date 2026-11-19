# Astra Emulator — Stage 1

Stage 1 changes prepared for the Lemon Project source:

- Vulkan presentation-pool policy for ARM Mali when frame generation is disabled.
- Astra Emulator branding/theme changes are documented in the Stage 1 changelog and included in the source archive from the conversation.
- `src/video_core/vulkan_common/vulkan_device.cpp` is intentionally unchanged.

## Apply Vulkan patch

From a Lemon Project source checkout, apply:

```sh
git apply ASTRA_STAGE1_MALI.patch
```

Then review and build/test for your target platform. No APK build has been verified.

## Files in this repository

- `ASTRA_STAGE1_MALI.patch`: focused Vulkan C++ patch.
- `Astra-Emulator-Stage1-Changelog.md`: implementation notes and validation.
- `assets/astra-logo.svg`: editable vector mark.

This repository was empty before this upload; this commit stores the patch package, not the full upstream source tree.
