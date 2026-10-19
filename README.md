# Prajvis plugins

A plugin catalog (marketplace) for Claude Code, Codex and Prajvis. It contains only
`.claude-plugin/marketplace.json`; every plugin lives in its own repository and is listed here by URL.

| Plugin | What it does | Source |
|---|---|---|
| `pcode` | Shell commands and AI coding agents inside Coder workspaces, for agents | [prajvis/pcode](https://github.com/prajvis/pcode/tree/master/pcode-plugin) |
| `photocraft` | Photoshop-style image editing through `photocraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/photocraft) |
| `filmcraft` | Premiere-style video editing through `filmcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/filmcraft) |
| `lightcraft` | Lightroom-style photo development through `lightcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/lightcraft) |
| `vectorcraft` | Illustrator-style vector art through `vectorcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/vectorcraft) |
| `pdfcraft` | Acrobat-style PDF work through `pdfcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/pdfcraft) |
| `effectcraft` | After Effects-style motion graphics through `effectcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/effectcraft) |
| `designcraft` | InDesign-style page layout through `designcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/designcraft) |
| `gridcraft` | Excel-style spreadsheets through `gridcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/gridcraft) |
| `cadcraft` | AutoCAD-style 2D drafting through `cadcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/cadcraft) |

Photoshop, Premiere, Lightroom, Illustrator, Acrobat, After Effects and InDesign are trademarks of
Adobe, Excel of Microsoft and AutoCAD of Autodesk; they are mentioned only to describe what each
app does.

## Install

**Claude Code**

```text
/plugin marketplace add prajvis/plugins
/plugin install photocraft@prajvis
```

**Codex**

```text
codex plugin marketplace add prajvis/plugins
```

**Prajvis** includes this catalog as a default marketplace.

**Cursor** can't install plugins from other repositories through a marketplace. Add
[prajvis/creative-plugins](https://github.com/prajvis/creative-plugins) or the `pcode-plugin/` folder of
[prajvis/pcode](https://github.com/prajvis/pcode) directly instead.

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json`:

- `"source": "url"` when the whole repository is the plugin.
- `"source": "git-subdir"` with `path` when the plugin is a folder inside another repository.
- `ref` follows a branch or tag; add `sha` to pin an exact commit.

The entry `name` must match the `name` in the plugin's own manifest.

## License

Apache License 2.0. See [LICENSE](LICENSE), [NOTICE](NOTICE) and [TRADEMARKS.md](TRADEMARKS.md).
Each listed plugin has its own license in its own repository.
