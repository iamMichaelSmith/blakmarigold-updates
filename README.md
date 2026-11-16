# Blak Marigold Updates

This repository hosts the update manifest and signed installers for Blak Marigold plug-ins. The plug-ins read `updates.json` from GitHub Pages to find new versions:

https://iammichaelsmith.github.io/blakmarigold-updates/updates.json

Windows only (64-bit VST3). Installers are signed by Blak Marigold Pro LLC and attached to the GitHub Releases of this repository, tagged `<product>-<version>` (for example `pro-eq-0.15.0`).

No plug-in source code lives here.

## Manifest format

```json
{
  "format": 1,
  "products": {
    "pro-eq": {
      "name": "Blak Marigold Pro EQ",
      "version": "0.15.0",
      "url": "https://github.com/iamMichaelSmith/blakmarigold-updates/releases/download/pro-eq-0.15.0/ProEQ-Setup-0.15.0-Windows-x64.exe",
      "sha256": "SHA-256 of the installer",
      "notes": ["One line per change"],
      "min_os": "windows-10",
      "page": "https://www.blakmarigold.com/store/p/blak-marigold-pro-eq"
    }
  }
}
```

Each product has its own key under `products`. To publish a release: upload the signed installer to a release tagged `<product>-<version>`, then update that product's `version`, `url`, `sha256` and `notes` in `updates.json`.

Store: https://www.blakmarigold.com
