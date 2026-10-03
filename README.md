<p align="center">
  <a href="https://www.unugames.com"><img src="https://www.unugames.com/assets/img/unu-logo.png" alt="UNU" width="120"></a>
</p>

<h1 align="center">UNU</h1>

<p align="center"><strong>A console experience for your PC games.</strong></p>

<p align="center">
  <a href="https://github.com/unugames/unu-releases/releases/latest/download/unu-windows-x64-setup.exe">Download for Windows</a> ·
  <a href="https://www.unugames.com">Website</a> ·
  <a href="https://www.unugames.com/features.html">Features</a> ·
  <a href="https://discord.gg/y2uChgJ9Qx">Discord</a> ·
  <a href="https://github.com/orgs/unugames/projects/1">Roadmap</a>
</p>

<p align="center">
  <a href="https://www.unugames.com"><img src="https://www.unugames.com/assets/img/app/showcase-unu-library.png" alt="The official UNU theme showing games from multiple providers in one library"></a>
</p>

UNU is a PC game launcher designed for a TV and a controller. It brings your
games from different stores together in one interface made for the big
screen. UNU is in beta on Windows; a Linux version is planned.

This repository is where UNU's [releases](https://github.com/unugames/unu-releases/releases)
are published and where you can report bugs, suggest features, and follow
the roadmap.

## What UNU does

- **One library, many stores.** Steam, Epic Games Store, Microsoft Store,
  Xbox Game Pass, Ubisoft Connect, and Ubisoft+ games side by side. Own a
  game on two stores? It shows up once.
- **Controller first.** Browse, open details, change settings, and launch
  games without putting the controller down.
- **The best info from every source.** Cover art from SteamGridDB and
  details from IGDB are combined field by field, and you can pin the ones
  you prefer.
- **Themes and plugins.** Change how UNU looks and add stores, metadata
  sources, and sound packs from the built-in catalog. New plugins start with
  no access until you approve what they need.
- **Your phone as a companion.** Scan a QR code to type API keys and
  passwords on your phone, or use it as a trackpad and keyboard for the PC.
- **Small and fast.** The whole app is around 22 MB, and scrolling stays
  smooth even with thousands of games.

<table>
  <tr>
    <td width="50%"><a href="https://www.unugames.com/features.html"><img src="https://www.unugames.com/assets/img/app/cyberpunk-detail.png" alt="UNU showing Cyberpunk 2077 cover art, description, metadata, and available actions"></a></td>
    <td width="50%"><a href="https://www.unugames.com/features.html"><img src="https://www.unugames.com/assets/img/app/plugin-catalog.png" alt="UNU's plugin catalog showing installed and available providers"></a></td>
  </tr>
  <tr>
    <td align="center">Game details, merged from several sources</td>
    <td align="center">Install themes and plugins from inside UNU</td>
  </tr>
</table>

See [all features](https://www.unugames.com/features.html) and the
[plugin catalog](https://www.unugames.com/plugins.html) on the website.

## Download

The latest Windows installer is always available at a stable URL:

```text
https://github.com/unugames/unu-releases/releases/latest/download/unu-windows-x64-setup.exe
```

Each release also publishes an immutable, version-named installer (for
example `unu-0.3.0-windows-x64-setup.exe`), a `SHA256SUMS.txt` digest file,
and a machine-readable `release.json` manifest, so you can always pin to or
verify a specific version.

## Verify a download

Every release publishes `SHA256SUMS.txt` alongside the installer. On
Windows PowerShell:

```powershell
Get-FileHash .\unu-0.3.0-windows-x64-setup.exe -Algorithm SHA256
```

Compare the output against the matching line in that release's
`SHA256SUMS.txt`. The published `release.json` also records the exact
private source commit the release was built from, its architecture, and its
signing state.

## Signing status

Until a code-signing certificate is configured, releases are published
**unsigned**; this is stated explicitly in each release's notes. Windows
SmartScreen may warn on first run of an unsigned installer. A SHA-256 match
confirms the download was not corrupted or tampered with in transit --
it does not by itself establish who published the file. Once signing is
configured, this section and each release's notes will say so, and an
unsigned installer will no longer be published here.

## Install, uninstall, and updates

Run the downloaded installer and follow the prompts. To uninstall, use
Windows Settings > Apps, or run the uninstaller from the install directory.
Automatic in-app updates are not implemented yet; check this page's
[latest release](https://github.com/unugames/unu-releases/releases/latest)
for new versions.

## Feedback and roadmap

This repository is the public home for UNU's community feedback:

- **Found a bug?** [Open a bug report](https://github.com/unugames/unu-releases/issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](https://github.com/unugames/unu-releases/issues/new?template=feature_request.yml).
- **Curious what's coming?** See the [Unu Roadmap](https://github.com/orgs/unugames/projects/1).

UNU is built in spare time alongside a full-time job. The roadmap shows
priority and direction (*Now*, *Next*, *Later*), not delivery dates. Items
move from *Inbox* to *Considering* to *Planned*, *In Progress*, and
*Shipped*; some land in *Not Now*, which means "not at the moment", not
"never".

## Getting help

- Installation and general help: [unugames.com](https://unugames.com)
- Community chat: the [UNU Discord](https://discord.gg/y2uChgJ9Qx)
- Security issues: see [SECURITY.md](./SECURITY.md) and please report them
  privately, not as a public issue

## What is not here

This repository does not accept pull requests. It never contains source
code, build configuration, or private CI history; those live in the private
source repository referenced by each release's `release.json`.
