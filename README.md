# Kalvyr

**Watch your software take shape.** Kalvyr is a local-first companion for building software with AI coding agents. It maps your project as an architecture of understandable components, shows where agents report they are working, and keeps a history of how the architecture changes. It runs on your computer and does not upload your code.

This repository hosts Kalvyr's downloads. Get the latest version from [Releases](https://github.com/kalvyrapp/kalvyr/releases).

## Linux (x86-64)

| Package | Best for |
| --- | --- |
| `Kalvyr-<version>-Linux-x64.deb` | Debian and Ubuntu (recommended) |
| `Kalvyr-<version>-Linux-x64.AppImage` | Any distribution |
| `Kalvyr-<version>-Linux-x64.tar.gz` | Any distribution, no installer |

**Debian or Ubuntu:**
```bash
sudo apt install ./Kalvyr-1.0.0-Linux-x64.deb
kalvyr
```

**AppImage:** needs FUSE 2 (`libfuse2`, or `libfuse2t64` on Ubuntu 24.04 and later).
```bash
chmod +x Kalvyr-1.0.0-Linux-x64.AppImage
./Kalvyr-1.0.0-Linux-x64.AppImage
```

**Archive:**
```bash
tar -xzf Kalvyr-1.0.0-Linux-x64.tar.gz
./Kalvyr-1.0.0-Linux-x64/kalvyr
```

On systems that restrict user namespaces (the default on Ubuntu 24.04 and later), the `.deb` sets up Kalvyr's window sandbox for you. The AppImage starts with that sandbox turned off. The archive stops with a "SUID sandbox helper" error until you run this once from its folder:
```bash
sudo chown root:root chrome-sandbox && sudo chmod 4755 chrome-sandbox
```

## Check your download

Each release includes `SHA256SUMS`. In the folder with your download:
```bash
sha256sum --check --ignore-missing SHA256SUMS
```

## Other systems

Windows and macOS downloads aren't published here yet.
