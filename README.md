# poe-trade-toolkit-data

Public data-only update channel for PoE Trade Toolkit domain snapshots. No executable code.

## Contract

The repository is intentionally public so installed PoE Trade Toolkit builds can fetch versioned domain data without GitHub authentication.

Published files:

- `manifest.json` — mutable channel pointer.
- `snapshots/doryani-domain-<version>.json` — immutable normalized Doryani domain snapshots.
- `.nojekyll` — keeps GitHub Pages in plain static-file mode.

The initial manifest has `current: null`. That means no remote snapshot has been published yet; clients must continue using their bundled last-known-good snapshot.

Once a snapshot is published, its file must never be overwritten. Corrections are published as a new version and the manifest is updated to point at that version.

## Safety boundary

This repository contains data only. It must never publish executable JavaScript, extension bundles, private diagnostics, user data, credentials, or runtime state.

The private application source remains in `KMelholy/poe-trade-toolkit`.
