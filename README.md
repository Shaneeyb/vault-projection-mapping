# VΛULT — Free Browser-Based Projection Mapping

**[🔗 Launch VAULT](https://vaultmapping.netlify.app/)**

VAULT is a free, browser-based projection mapping tool built for tabletop RPG players, VJs, and anyone who wants to warp video or images onto surfaces using a projector. No downloads, no installs, no accounts. Just open and go.

![VAULT Screenshot](screenshot.png)

## Features

- **Projection mapping** — Drag corner pins to warp your image/video onto any surface. Add extra control points along edges for irregular shapes.
- **Zoom & Pan** — Click +/− to zoom in whole number steps (1×, 2×, 3×…) or scroll wheel for smooth zoom. Shift+drag, right-drag, or arrow keys to pan. Minimap shows your viewport position. Works with projection mapping.
- **Fog of War** — Cover the map in darkness. Paint with an adjustable brush to reveal areas as the party explores. DM sees a dimmed preview of hidden areas; players see only what's been revealed (full black). Toggle between Reveal and Cover modes with a Paint on/off button so the brush isn't always active. Each clip has its own fog mask — switch maps and come back with fog intact. Reset button to re-cover everything.
- **Grid Calibration** — Click the 4 corners of any grid square and VAULT auto-detects the full grid, handling rotation and skew. Toggle overlay with adjustable opacity and color. Grid only appears in revealed areas when Fog of War is active. Each clip stores its own grid — switch maps and your calibration persists.
- **Atmosphere FX** — Toggle Fog, Rain, Snow, Embers, Fireflies, and Torch Flicker effects with adjustable intensity. All effects overlay on the projected output.
- **Video + Image support** — Load battle maps, animated scenes, static images, or video loops
- **Two layers with 10 slots each** — Blend content (e.g., a map on Layer A + weather effects on Layer B). Clips auto-activate when added.
- **Color presets** — Neutral, Warm, Cool, Sunset, Neon, Moody, Vintage, Ice — with adjustable strength
- **Color controls** — Brightness, contrast, saturation, hue rotation, and color tint with picker
- **Transform** — Scale, rotate, and playback speed controls
- **Seamless video looping** — Double-buffer system eliminates black frames between loops
- **Output window** — Pop out a separate window for your projector, keeps controls on your main screen. DM sees the full map with dimmed fog; output shows only what players should see, warped to fit the table.
- **Preview window** — Clean unmapped feed for a TV or second monitor so players can see the map without projection distortion. Includes fog of war, grid, and atmosphere. Runs at 30fps to keep performance smooth.
- **Save/Load projects** — Save your mapping, colors, fog, grid, atmosphere, and settings as a `.vault` file. Reload between sessions (re-import clips into matching slots).
- **Blackout** — One-click to black out the output for dramatic moments
- **100% client-side** — No data ever leaves your browser. All processing happens locally.

## How to Use

### Quick Start
1. Open [vaultmapping.netlify.app](https://vaultmapping.netlify.app/) (or open `index.html` locally)
2. Click a slot in Layer A and load an image or video
3. Click **⬡ Output** and drag the window to your projector
4. Click **◈ Map** and drag the corners to fit your surface
5. Hit **✓ Save & Close** — done!

### Self-Hosting
VAULT is a single HTML file with zero dependencies. To run it locally:

1. Download or clone this repo
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari)
3. That's it. No server, no build step, no npm install.

### For D&D / Tabletop RPGs
- Set your projector as an **extended display** (not mirrored)
- Load your battle maps into the 10 slots before your session
- **Scroll to zoom** into the area your party is exploring — the zoomed view projects through your mapping
- **Shift+drag** or **arrow keys** to pan around while zoomed (right-click drag also works)
- Press **Esc** or **0** to reset zoom. **+/-** keys also zoom in/out.
- **Calibrate the grid** — click ⊞ Calibrate Grid, then click the 4 corners of one grid square. VAULT auto-detects the full grid including rotation and skew. Each map remembers its own grid.
- **Fog of War** — Enable in the sidebar, click Paint, and brush over areas to reveal as your party explores. Toggle Cover mode to hide areas again. Each map keeps its own fog state.
- Use the **Preview window** on a wall-mounted TV so players can see the map without projection distortion
- Use Layer B for ambient effects (fog, fire, weather) blended over your map
- Use color presets to set mood — "Moody" for dungeons, "Warm" for taverns
- **Save your project** so mapping, fog, grid, and zoom persist between sessions

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `+` / `-` | Zoom in/out (whole steps) |
| `0` / `Esc` | Reset zoom |
| Arrow keys | Pan while zoomed |
| `B` | Toggle blackout |

## Tech

- Pure HTML/CSS/JavaScript — no frameworks, no dependencies
- Canvas 2D rendering with real-time compositing
- Double-buffer video system for seamless looping
- Fan triangulation from centroid for multi-point mesh warping
- Per-clip fog masks and grid calibration stored in memory
- Preview window throttled to 30fps for performance
- All processing client-side — works offline after first load

## License

MIT License — free to use, modify, and distribute.

## Support

If you find VAULT useful, you can [buy me a coffee ☕](https://venmo.com/shane-burke)

Built with ❤️ for the D&D and projection mapping community.
