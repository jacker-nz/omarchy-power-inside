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

## Update

```bash
omarchy plugin update jacker-nz.power-inside
```

## Remove

```bash
omarchy plugin disable jacker-nz.power-inside
omarchy plugin remove jacker-nz.power-inside
```

Restores the built-in `omarchy.power` widget.

## Features

- Percentage inside the icon; sub-pixel optically centered digits stay legible at any charge level
- Bolt marker and shimmer animation while charging
- Red warning pill at ≤ 20% with high-contrast digits; breathing red tint at ≤ 10%
- Full stock power panel: level, capacity, cycles, rate, time, profile picker
- Theme-aware; adapts automatically to light and dark bars

## Requirements

- Omarchy Quattro (4.4.x and 4.5.0+)
- `upower` (bundled with Omarchy)

## Notes

- Declares `omarchy.clonedFrom: "omarchy.power"` — takes the built-in
widget's bar slot; nothing to move manually
- In-icon mode on horizontal bars; vertical bars fall back to the glyph
- Hidden on systems without a battery

## Support

Power Inside is free and open source. If it saves you time, you can buy me a coffee:

- Afdian （爱发电）: https://afdian.com/a/jacker-nz

## License

MIT — see [LICENSE](LICENSE)
