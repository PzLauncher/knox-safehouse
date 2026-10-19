<p align="center"><img src="images/icon.png" width="96" alt=""></p>

<h1 align="center">Knox Safehouse</h1>

<p align="center"><b>Your Project Zomboid server for friends, on the air in minutes.</b><br>
A free Windows app that installs and runs a Project Zomboid dedicated server: Workshop mods in the right order, firewall and an invite for your friends — no command lines.</p>

<p align="center">
  <a href="https://safehouse-works.pages.dev"><b>Website</b></a> ·
  <a href="https://github.com/PzLauncher/knox-safehouse/releases/latest"><b>Download</b></a> ·
  <a href="#-português">Português</a>
</p>

> Unofficial fan project, not affiliated with or endorsed by The Indie Stone. Project Zomboid belongs to its owners. Non-commercial.

![Knox Safehouse — Home](images/home.png)

## What it does
- **The server in one click** — installs and updates the official dedicated server with SteamCMD (Valve's signature checked), start/stop/restart, a console with filters and command history, a daily restart that warns the players and copies the world.
- **Mods in the right order** — paste Workshop links or a whole collection: Workshop IDs ↔ Mod IDs, dependencies added automatically, drag to reorder, warnings when something is out of place, alerts for outdated or removed mods.
- **Friends inside** — Windows Firewall rule (UDP, server ports only, Private networks), router steps, an invite ready for Discord, and modpack codes so friends can check they have the same mods.
- **Go back when it breaks** — every change to the mod list is kept; restore the last list that worked.
- **Private by default** — passwords in Windows Credential Manager, `UPnP=false`, RCON off, no telemetry.
- **Leaves no trace** — per-user install (no administrator) or portable mode; the uninstaller removes exactly what the app created.
- Portuguese (Portugal), Brazilian Portuguese and English · dark and light themes · keyboard and screen-reader friendly.

| Server | Mods | Profiles |
|---|---|---|
| ![Server page](images/server.png) | ![Mods page](images/mods.png) | ![Profiles page](images/profiles.png) |

## Download
Get the latest **`KnoxSafehouse-<version>-win-x64.zip`** from [Releases](https://github.com/PzLauncher/knox-safehouse/releases). It contains `KnoxSafehouse.exe` (self-contained, no .NET install needed), its SHA-256, `LEIA-ME.txt` and `SECURITY.md`.

- **Requirements:** Windows 10 or 11, 64-bit. The in-app Workshop uses Microsoft Edge WebView2 (already on almost every PC; the app links to Microsoft's page if it is missing).
- **Check the file:** `Get-FileHash .\KnoxSafehouse.exe -Algorithm SHA256` must match the hash in the release notes and in [SECURITY.md](SECURITY.md).
- **SmartScreen:** builds are not code-signed yet, so Windows may warn — *More info → Run anyway*.

## About
This repository holds the **public releases** of Knox Safehouse. The source code is kept private for now.

Made by **Safehouse Works**:
- **PzLauncher** — creator: the idea, the decisions and the testing on real hardware.
- **Claude** — AI collaborator (Anthropic's assistant): helped write and review the code and design the app and the website, with the creator making the final calls. Anthropic is not affiliated with or endorsing this project.

Thanks to The Indie Stone for creating Project Zomboid (https://projectzomboid.com/), which made this possible. This is an unofficial fan production for non-commercial purposes made under the Indie Stone Terms.

Licence: all rights reserved — free to download and use, no warranty.

---

## 🇵🇹 Português

**O teu servidor de Project Zomboid para os amigos, no ar em minutos.** App gratuita para Windows 10/11 que instala e gere um servidor dedicado: mods do Workshop pela ordem certa, firewall e convite para os amigos, sem linhas de comando.

> Projeto de fãs, não oficial, sem ligação à The Indie Stone. Project Zomboid pertence aos respetivos donos. Não comercial.

- **Site:** https://safehouse-works.pages.dev
- **Descarregar:** em [Releases](https://github.com/PzLauncher/knox-safehouse/releases), o ficheiro `KnoxSafehouse-<versão>-win-x64.zip`. Confirma o SHA-256 (está nas notas da versão e no [SECURITY.md](SECURITY.md)) e segue o `LEIA-ME.txt`.
- **Aviso azul do Windows (SmartScreen):** a app ainda não tem assinatura digital — *Mais informações › Executar mesmo assim*.

Feito pela **Safehouse Works**: **PzLauncher** (criador) com a ajuda do **Claude**, assistente de IA da Anthropic (a Anthropic não está ligada ao projeto).
