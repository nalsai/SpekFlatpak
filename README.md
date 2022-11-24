# Spek Flatpak

📦 Flatpak Package of Spek for Linux

Spek is an acoustic spectrum analyser written in C and C++. It uses FFmpeg
libraries for audio decoding and wxWidgets for the GUI.

Find out more about Spek on its website: <http://spek.cc/>

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/repo/appstream/cc.spek.Spek.flatpakref
```

You also need to install the ffmpeg-full extension:

```bash
flatpak install flathub org.freedesktop.Platform.ffmpeg-full//22.08
```

## Building

```bash
flatpak install flathub org.freedesktop.Platform.ffmpeg-full//22.08
flatpak-builder --install-deps-from=flathub --force-clean build-dir cc.spek.Spek.yml
```

## Update shared-modules

```bash
git submodule update --remote --merge
```
