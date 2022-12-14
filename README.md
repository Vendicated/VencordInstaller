# Vencord Installer

Vencord Installer allows you to install [Vencord, a Discord Desktop client mod](https://github.com/Vendicated/Vencord)

![image](https://user-images.githubusercontent.com/45497981/211718824-83d098d5-f7bf-4a7f-86a9-ef1b34f0442c.png)

## Usage

### Windows

Download the latest VencordInstaller.exe from [GitHub Releases](https://github.com/Vendicated/VencordInstaller/releases/latest) and run it

### Linux

```sh
sh -c "$(curl -sS https://raw.githubusercontent.com/Vendicated/VencordInstaller/main/install.sh)"
```

### Mac

Download the latest Mac build from [GitHub Releases](https://github.com/Vendicated/VencordInstaller/releases/latest), unzip it, and run `VencordInstaller.app` 

If you get a `VencordInstaller can't be opened` message, right-click `VencordInstaller.app` and click open.

This error shows because the app isn't signed since I'm not willing to pay 100 bucks a year for an Apple Developer license.

### Building from source

You need the go compiler and gcc (MinGW on Windows).

On Linux, you also need some dependencies:

```sh
apt install -y pkg-config libsdl2-dev libglx-dev libgl1-mesa-dev

# X11
apt install -y xorg-dev

# Wayland
apt install -y libwayland-dev libxkbcommon-dev wayland-protocols extra-cmake-modules
```

Then just run

```sh
# Windows / MacOs / Linux X11
go build

# Linux Wayland
go build --tags wayland
```

You might want to pass some flags to this command to get a better build.
See [the GitHub workflow](https://github.com/Vendicated/VencordInstaller/blob/main/.github/workflows/release.yml) for what flags I pass or if you want more precise instructions
