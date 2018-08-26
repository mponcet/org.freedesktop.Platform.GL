# org.freedesktop.Platform.GL.default

mesa-git and llvm-git as a flatpak extension.

## Build & install instructions
```
flatpak-builder --arch=x86_64 --force-clean --repo=repo build/ org.freedesktop.Platform.GL.default.json
flatpak remote-add --no-gpg-verify mesa-llvm-git repo
flatpak install mesa-llvm-git org.freedesktop.Platform.GL.default
```

## Run

### Radeon vulkan
```
flatpak run --env=VK_ICD_FILENAMES=/usr/lib/x86_64-linux-gnu/GL/default/vulkan/icd.d/radeon_icd.x86_64.json com.valvesoftware.Steam
```
### Intel vulkan
```
flatpak run --env=VK_ICD_FILENAMES=/usr/lib/x86_64-linux-gnu/GL/default/vulkan/icd.d/intel_icd.x86_64.json com.valvesoftware.Steam
```
