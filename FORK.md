# MySkills fork notes

This repo mirrors [mattpocock/skills](https://github.com/mattpocock/skills) for Claude marketplace install as `mattpocock-skills@MySkills`.

## Version field (do not drop)

Claude detects plugin updates via `.claude-plugin/plugin.json` → `version`.

When merging upstream:

1. Keep `version` in `.claude-plugin/plugin.json` (never delete / never leave unset).
2. Keep the same `version` on the `mattpocock-skills` entry in both:
   - `.claude-plugin/marketplace.json`
   - `marketplace.json`
3. Keep `package.json` `version` in sync with the plugin version.
4. If the merge brings real skill/doc changes and `version` did not increase, bump all three places yourself (semver patch/minor as appropriate).

Without a `version`, Cowork / Claude will not show an update even after `marketplace update`.
