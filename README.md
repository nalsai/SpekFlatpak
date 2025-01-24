# Spek Flatpak

> [!CAUTION]
>
> Spek is now on Flathub (<https://flathub.org/apps/cc.spek.Spek>).  
> Therefore this repository is no longer maintained.

📦 Flatpak Package of Spek for Linux

Spek is an acoustic spectrum analyser written in C and C++. It uses FFmpeg
libraries for audio decoding and wxWidgets for the GUI.

Find out more about Spek on its website: <http://spek.cc/>

## Installing

I'm hosting this Flatpak on my own Flatpak Repo. You can install it from there like this:

```bash
flatpak install https://flatpak.nils.moe/repo/appstream/cc.spek.Spek.flatpakref
```

## Building

```bash
flatpak-builder --install-deps-from=flathub --force-clean build-dir cc.spek.Spek.yml
```

## Update shared-modules

```bash
git submodule update --remote --merge
```
