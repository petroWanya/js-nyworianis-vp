# JS NYWORIANIS VP

**A pure JS/Canvas 3D orrery engine** with realistic perspective projection, Keplerian orbital mechanics, and procedurally generated planet textures. All objects — stars, planets, moons, rings, and asteroid belts — are depth-sorted for proper occlusion and rendered with perspective scaling.

> Licensed under **CC BY 4.0** — free to use, share, and modify.

---

## Key features

- **Full 3D engine from scratch** — Custom vector math, spherical-coordinate orbital camera, 3D→2D projection, frustum culling, and painter's algorithm — no external libraries
- **Physically-inspired orbital mechanics** — Kepler's laws in action: inner planets orbit faster than outer ones, hierarchical "star → planet → moons" system, asteroid belt with individual speeds for each body
- **Procedural texture generation** — 4-octave fBm (fractal Brownian motion) noise creates unique surfaces for gas giants, rocky worlds, ice planets, and lava worlds. Textures are seed-based — no external images required
- **Interactive orbital camera** — Drag to rotate, scroll to zoom, smooth planet following (F key), instant view reset (R), and simulation pause (Space)
- **Real-time visual effects** — 3-layer parallax starfield (600 twinkling stars), ring systems around gas giants, gradient-based global lighting with shadows, atmospheric glow for planets
- **Optimized performance** — Depth-sorted rendering, frustum culling, perspective sprite scaling — smooth even on integrated graphics
- **Adaptive scalability** — Canvas automatically fits any browser window via CSS transform, preserving crisp pixel rendering of stars and textures
- **Fully self-contained** — No server, CDN, external textures, or library downloads. Everything in a single HTML file
- **Cross-platform** — Works in any modern browser on Windows, macOS, Linux, Android, and iOS (including mobile touch devices)
- **Clean, readable code** — Every math class is thoroughly documented in English with explanations of formulas, geometric intuition, and physics principles. Perfect for learning 3D graphics and game math

---

## Live demo

🔗 [View the orrery in action](https://petroWanya.github.io/js-nyworianis-vp)

---

## All-in-one HTML

The entire project is contained in a **single HTML file** — CSS, JavaScript, and Canvas are all embedded inside.  
Just download and open in any browser. No build steps, no dependencies.

---

## How to use

1. **Download** — save `index.html` to your computer
2. **Open the code** — edit the file in any text editor (VS Code, Sublime, Notepad++)
3. **Customize** — all parameters, orbital mechanics, planet types, and visual effects are heavily commented at the top of the script
4. **Run** — double-click the file to open it in your browser and see your changes instantly

No build steps, no compilers, no dependencies — just pure HTML/Canvas.

---

## Controls

|       Action        |       Control      |
|---------------------|--------------------|
| Rotate view         | Drag mouse / touch |
| Zoom in/out         | Scroll / pinch     |
| Pause simulation    | Space bar          |
| Reset camera        | R key              |
| Follow planet       | F key              |
| Return to free view | Escape key         |

---

## Customization

Open the HTML file in any text editor. Everything is heavily commented. You can easily change:

- Orbital radii and speeds (Keplerian parameters)
- Planet types (gas, rocky, ice, lava)
- Texture generation (noise octaves, color palettes)
- Starfield density and parallax layers
- Ring systems and axial tilts
- Camera sensitivity and zoom limits
- Simulation speed and pause behavior

---

## Planetary system architecture

The simulation includes:

- **Nywarianis Prime** — Central K-type star (warm golden glow)
- **Nywarianis b** — Lava world (tidally stressed, volcanic)
- **Nywarianis c** — Rocky habitable-zone planet with 2 moons
- **Nywarianis d** — Gas giant with spectacular rings and 4 major moons
- **Nywarianis e** — Ice giant with faint ring and 1 moon
- **Asteroid belt** — 300 individual particles between c and d

Each planet and moon has:
- Unique procedural texture (generated from seed)
- Proper orbital speed (Kepler's third law: inner orbits faster)
- Independent rotation (day/night cycle)
- Optional ring system with realistic perspective projection

---

## License

This project is licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

You are free to:
- Share — copy and redistribute the material in any medium or format
- Adapt — remix, transform, and build upon the material for any purpose, even commercially

Under the following terms:
- Attribution — You must give appropriate credit, provide a link to the license, and indicate if changes were made.

See the [LICENSE](LICENSE) file or visit [creativecommons.org/licenses/by/4.0](https://creativecommons.org/licenses/by/4.0/)

---

## Technical notes

- **No WebGL** — Uses pure Canvas 2D with manual 3D projection. Every pixel is calculated in JavaScript
- **No textures** — All planet surfaces are procedurally generated using fractal noise. Zero external assets
- **Perspective projection** — `screenX = (focalLength * cameraX) / cameraZ + centerX` — classic pinhole camera model
- **Painter's algorithm** — Objects sorted by depth (farthest to nearest) for correct occlusion
- **Parallax starfield** — 3 distance layers create convincing depth during camera movement

---

## Acknowledgements

Created as a pure JavaScript showcase — no frameworks, no libraries, just Canvas, geometry, and orbital mechanics.

Inspired by real exoplanet demographics observed by Kepler and TESS missions.