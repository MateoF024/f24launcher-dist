# F24Launcher

A small, private launcher for **Minecraft: Java Edition**, built by one person and shared with
friends.

This repository hosts the **released installers and the modpacks we share**. The launcher's source
code is kept in a private repository — this is a personal project, not a product.

<img width="1920" height="1033" alt="{798377A9-4B63-4D61-9D70-7BC6B4181642}" src="https://github.com/user-attachments/assets/2b99184d-e4f1-4eb9-8d24-0d2e3ad0119d" />

<img width="1920" height="1033" alt="{365EF8F1-47B7-44ED-8F34-6C96619B75DF}" src="https://github.com/user-attachments/assets/73d43884-91a1-423c-aff3-6c764325b540" />

<img width="1920" height="1035" alt="{3F8DC9BF-C947-477C-A269-66E98F165DDD}" src="https://github.com/user-attachments/assets/0721a16d-8d7d-42ba-affe-90e3f4985ab1" />

<img width="1920" height="1034" alt="{7AD7E5E3-B915-415C-9930-8886DD236C8E}" src="https://github.com/user-attachments/assets/5c67bb5b-7405-451e-a5ae-c6dbff5bc5a2" />



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
