# Astra Emulator — Stage 1 Change Log

## Vulkan Mali
- File: `src/video_core/renderer_vulkan/vk_present_manager.cpp`
- Mali driver detection uses the existing `Device::GetDriverID()` API.
- With ARM proprietary Vulkan driver and no frame generation, cap internal presentation frames to 3 or the swapchain image count, whichever is smaller.
- With frame generation enabled, preserve the original generation/queue calculation.
- Non-Mali drivers keep the original maximum of 7.
- This is a queue-depth/memory trade-off, not a measured FPS claim. It may make the render thread wait sooner if presentation falls behind.

## Branding
The full Stage 1 source archive includes Android app-name, theme, splash, launcher/adaptive icon, banner, and UI text branding changes. The package/application ID and internal namespaces are retained. The upstream attribution is preserved.

## Protected file
`src/video_core/vulkan_common/vulkan_device.cpp` is intentionally unchanged.

## Validation
Patch and packaging checks were performed on the source archive. Android SDK/NDK were unavailable, so no APK build or device benchmark is claimed.
