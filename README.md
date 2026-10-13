# Creature Color Studio

A single-page RGB calibration tool for creature skins. Paint ten anatomical channels, then export them as one space-delimited stream of 30 integers.

Everything lives in [`index.html`](index.html). There is no build step and no install.

## Open it

Open `index.html` in a browser. The page loads Tailwind and fonts from a CDN, so it needs a network connection the first time those assets are fetched.

## How to use

1. Pick a channel from the overview grid, or step through them with the previous and next buttons.
2. Set the color with the hue/saturation wheel, the brightness slider, the R/G/B sliders, the number fields, or a typed `r, g, b` value.
3. Copy the active channel as `r, g, b`, or open **Export RGB** to copy the full palette.

**Theme** loads a named preset across all ten channels. **Randomize** builds a new harmonious palette. **Default** restores the selected channel to its starting color.

## Channels

Export order is fixed, from Body through Claws:

| Slot | Channel      | Role                           |
| ---- | ------------ | ------------------------------ |
| 1    | Body         | Primary pigmentation           |
| 2    | Markings     | Dorsal stripes and patterns    |
| 3    | Flank        | Lateral torso shading          |
| 4    | Underbelly   | Belly and throat               |
| 5    | Detail 1     | Spine ridges and accents       |
| 6    | Eyes         | Iris                           |
| 7    | Male Display | Crest, plumage, and dimorphism |
| 8    | Teeth        | Enamel                         |
| 9    | Mouth        | Oral cavity                    |
| 10   | Claws        | Talons                         |

## Export format

**Export RGB** copies one line of space-separated integers, three per channel, in the order above:

```
59 66 82 235 94 40 76 86 106 216 222 233 235 203 139 208 135 112 180 142 173 236 239 244 191 97 106 46 52 64
```

Each value is an integer from 0 to 255. The example above is the Apex Predator preset (also the default palette).
