# fur-generator

A single-file fur texture generator. Open `Fur.html` in a browser and it fills the page with procedurally drawn fur, rendered on a canvas in four layered passes. A control panel drives colour, density, strand length, flow direction, swirl, and curl. Everything is seeded, so a seed plus settings reproduces the same texture every time.

## Running it

No build step and no dependencies beyond Google Fonts. Open the file directly, or serve the folder:

```
python3 -m http.server
```

## Controls

- Colour: base hue, hue spread, saturation, base lightness
- Tone: brightness and contrast
- Fur: density, strand length, thickness, clumping and clump size
- Flow: direction, swirl strength and size, curl, jitter
- Seed: type a number or hit Shuffle

Sliders redraw at reduced quality while you drag, then repaint at full quality on release.

## Exporting

Everything saves as a normal browser download. Four options: a PNG at 1–3× screen size, the current settings as JSON, a standalone HTML page, and a standalone script with your settings baked in. The script saves as `.txt`; rename it to `fur.js` before use.

The baked script textures any element carrying a `data-fur` attribute, or fills the whole page behind your content if nothing is marked.
