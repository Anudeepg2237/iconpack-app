# IconPack packs

Icon packs for IconPack, a Windows app that swaps your app, file-type and folder icons the way an Android icon pack does. The app downloads everything in this repo from its GitHub Pages site.

**Status:** placeholder packs only (Mono, Outline, Paper). Their icons are two-letter labels, not finished designs.

## What's here

- `catalog.json`: the list of packs the app shows, with each zip's SHA-256.
- `catalog.json.sig`: an ed25519 signature of `catalog.json`. The app ships with the public key and ignores a catalog that doesn't match it, so nobody else can slip a pack in.
- `packs/<id>-<version>.zip`: one `.ico` per app, file type or folder, plus `pack.json`.
- `previews/`: the gallery images.

These files are generated and signed by IconPack's publish tool. Editing one by hand breaks the signature or a checksum, and the app will refuse it.
