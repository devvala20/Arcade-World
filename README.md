# 🕹️ Arcade-World

> Play classic retro WebAssembly games directly in your browser, powered by the [WASM-4](https://wasm4.org) fantasy console and Express.js.

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org)
[![Express](https://img.shields.io/badge/Express-4.21.2-blue.svg)](https://expressjs.com)
[![EJS](https://img.shields.io/badge/EJS-3.1.10-yellow.svg)](https://ejs.co)
[![WASM-4](https://img.shields.io/badge/Runtime-WASM--4-purple.svg)](https://wasm4.org)
[![License: ISC](https://img.shields.io/badge/License-ISC-brightgreen.svg)](LICENSE)

---

## 🌟 Overview

**Arcade-World** is a curated retro gaming web portal. It delivers lightweight, high-performance 8-bit fantasy console games compiled to WebAssembly (WASM-4 carts) embedded inside an immersive dark-mode arcade web interface with background music and ambient video styling.

---

## 🚀 Features

- 🎮 **25+ Retro Arcade Games**: Handpicked WASM-4 titles ranging from puzzle games to action and platformers.
- ⚡ **Zero Client Build Required**: Server-rendered dynamic pages using Express and EJS with instant page loads.
- 🎵 **Atmospheric Audio & Video**: Ambient retro background audio and video effects with toggle controls.
- 🕹️ **Pure WASM Performance**: Low-latency, sandboxed WebAssembly execution via the WASM-4 runtime.
- 📱 **Responsive Grid Layout**: Clean, dark-mode catalog that adapts smoothly across screens.
- ⌨️ **Keyboard Controls**: Standard retro gaming bindings (D-Pad / Arrow keys + Action buttons).

---

## 🛠️ Tech Stack

- **Runtime Environment:** Node.js
- **Server Framework:** Express.js (v4.21.2)
- **Template Engine:** EJS (v3.1.10)
- **Game Engine / VM:** WASM-4 WebAssembly Fantasy Console
- **Styling:** CSS3 (Custom Dark & Arcade Aesthetic, Responsive Grid, FontAwesome)

---

## 📁 Project Structure

`
Arcade-World/
├── Games/
│   ├── HTML/             # HTML wrappers for each game
│   │   ├── bubblewrap.html
│   │   ├── snake.html
│   │   ├── watris.html
│   │   └── ... (25 games)
│   └── WASM/             # Precompiled WASM-4 binary game carts (.wasm)
│       ├── bubblewrap.wasm
│       ├── snake.wasm
│       ├── watris.wasm
│       └── ...
├── public/
│   ├── css/
│   │   └── style.css     # Global styles and layout
│   ├── images/           # Game thumbnail preview covers
│   └── media/            # Ambient background video & soundtrack
│       ├── background.mp3
│       ├── background.mp4
│       └── game.mp3
├── views/
│   ├── 404.ejs           # Not found page
│   ├── about.ejs         # About Arcade-World info
│   ├── game.ejs          # Game runner & iframe viewport
│   └── home.ejs          # Catalog grid & header showcase
├── .gitattributes        # Git attributes configuration
├── .gitignore            # Git ignore rules
├── package.json          # Project metadata and dependencies
└── server.js             # Express application & game routing
`

---

## 🎮 Available Games

| # | Game Title | Category / Description |
|---|------------|------------------------|
| 1 | **Bubblewrap** | Satisfying virtual bubble-popping puzzle |
| 2 | **Fools Paradise** | Pixel adventure exploration |
| 3 | **Glowfish Chess** | Minimalist chess against chess AI |
| 4 | **Hills Moonlight** | Nighttime platformer journey |
| 5 | **Heroes of the Wild** | Retro fantasy action |
| 6 | **Lad 2024** | Arcade retro adventure |
| 7 | **Lumber Night** | Fast-paced woodchopping reflex game |
| 8 | **Ninja vs Knights** | Action combat platformer |
| 9 | **Nyan Cat** | Classic flying rainbow feline runner |
| 10 | **Phantom Shift** | Tactical puzzle stealth game |
| 11 | **Piano** | Interactive 8-bit synthesizer keyboard |
| 12 | **Presents to the Metal** | High-speed holiday delivery |
| 13 | **Punch 'Em Up** | Street-brawler combat game |
| 14 | **Skipahead** | Precision timing platformer |
| 15 | **Snake** | Classic grid-based retro snake |
| 16 | **Tankle Adventure** | Top-down tank puzzle exploration |
| 17 | **Tankle** | Tactical arena tank battles |
| 18 | **Tic-Tac-Toe** | Strategic 3x3 board game |
| 19 | **Tiny Pong** | Classic 2-player paddle duel |
| 20 | **Train** | Railway route management puzzle |
| 21 | **Untangle** | Geometric knot untangling challenge |
| 22 | **Wasm4nia** | Rhythm mania arcade challenge |
| 23 | **Watris** | Tetris-inspired block-stacking puzzle |
| 24 | **Wormhole** | Space portal arcade shooter |
| 25 | **ZXZ** | Fast-paced retro arcade shooter |

---

## ⌨️ Controls & Keybindings

All games utilize the WASM-4 fantasy console controller scheme:

| Action | Player 1 (Keyboard) | Gamepad |
|--------|---------------------|---------|
| **Directional Movement** | Arrow Keys or W, A, S, D | D-Pad / Left Stick |
| **Primary Action (Button 1)** | X or V | A / Cross |
| **Secondary Action (Button 2)** | Z or C | B / Circle |
| **Reset Game** | R | Select / Back |
| **Fullscreen** | F | - |

---

## ⚡ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (version 18 or higher recommended)
- [npm](https://www.npmjs.com/) (bundled with Node.js)

### 1. Clone the Repository

`ash
git clone https://github.com/devvala20/Arcade-World.git
cd Arcade-World
`

### 2. Install Dependencies

`ash
npm install
`

### 3. Start the Server

`ash
npm start
`

### 4. Play in Your Browser

Open your browser and navigate to:
`
http://localhost:3001
`

---

## 🧩 Architecture & How It Works

1. **Dynamic Game Discovery**: On startup, server.js scans the Games/HTML/ directory, extracts game identifiers, and formats display titles and metadata dynamically.
2. **EJS Templating**: When a user accesses /, iews/home.ejs renders the catalog with live cover images and descriptions.
3. **Sandboxed Iframes**: Launching a game routes to /game/:id, which embeds /game-content/:id in an isolated viewport alongside audio controls and player guidelines.

---

## 📄 License & Credits

- Platform code licensed under the [ISC License](LICENSE).
- Individual games are created by the [WASM-4](https://wasm4.org) community and their respective authors.
