# org.kde.kStyle.Darkly
Darkly style for the qt apps in flatpak

## Build Instructions
runtime 6.9
```
flatpak-builder --install-deps-from=flathub --repo=local --force-clean .build-dir org.kde.KStyle.Darkly6.9.json
flatpak build-bundle local/ org.kde.kStyle.Darkly.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.9
```
runtime 6.8
```
flatpak-builder --install-deps-from=flathub --repo=local --force-clean .build-dir org.kde.KStyle.Darkly6.8.json
flatpak build-bundle local/ org.kde.kStyle.Darkly.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.8
```
runtime 5.15-24.08
```
flatpak-builder --install-deps-from=flathub --repo=local --force-clean .build-dir org.kde.KStyle.Darkly5.15-24.08.json
flatpak build-bundle local/ org.kde.kStyle.Darkly.flatpak runtime/org.kde.KStyle.Darkly/x86_64/5.15-24.08
```
