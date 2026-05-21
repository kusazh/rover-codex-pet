# Codex Rover Pet

A Codex custom pet made from the classic Rover dog animations.

This package contains the files needed to install Rover as a Codex pet:

- `pet.json` - Codex pet manifest
- `spritesheet.webp` - 9-row Codex pet animation atlas
- `contact-sheet.png` - visual preview of the animation states

![Rover pet contact sheet](contact-sheet.png)

## Installation

Copy the pet files into your Codex pets directory:

```bash
mkdir -p ~/.codex/pets/rover
cp pet.json spritesheet.webp ~/.codex/pets/rover/
```

Then restart the Codex desktop app, or select `Rover` from the appearance / pet settings if it appears there.

If Codex asks for a manifest path, use:

```text
~/.codex/pets/rover/pet.json
```

## Animation Format

The pet uses the standard Codex custom pet atlas layout:

- Atlas size: `1536x1872`
- Cell size: `192x208`
- Grid: `8` columns x `9` rows
- Format: transparent WebP

Included Codex states:

| Row | State |
| --- | --- |
| 0 | idle |
| 1 | running-right |
| 2 | running-left |
| 3 | waving |
| 4 | jumping |
| 5 | failed |
| 6 | waiting |
| 7 | running |
| 8 | review |

## Source Attribution

This pet was converted from the Rover animation frames in the original repository:

[youngjae99/rover-app](https://github.com/youngjae99/rover-app)

The source frames come from `rover/Resources/*/*.png` in that repository. They were rearranged, scaled, and mapped into the 9-row Codex pet spritesheet format.

Approximate state mapping:

| Codex state | Source animation folder |
| --- | --- |
| idle | `_1Idle` |
| running-right | `Come` |
| running-left | `Come` mirrored |
| waving | `_4Idle` |
| jumping | `Haf` |
| failed | `Ashamed` |
| waiting | `GetAttention` |
| running | `Eat` |
| review | `Reading` |

Thanks to the original Rover.app project for collecting and adapting the Rover assets. This package is not affiliated with Microsoft.

## Validation

The generated atlas was checked for the Codex pet format:

- `spritesheet.webp` is `1536x1872`
- Used cells are non-empty
- Unused cells are transparent
- Transparent pixels have no hidden RGB residue
- `pet.json` and `spritesheet.webp` are staged together as an installable pet

## License / Rights

Before redistributing this package, please review and follow the license and asset usage requirements of the original repository and the original Rover / Windows XP assets.

The conversion notes and manifest in this package may be reused freely. Rover and the original animation assets belong to their respective rights holders.
