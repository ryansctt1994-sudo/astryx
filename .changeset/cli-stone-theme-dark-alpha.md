---
'@astryxdesign/cli': patch
---

[fix] Regenerate the bundled Stone CLI theme so dark-mode accent-muted, overlay, border and shadow tokens keep their alpha channel

The committed `stoneTheme.ts` template had drifted from `pnpm bundle:cli-themes` output: dark-mode values such as `--color-border` and `--color-overlay` were fully opaque (`#f3f3f5`, `#28282a`) instead of the intended 10% / 80% alpha, so scaffolded apps got solid near-white borders and opaque overlays in dark mode.
@ryansctt1994-sudo
