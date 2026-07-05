# Police Chase - Endless Runner Game

A fast-paced, side-scrolling endless runner game built with vanilla JavaScript and HTML5 Canvas. Dodge obstacles, collect power-ups, and survive as long as you can!

## Live Demo

[Play the game on Vercel](https://police-chase-two.vercel.app)

## Gameplay

- **Objective**: Run as far as possible without hitting obstacles
- **Control**: Tap/Space to jump over red obstacle blocks
- **Scoring**: Your score increases the longer you survive
- **Difficulty**: Game speed gradually increases over time

### Controls

| Action | Desktop | Mobile |
|--------|---------|--------|
| Jump | Space bar | Tap screen |
| Restart (Game Over) | Space bar | Tap screen |

### Power-ups

Collect colored power-up blocks to gain temporary advantages:

| Power-up | Color | Effect |
|----------|-------|--------|
| Score Multiplier | Gold (`#ffd700`) | Doubles score gain for 5 seconds |
| Shield | Deep Sky Blue (`#00bfff`) | Absorbs one obstacle hit |
| High Jump | Lime Green (`#32cd32`) | Increased jump height for 5 seconds |
| Slow Time | Blue Violet (`#8a2be2`) | Slows down game speed for 5 seconds |

## Features

- **Endless procedural generation** — obstacles and power-ups are randomly generated
- **Parallax scrolling background** — creates a sense of depth
- **Progressive difficulty** — game speed increases as you play
- **Power-up system** — 4 different power-ups with visual feedback
- **High score tracking** — persisted in browser's localStorage
- **Mobile-friendly** — responsive canvas with touch support
- **Visual feedback** — shield circle, active power-up indicators on HUD

## How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/police-chase.git
   cd police-chase
   ```

2. **Open in browser:**
   Simply open `index.html` in any modern web browser.

   No build tools, dependencies, or server required — it's pure HTML, CSS, and JavaScript.

## Project Structure

```
police-chase/
├── index.html          # Main HTML page with canvas and styles
├── script.js           # Complete game logic (classes, physics, rendering)
├── README.md           # Project documentation
└── icon.png            # Favicon
```

### Code Overview

- **`index.html`** — Contains the canvas element, responsive CSS, and viewport meta tag for mobile
- **`script.js`** — All game code organized into classes:
  - `Player` — Player character physics (gravity, jumping)
  - `Obstacle` — Red obstacle blocks that scroll from right to left
  - `PowerUp` — Collectible power-ups with random types
  - `Game` — Main game controller (loop, collision, difficulty, UI)

## Technical Details

- **Rendering**: HTML5 Canvas 2D API
- **Game Loop**: `requestAnimationFrame` with delta-time calculation
- **Physics**: Simple gravity simulation (velocity + ground collision)
- **Collision Detection**: Axis-Aligned Bounding Box (AABB) overlap check
- **Persistence**: `localStorage` for high scores
- **Mobile**: Touch event listeners (`touchstart`) with `preventDefault()` to disable scroll/zoom

## Deployment

This game is deployed on **Vercel**. To deploy your own copy:

1. Push the code to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and import the GitHub repo
3. Vercel will auto-detect it as a static site — no configuration needed
4. Your game will be live at a `*.vercel.app` URL

## License

This project is for educational and entertainment purposes.
