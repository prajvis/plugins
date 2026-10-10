# Prajvis plugins

A plugin catalog (marketplace) for Claude Code, Codex and Prajvis. It contains only
`.claude-plugin/marketplace.json`; every plugin lives in its own repository and is listed here by URL.

| Plugin | What it does | Source |
|---|---|---|
| `photocraft` | Photoshop-style image editing through `photocraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/photocraft) |
| `filmcraft` | Premiere-style video editing through `filmcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/filmcraft) |
| `lightcraft` | Lightroom-style photo development through `lightcraft-cli` | [prajvis/creative-plugins](https://github.com/prajvis/creative-plugins/tree/master/plugins/lightcraft) |

Photoshop, Premiere and Lightroom are trademarks of Adobe; they are mentioned only to describe what
each app does.

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
[prajvis/creative-plugins](https://github.com/prajvis/creative-plugins) directly instead.

## Adding a plugin

Add an entry to `.claude-plugin/marketplace.json`:

- `"source": "url"` when the whole repository is the plugin.
- `"source": "git-subdir"` with `path` when the plugin is a folder inside another repository.
- `ref` follows a branch or tag; add `sha` to pin an exact commit.

The entry `name` must match the `name` in the plugin's own manifest.

## License

Apache License 2.0. See [LICENSE](LICENSE), [NOTICE](NOTICE) and [TRADEMARKS.md](TRADEMARKS.md).
Each listed plugin has its own license in its own repository.
