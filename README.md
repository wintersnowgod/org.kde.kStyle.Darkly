# org.kde.kStyle.Darkly
Darkly style for the qt apps in flatpak

# Instructions
1. Build flatpak bundle / download bundle from release
2. Install flatpak according to system or user also according to what runtime your flatpak is using
- for that use command
```
flatpak list --app --columns=app,runtime | grep org.kde.Platform
```
and see what runtime versions are your app using. Install corresponding Darkly flatpak using:-

- system flatpaks
```
sudo flatpak install <pkgname>
```
- user flatpaks
```
flatpak install <pkgname> --user
```

If you install flatpaks pkgs with `--user` then do the one for user flatpaks otherwise do the system flatpaks method. If unsure you can do both.

3. Override the environment variables for flatpak
- system flatpaks
```
sudo flatpak override --env=QT_QPA_PLATFORMTHEME=kde
sudo flatpak override --env=QT_STYLE_OVERRIDE=Darkly
sudo flatpak override --filesystem=~/.config/kdeglobals:ro
```
- user flatpaks
```
flatpak override --env=QT_QPA_PLATFORMTHEME=kde --user
flatpak override --env=QT_STYLE_OVERRIDE=Darkly --user
flatpak override --filesystem=~/.config/kdeglobals:ro --user
```

If you install flatpaks pkgs with `--user` then do the one for user flatpaks otherwise do the system flatpaks method. If unsure you can do both.

4. Ok thats it. It should work for your Flatpak pkgs now.

- If you want to request any other version of the runtime then you can open the issue for it!!

## Build Instructions
# System flatpak
runtime 5.15-24.08
```
flatpak-builder --install-deps-from=flathub --repo=local-5.15-24.08 --force-clean .build-dir-5.15-24.08 org.kde.KStyle.Darkly5.15-24.08.json
flatpak build-bundle local-5.15-24.08/ org.kde.kStyle.Darkly5.15-24.08.flatpak runtime/org.kde.KStyle.Darkly/x86_64/5.15-24.08
```
runtime 6.8
```
flatpak-builder --install-deps-from=flathub --repo=local-6.8 --force-clean .build-dir-6.8 org.kde.KStyle.Darkly6.8.json
flatpak build-bundle local-6.8/ org.kde.kStyle.Darkly6.8.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.8
```
runtime 6.9
```
flatpak-builder --install-deps-from=flathub --repo=local-6.9 --force-clean .build-dir-6.9 org.kde.KStyle.Darkly6.9.json
flatpak build-bundle local-6.9/ org.kde.kStyle.Darkly6.9.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.9
```
# User flatpak
runtime 5.15-24.08
```
flatpak-builder --install-deps-from=flathub --repo=local-5.15-24.08 --force-clean .build-dir-5.15-24.08 org.kde.KStyle.Darkly5.15-24.08.json --user
flatpak build-bundle local-5.15-24.08/ org.kde.kStyle.Darkly5.15-24.08.flatpak runtime/org.kde.KStyle.Darkly/x86_64/5.15-24.08
```
runtime 6.8
```
flatpak-builder --install-deps-from=flathub --repo=local-6.8 --force-clean .build-dir-6.8 org.kde.KStyle.Darkly6.8.json --user
flatpak build-bundle local-6.8/ org.kde.kStyle.Darkly6.8.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.8
```
runtime 6.9
```
flatpak-builder --install-deps-from=flathub --repo=local-6.9 --force-clean .build-dir-6.9 org.kde.KStyle.Darkly6.9.json --user
flatpak build-bundle local-6.9/ org.kde.kStyle.Darkly6.9.flatpak runtime/org.kde.KStyle.Darkly/x86_64/6.9
```
