# IconPack

Android-style icon packs for Windows. Pick a pack, click Apply, and your app, file-type and folder icons change. Restore puts the originals back.

**Status:** early preview. Download `IconPack-Setup-0.1.0.exe` from the [Releases page](https://github.com/Anudeepg2237/iconpack-app/releases/latest) (Windows 10/11, 64-bit, no admin rights needed). The packs here are placeholders (two-letter labels), not finished designs. Store apps such as Settings and Photos keep their own icons. The installer isn't code-signed yet, so SmartScreen asks you to confirm before it runs.

## What's in this repo

The app downloads its packs from this repo's GitHub Pages site:

- `catalog.json`: the list of packs the app shows, with each zip's SHA-256.
- `catalog.json.sig`: an ed25519 signature of `catalog.json`. The app ships with the public key and ignores a catalog that doesn't match it, so nobody else can slip a pack in.
- `packs/<id>-<version>.zip`: one `.ico` per app, file type or folder, plus `pack.json`.
- `previews/`: the gallery images.

These files are generated and signed by IconPack's publish tool. Editing one by hand breaks the signature or a checksum, and the app will refuse it.

Copyright © 2026 Anudeepg2237. All rights reserved. The app's source code is not public.
