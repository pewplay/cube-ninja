# Cube Ninja for PewPlay

This directory contains the original static game adapted for the PewPlay game template. Open `index.html` to play.

`game.json` holds the game page text. `preview.png` and `cover.png` provide the page images. The PewPlay workflow checks pushes to `preview` and `main`. The game remains a draft until you remove `"draft": true` after reviewing it.

Game controls: Start a round and slice the moving targets while avoiding mistakes. Use the on-screen menu to replay.

## Update (October 2026)

- Slicing rewritten on Pointer Events (mouse, touch, pen) with pointer capture and `pointercancel`; swipe speed is now frame-rate independent (works on 120 Hz screens) and the slice threshold adapts to small screens.
- Canvas fills the frame at any size/orientation, re-reads devicePixelRatio on resize, scene adapts to portrait and short landscape screens (cube launch speed scales with the scene height).
- Menus/HUD restyled to be readable and tappable on a 390 px phone (≥ 48 px buttons, safe-area insets), main menu shows a hint and the best score.
- Auto-pause when the page is hidden; P or Esc toggles pause. Duplicate menu handlers removed.
- High score now stored as `cube-ninja:highScore` (old saves are not imported).
- New cover, screenshots and a redrawn, centred preview icon.
