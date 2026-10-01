# VLauncher

A free, non-commercial custom launcher for **Minecraft: Java Edition**, built for the community of a private Minecraft server.

> VLauncher is not affiliated with, endorsed by, or associated with Mojang Studios or Microsoft. Minecraft is a trademark of Mojang Studios.

## What it does

- Downloads the official game files, libraries and assets directly from Mojang's servers and starts the **unmodified official game client**. It does not bundle or redistribute any Minecraft files.
- Lets you choose the game version and a mod loader: Vanilla, Fabric, Forge, NeoForge or Quilt.
- Mod, shader and resource pack browser powered by the public Modrinth API.
- Multiple game profiles, screenshots viewer, themes and interface settings.
- Optional Discord Rich Presence.
- Automatic launcher updates from GitHub Releases (SHA-256 checked).

## Accounts

**Microsoft account sign-in** (for players who own Minecraft: Java Edition):

- Uses the official Microsoft OAuth 2.0 *device code flow*: you enter a code on Microsoft's own page. The launcher never sees your password.
- Then the standard Xbox Live, XSTS and Minecraft Services chain is used to get your profile and game token.
- Only an encrypted refresh token is stored on your PC (Windows DPAPI). You can sign out at any time in Settings.
- Without a license the account cannot be used to play online.

**Local nickname mode:** the launcher can also start the game with a plain nickname, which is intended only for private servers that run with `online-mode=false`. It is a separate option and is not related to Microsoft sign-in.

## Privacy

- No ads, no paid features, no telemetry or analytics.
- Network requests go only to: Mojang / Microsoft / Xbox services, Modrinth, the mod loaders' official download servers, Discord (optional presence) and GitHub (updates).
- Settings are stored locally in `%APPDATA%`.

## Installation

1. Download `VLauncher.exe` from the [Releases](../../releases) page.
2. Run it. Java is downloaded automatically when needed.

Windows 10/11 is required.

## Building from source

```bash
pip install minecraft-launcher-lib requests pywebview pypresence yt-dlp pyinstaller
python launcher.py
python -m PyInstaller --onefile --noconsole --name VLauncher launcher.py
```

## License and legal

This project is a personal, non-commercial hobby project. Use of Minecraft is subject to the [Minecraft EULA](https://www.minecraft.net/eula) and the [Usage Guidelines](https://aka.ms/mcusageguidelines).
