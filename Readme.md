# image-pulsate-glow.html  : Interactive Glow Logo Editor

A lightweight, self‑contained HTML/CSS/JS tool that lets you apply and preview a pulsing, multi‑tone drop‑shadow glow around any image—or your star logo—then export your settings or a standalone HTML snippet.



https://github.com/user-attachments/assets/aa929bde-ab68-4966-9682-6d5968cf26ab

## Features

* **Custom Image Upload**: Replace the default logo with your own image via drag‑and‑drop or file picker.
* **Glow Controls**:

  * **Color Pickers** for four shadow layers to create a rich, gradient glow.
  * **Pulse Duration Slider** to set how fast the glow pulses.
  * **Shadow Width Slider** to adjust the base blur radius of the glow.
* **Live Preview**: Changes take effect immediately using CSS variables and `drop-shadow` filters.
* **Export Settings**: View your current configuration as JSON.
* **Export HTML**: Generate a standalone HTML file (with inlined CSS) referencing your image filename—no JS needed to recreate the effect.

## Getting Started

1. **Open** `index.html` in your browser.
2. **Upload** an image or use the default `logo1.png`.
3. **Adjust** colors, pulse duration, and shadow width in the settings card at the top‑right.
4. **Export**: Click **Export** to view a modal where you can:

   * Switch to **Settings**: copy JSON of your parameters.
   * Switch to **Export HTML**: copy a complete HTML+CSS snippet ready for embedding.

## How It Works

* **CSS Variables**: Root-level variables (`--c1…--c4`, `--pulse-time`, `--shadow-width`) drive both the `filter: drop-shadow(...)` layers and the `@keyframes pulseGlow` animation.
* **JavaScript**: Listens for input events on color pickers, range sliders, and file uploads; updates CSS variables and image `src` in real time.
* **Modal Export**: Collects computed CSS variables and current image filename to build:

  * A **JSON** representation of the glow settings.
  * A **Standalone HTML** document with inlined CSS using your chosen parameters.

## File Structure

```
├─ index.html       # Main interactive interface
├─ logo1.png        # Default logo (replaceable)
└─ README.md        # This documentation
```

## Customization

* Tweak default values in the `:root` CSS block.
* Modify the `width` of `.glow-logo` for different image sizes.
* Enhance the UI by updating the `.settings-card` styles or adding more controls.

---

Enjoy creating glowing logos with ease! Feel free to share feedback or improvements.

