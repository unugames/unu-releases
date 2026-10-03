# unu releases

This repository publishes signed release assets for **unu**, a pluggable,
couch-first PC games launcher for Windows. It is intentionally **binary
only**: it contains no application source code, only [GitHub
Releases](https://github.com/unugames/unu-releases/releases) and the
community/security documentation on this page. The application is built and
tested in a private source repository and published here only after every
release gate passes.

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

This repository is the public home for unu's community feedback:

- **Found a bug?** [Open a bug report](https://github.com/unugames/unu-releases/issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](https://github.com/unugames/unu-releases/issues/new?template=feature_request.yml).
- **Curious what's coming?** See the [Unu Roadmap](https://github.com/orgs/unugames/projects).

unu is built in spare time alongside a full-time job. The roadmap shows
priority and direction (*Now*, *Next*, *Later*), not delivery dates. Items
move from *Inbox* to *Considering* to *Planned*, *In Progress*, and
*Shipped*; some land in *Not Now*, which means "not at the moment", not
"never".

## Getting help

- Installation and general help: [unugames.com](https://unugames.com)
- Community chat: the unu Discord (linked from
  [unugames.com](https://unugames.com))
- Security issues: see [SECURITY.md](./SECURITY.md) and please report them
  privately, not as a public issue

## What is not here

This repository does not accept pull requests. It never contains source
code, build configuration, or private CI history; those live in the private
source repository referenced by each release's `release.json`.
