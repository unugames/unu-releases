# Security policy

## Reporting a vulnerability

This repository is a binary-only publication target with no application
source code, but it is the right place to report a security issue found in
a **published unu Windows installer or release asset** -- including a
suspicious asset, a checksum mismatch you cannot explain, or a concern about
how a release was signed or published.

Please report privately rather than opening a public issue:

- Preferred: use this repository's
  [private vulnerability reporting](https://github.com/unugames/unu-releases/security/advisories/new)
  (GitHub Security Advisories).
- If that is unavailable, reach out through the contact links on
  [unugames.com](https://unugames.com).

Do not include exploit code or secrets in a public issue, discussion, or
pull request on this repository.

## What this repository can and cannot fix directly

This repository never contains application source code or CI configuration
-- it only holds published release assets and community documentation.
Ordinary (non-security) bugs and feature requests are welcome as
[public issues](https://github.com/unugames/unu-releases/issues/new/choose).
Anything with a security impact, whether in the application itself or in
the integrity, authenticity, or publication of a release asset, should be
reported privately as described above.

## Verifying what you downloaded

Before reporting a checksum concern, re-verify against the exact
`SHA256SUMS.txt` published in the same release as the installer you
downloaded -- see the main [README](./README.md#verify-a-download) for the
verification command. Include the release version, the exact filename, and
the hash you computed in your report.

## Supported versions

Only the latest published release receives security fixes. There is no
long-term-support branch.
