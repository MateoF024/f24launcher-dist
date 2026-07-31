# F24Launcher
<img width="512" height="512" alt="icon" src="https://github.com/user-attachments/assets/a2654cbc-6e02-4792-9f67-5b6189262a27" />

A small, private launcher for **Minecraft: Java Edition**, built by one person and shared with
friends.

This repository hosts the **released installers and the modpacks we share**. The launcher's source
code is kept in a private repository — this is a personal project, not a product.

<img width="1920" height="1011" alt="{2898FBFC-A43E-4180-A45C-8771654A322C}" src="https://github.com/user-attachments/assets/fa3e17cf-338b-4125-bd0d-915982a56719" />

## What it does

- **Instances** — create and manage separate Minecraft installations, each with its own mod loader
  (Fabric, Quilt, Forge, NeoForge or vanilla), memory settings and world saves.
- **Content** — browse, install and update mods, resource packs, shader packs and datapacks from
  **Modrinth**, with per-instance version tracking and update detection.
- **Modpacks** — install shared modpacks, and export any instance to a Modrinth-compatible
  `.mrpack` or to the launcher's own `.f24pack`. Both formats reference files by download URL and
  hash rather than bundling them, so importing re-downloads each file from its original source.
- **Dedicated servers** — create, run and back up Minecraft servers, with a live console.
- **Accounts** — Microsoft authentication for online play.

## Design notes

- **Self-contained install.** Everything the launcher needs lives in the folder you choose at
  install time — the bundled Java runtime, the instances and the configuration. Nothing is written
  to `%APPDATA%` or elsewhere.
- **No telemetry.** The launcher makes no analytics or tracking requests. Network traffic is limited
  to the official Mojang APIs, Modrinth, and the update channel of this repository.
- **Non-commercial.** Free, with no advertising, subscriptions or donations. It is not published to
  any app store or public download site.

## Attribution and mod distribution

Mod metadata comes from the [Modrinth API](https://docs.modrinth.com/). Mods are always shown with
their name, author and a link to their project page, which opens in the system browser.

**The launcher never re-hosts or mirrors mod files.** Each installation downloads them from their
original source, and when an author has not permitted third-party distribution, the launcher says so
and links to the project page instead of obtaining the file some other way.

The same applies to the modpacks published here. They are ZIP archives that reference every mod by
download URL and SHA-1/SHA-512 hash in `modrinth.index.json`; **no mod `.jar` is contained in
them**. The only files travelling inside a pack are our own configuration, schematics and resource
packs.

## Downloads

See the [Releases](https://github.com/MateoF024/f24launcher-dist/releases) page.

> The installer is **not code-signed**, so Windows SmartScreen will show an "Unknown publisher"
> warning. A code-signing certificate is not economically viable for a non-commercial project of
> this size.
