# Power Inside

Omarchy plugin: the stock power widget, but with the battery percentage
rendered **inside** the battery icon — iOS-style.

![battery widget on the bar](assets/bar-zoom.png)

## Install

```bash
omarchy plugin add https://github.com/jacker-nz/omarchy-power-inside --enable
```

The in-icon percentage is on by default. Right-click or middle-click the
battery icon to toggle back to the plain glyph (writes `showPercentage` on
the `jacker-nz.power-inside` bar entry in `shell.json`).

## Remove

```bash
omarchy plugin disable jacker-nz.power-inside
omarchy plugin remove jacker-nz.power-inside
```

Restores the built-in `omarchy.power` widget.

## Features

- Percentage inside the icon; digits stay legible at any charge level
- Bolt marker and shimmer animation while charging
- Urgent fill color at ≤ 20%, pulse at critical level
- Full stock power panel: level, capacity, cycles, rate, time, profile picker
- Theme-aware; the only fixed color is the charging green

## Requirements

- Omarchy Quattro (Quickshell shell)
- `upower` (bundled with Omarchy)

## Notes

- Declares `omarchy.clonedFrom: "omarchy.power"` — takes the built-in
  widget's bar slot and keeps its settings; nothing to move manually
- In-icon mode on horizontal bars; vertical bars fall back to the glyph
- Hidden on systems without a battery

## License

MIT — see [LICENSE](LICENSE)
