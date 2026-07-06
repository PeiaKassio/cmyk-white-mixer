# CMYK+White – mix paints like real tubes

CMYK+White is a single-page paint mixing game and paint mixing simulator. It lets you mix cyan, magenta, yellow, black and white in simple ratios, like squeezing real paint from tubes onto a palette.

Use it to test a color idea before wasting real paint: add parts from the tubes, compare the resulting color, save useful mixes, and practice matching target colors.

## Live demo

Play the GitHub Pages demo: <https://github.com/PeiaKassio/cmyk-white-mixer>


## How to play

1. Open `index.html` in a browser or visit the GitHub Pages demo.
2. Choose **Free mixing** to experiment or **Match the target** to play the challenge mode.
3. Use the `+` and `−` buttons beside **Cyan**, **Magenta**, **Yellow**, **Black** and **White** to add or remove paint parts.
4. Watch the paint blob and reduced ratio update as you mix.
5. Click **Save mix** to add the current color to your palette and reuse it in later mixes.
6. Click **Clear palette** to remove all active parts from the current mix.
7. In target mode, click **New target color** or **Next target** to continue practicing.

## Why doesn't cyan + yellow make gray on a computer?

Screens normally use RGB light mixing: red, green and blue light are added together, so more light makes colors brighter. Paint uses subtractive pigment mixing: pigments absorb parts of the light and reflect what remains. Cyan and yellow pigments can make green because cyan absorbs reddish light while yellow absorbs bluish light, leaving more green reflected back to your eye.

A simple RGB average of cyan and yellow can look dull or gray because it is blending screen color values, not modeling how real pigments absorb and scatter light. This game uses pigment-oriented mixing so colors behave more like real paint than a basic computer color picker.

## Tech notes

- No build step: the whole game lives in `index.html`, so it can run directly on GitHub Pages.
- Color mixing uses [Mixbox](https://scrtwpns.com/mixbox/) when the library loads from its script tag.
- If Mixbox cannot load, the page falls back to a built-in Kubelka-Munk-style simulation so the game still works offline or without the external script.
- The app is written in vanilla HTML, CSS and JavaScript.

## Attribution

Color mixing powered by Mixbox © Secret Weapons, licensed CC BY-NC 4.0. This project is non-commercial.

## License

This repository's original code is licensed under the MIT License. Mixbox itself remains under CC BY-NC 4.0 and is not relicensed by this project.
