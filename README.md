# org.freedesktop.Platform.GL.default

## Build & install instructions
```
flatpak build-init build org.freedesktop.Platform.GL.default org.freedesktop.Platform/x86_64/1.6 org.freedesktop.Sdk/x86_64/1.6
flatpak-builder --arch=x86_64 --force-clean build/ org.freedesktop.Platform.GL.default.json
flatpak build-export repo build 1.6
flatpak remote-add --no-gpg-verify mesa-llvm repo
flatpak install mesa-llvm org.freedesktop.Platform.GL.default
```
