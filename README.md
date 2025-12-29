# ✈️ Paper Drift — 2.5D Paper Plane Flight Game

**Paper Drift** is a relaxing, skill-based **2.5D paper plane flying game** built as a modern web app using **Three.js** and a **custom flight physics system**.  
Inspired by real paper plane contests, the core objective is simple:

> **Stay in the air as long as possible before touching the ground.**

No combat. No stress. Just air, flow, and mastery.

---

## 🎮 Gameplay Overview

- The plane launches automatically and begins gliding
- You control **pitch**, **yaw**, and a temporary **jet assist**
- Wind thermals can be used to gain altitude
- The **flight timer** starts when the plane begins moving
- The timer **stops the moment the plane touches the ground**
- Highest time wins

This mirrors real-world paper plane *time-aloft* competitions.

---

## 🕹️ Controls

### Keyboard
| Key | Action |
|---|---|
| ↑ / ↓ | Pitch up / down |
| ← / → or A / D | Turn left / right |
| Space | Jet mode (uses fuel) |
| R | Reset flight |

### Mouse (if enabled)
- Move up/down → pitch
- Move left/right → yaw

---

## 🚀 Jet Mode

Jet mode temporarily allows **jet-style flight**:

- Continuous forward thrust
- Reduced gravity effect
- Stronger lift
- Limited by **jet fuel**

### Jet Fuel Rules
- Max fuel: **5 seconds**
- Fuel drains while jet is active
- Jet stops automatically when fuel reaches zero
- Fuel refills on reset

Jet mode is designed to **enhance**, not replace, glide skill.

---

## 🌬️ Flight Physics (Custom)

Paper Drift does **not** use a physics engine.

Instead, it implements a handcrafted flight model featuring:

- Gravity
- Lift based on speed and angle of attack
- Drag that increases during sharp turns
- Stall behavior at low speed or high pitch
- Wind thermals (vertical lift zones)
- Gentle auto-stabilization for accessibility

The goal is **believable and expressive flight**, not strict realism.

---

## ⏱️ Flight Timer Rules

- Timer starts automatically when flight begins
- Timer runs only while the plane is above the ground
- Ground level is defined by the world grid
- Once the plane crosses below ground:
  - Timer stops
  - No reset, no crash animation
  - Final time remains visible
- Press **R** to try again

---

## 🧱 Tech Stack

- **Three.js** — rendering & scene management
- **Vanilla JavaScript (ES Modules)** — game logic
- **Custom physics loop** — deterministic, frame-safe
- **HTML / CSS** — lightweight UI

No build tools required.

---

## ▶️ How to Run Locally

> Because ES modules are used, the game must be served via a local web server.

### Option 1: VS Code Live Server (Recommended)
1. Install **Live Server** extension
2. Right-click `index.html`
3. Select **Open with Live Server**

### Option 2: Simple Local Server

#### Using Node.js
```bash
npx serve .
```

Then open
```http://localhost:8000```

## Project Structure

```
paper-drift/
├── index.html
└── README.md
```
(Designed to be easily expandable into modules later.)

## Design Philosophy

- Feel > realism
- Readable mistakes
- Minimal UI
- Short sessions
- High skill ceiling, low friction

Paper Drift is about flow, not force.

## Planned / Possible Enhancements

- Best-time tracking (localStorage)
- Jet fuel pickups
- Zen mode (no UI, no score)
- Plane archetypes with different physics
- Mobile touch controls
- Visual exhaust effects for jet mode

## Credits

Built using Three.js
Concept inspired by real-world paper plane flight contests

Enjoy the glide!