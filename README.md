# Spek Flatpak

📦 Flatpak Package of Spek for Linux

Spek is an acoustic spectrum analyser written in C and C++. It uses FFmpeg
libraries for audio decoding and wxWidgets for the GUI.

Spek is available on *BSD, GNU/Linux, Windows and Mac OS X.

Find out more about Spek on its website: http://spek.cc/

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/cc.spek.Spek.flatpakref
```

You can also install it from the bundle in Releases on GitHub, but you won't get updates that way.

## Building

### Install SDK, Platform and ffmpeg Extension

```bash
flatpak install flathub org.freedesktop.Sdk//21.08
flatpak install flathub org.freedesktop.Platform//21.08
flatpak install flathub org.freedesktop.Platform.ffmpeg-full//21.08
```

### Build and install for user

```bash
flatpak-builder --user --install --force-clean build-dir cc.spek.Spek.yml
```

### Build to repo

```bash
flatpak-builder --repo=repo --force-clean build-dir cc.spek.Spek.yml
```

### Make single-file bundle from repo

```bash
flatpak build-bundle repo spek.flatpak cc.spek.Spek stable --runtime-repo="https://flathub.org/repo/flathub.flatpakrepo"
```

## Update submodule (shared-modules)

```bash
git submodule update --remote --merge
```
