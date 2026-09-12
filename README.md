# 🎮 Neon Brick Breaker Pro

![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-yellow.svg)
![Status](https://img.shields.io/badge/Status-Playable-brightgreen.svg)

A **neon-themed Breakout/brick-breaker game** built with vanilla JavaScript and HTML5 Canvas — featuring dynamic power-ups, a combo scoring system, particle effects, and progressive difficulty. No frameworks, no build tools, just a canvas and a game loop.

---

## 📋 Overview

Neon Breaker Pro reimagines the classic brick-breaker with a glowing neon aesthetic, a full main menu with difficulty selection, and gameplay mechanics that go well beyond a basic Breakout clone — combo multipliers, four distinct power-ups, multiple brick layout patterns, and persistent high scores.

## ✨ Features

- 🕹️ **Classic Breakout Gameplay** — paddle, ball physics, and destructible bricks, controllable by mouse or arrow keys
- 🎚️ **Three Difficulty Levels** — Easy, Normal, and Hard, each adjusting brick count, paddle size, and starting lives
- ⚡ **Four Power-Ups** — Laser (shoot bricks), Multi-Ball, Paddle Expand, and Slow Motion, each with its own timer and visual effect
- 🔥 **Combo Multiplier System** — chaining brick hits increases your score multiplier and temporarily speeds up the ball
- 🧱 **Randomized Brick Patterns** — solid, checkerboard, and pyramid layouts generated per level
- ✨ **Particle Effects** — collision sparks, brick destruction bursts, and glowing trails
- 🏆 **Persistent High Scores** — saved per difficulty via `localStorage`, no backend required
- ⏸️ **Pause / Resume / Restart** — full game state controls, keyboard shortcut (`P`) included

  <img width="1920" height="1773" alt="image" src="https://github.com/user-attachments/assets/faee6912-533b-479a-aedc-6fef025b8eeb" />


## 🎮 Controls

| Input | Action |
|---|---|
| Mouse movement | Move paddle |
| `←` / `→` | Move paddle (keyboard alternative) |
| `Space` | Fire laser (when laser power-up is active) |
| `P` | Pause / Resume |

## 🛠️ Tech Stack

| Category | Details |
|---|---|
| Rendering | HTML5 `<canvas>` (2D context) |
| Logic | Vanilla JavaScript (ES6) |
| Styling | Custom CSS (gradients, backdrop blur, animations) |
| Icons | Font Awesome (CDN) |
| Persistence | Browser `localStorage` (high scores, selected difficulty) |

## 📁 Project Structure

```
Neon-Breaker-Pro/
├── index.html    # Main menu — difficulty select, controls guide, high scores
├── game.html     # Gameplay screen — canvas, HUD, game loop
└── README.md
```

> ⚠️ File names matter: `index.html`'s "Launch Game" button navigates to `game.html` by name, and `game.html`'s "Menu" button navigates back to `index.html`. Keep these exact names if cloning or renaming.

## ▶️ How to Run

No build step, server, or dependencies required — everything runs client-side.

```bash
git clone https://github.com/<your-username>/Neon-Breaker-Pro.git
cd Neon-Breaker-Pro
open index.html
```

## 🌐 Play It Live

Since this is pure client-side HTML/CSS/JS, you can host it for free with **GitHub Pages**:
1. Repo → **Settings** → **Pages**
2. Source: `main` branch, root folder → Save
3. Play at `https://<your-username>.github.io/Neon-Breaker-Pro/`

   <img width="1920" height="1433" alt="image" src="https://github.com/user-attachments/assets/8c4f136d-b8b1-4d43-abfb-a13b333f3d7e" />


## 🧠 Implementation Notes

- Game state (score, lives, active power-ups, bricks) is tracked in plain JS objects/arrays and driven by a `requestAnimationFrame` game loop (`update()` → `draw()`)
- Power-ups use a `Map` to track multiple simultaneously active effects with independent countdown timers
- Difficulty selected on the main menu is passed to the gameplay screen via `localStorage`, avoiding URL parameters
- Brick layouts are randomly chosen each level from three patterns (solid, checkerboard, pyramid) for replay variety

## 📚 What I Learned

- Building a real-time game loop and collision detection system (ball-paddle, ball-brick, ball-wall) from scratch
- Managing multiple simultaneous timed effects (power-ups) cleanly using a `Map`
- Using `localStorage` for lightweight persistence (high scores, settings) without a backend
- Creating visual polish (particles, glow effects, combo animations) with plain Canvas drawing and CSS

## 🔮 Future Improvements

- Add sound effects and background music
- Mobile/touch controls for paddle movement
- Additional power-ups (shield, extra life, fireball)
- Global leaderboard with a backend instead of local-only high scores

## 👩‍💻 Author

**Fatima Nadeem**

## 📎 Notes

- Requires an internet connection on first load (Font Awesome is loaded via CDN)
- High scores are stored per-browser via `localStorage` — they won't sync across devices
- Tested in modern Chromium/Firefox browsers
