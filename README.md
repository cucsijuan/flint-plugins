# Flint community plugins

The list of community plugins that [Flint](https://github.com/cucsijuan/flint) shows in Settings → Plugins → Browse.

## Adding your plugin

1. Publish your plugin in its own public GitHub repository, with a release whose assets include `main.js` and `manifest.json` (and `styles.css` if it has one). The release tag must match `version` in `manifest.json`.
2. Open a pull request that adds an entry to the end of `plugins.json`:

```json
{
  "id": "word-count",
  "name": "Word count",
  "author": "Your name",
  "description": "Shows word and character counts for the current note.",
  "repo": "your-name/flint-word-count"
}
```

`id` must match the `id` in your `manifest.json` and be unique in this list.

## Licenses

Flint is AGPL-3.0-or-later. Plugins declare an SPDX license in their manifest, and Flint warns when it isn't compatible with the AGPL.
