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

### Several plugins in one repository

Keep each plugin in its own folder and release each one with a tag that starts with a prefix of its own, like `my-plugin-1.2.0`; the part after the prefix must match `version` in the plugin's `manifest.json`. Add `"tagPrefix": "my-plugin-"` to the plugin's entry, and Flint (0.12 and later) installs that plugin's newest release, skipping drafts and pre-releases. [flint-official-plugins](https://github.com/cucsijuan/flint-official-plugins) is set up this way.

## Licenses

Flint is AGPL-3.0-or-later. Plugins declare an SPDX license in their manifest, and Flint warns when it isn't compatible with the AGPL.
