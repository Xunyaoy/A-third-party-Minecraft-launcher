# A-third-party-Minecraft-launcher
A third‑party Minecraft launcher built with Electron + Vite + Vue

Important Notice
This project is a third‑party Minecraft launcher, not an official product of Mojang Studios / Microsoft. This project does not distribute the Minecraft game client. You must own a legitimate Minecraft account to use this launcher. No functionality for circumvention of official authentication is implemented.

Project Principles & Scope
This launcher will NOT internally download the Minecraft client, game libraries, assets, loader installers, or Java runtime. It only parses metadata and verifies local file integrity. If required files are missing, external download links will be provided for users to obtain files manually via browser.
Modrinth ecosystem content including mods, shaders, resource packs and data‑packs supports in‑launcher one‑click download, hash verification and automatic deployment to corresponding game directories.
For .mrpack modpack processing: extract overrides; automatically download and install Modrinth‑hosted components; original Minecraft‑related entries will only show external download links and will not be downloaded inside the launcher.
High‑risk operations such as file I/O and network requests run entirely in the Electron main process. IPC communication between main and renderer processes is implemented via preload scripts and contextBridge.
Key Features
Account system: Offline login, Microsoft DeviceCode authentication, Authlib Yggdrasil external authentication (skin libraries)
Local version parsing with version inheritance support; real‑time game log view and crash‑report export
Custom JVM arguments with pre‑configured memory presets
Modrinth API integration: search, download and hash‑verify mods, shaders and resource packs
.mrpack modpack parsing and installation
Java environment detection; redirect to external download page when Java is missing
Launcher version check (notification‑only; no automatic update download)
Not implemented: Server list, multiplayer lobby, network tunneling and all private‑server‑related features

Build & Development
Requirements
Node.js: 20 LTS
Package manager: pnpm
Git
# Install pnpm (if missing)
npm install -g pnpm

# Install dependencies
pnpm install

# Start development mode
pnpm dev

# Build for production
pnpm build
