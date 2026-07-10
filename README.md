# SagaCanvas 🔷 Beta

> A free-form storyboarding canvas that doesn't tell you where to draw.

---

## 🔷 What makes this different

Most storyboarding tools lock you into a grid of fixed frames, a timeline, or a sequence of slides. They decide the structure for you. SagaCanvas starts from the opposite assumption: **the interface should never constrain the author.**

You get an infinite dark canvas and a single drawing window — a frame that behaves like a physical piece of film stock lying on a table. Draw inside it and your strokes appear in black. Draw outside and they turn white, waiting in the margins. Resize the window and previously-hidden strokes slide into view, turning black as the frame edge sweeps over them. Nothing is ever lost. The drawing exists on the infinite surface; the frame is just a viewport you move and reshape.

This is the core interaction loop of SagaCanvas: draw freely on an unbounded surface, then shape the frame around what you've drawn — or pan away and draw somewhere else entirely. No layers panel. No undo stack. No preset layout. Just pen, eraser, and a window you can stretch, zoom, and reposition however you like.

It's early — this is version 0.2, the very beginning. The core interaction with the frame is worked out. What comes next is where the real tool takes shape.

---

## ✨ Current features

- **Infinite canvas** — draw anywhere; the surface grows as you pan
- **Frame as viewport** — a resizable drawing window on an unbounded surface; ink inside is visible (black), ink outside is hidden (white)
- **Real-time ink classification** — strokes dynamically turn black or white as the frame edge sweeps over them during resize
- **Pen and eraser** — two tools, switchable from the toolbar
- **Clear** — wipe the canvas and start fresh
- **Camera pan** — scroll or two-finger trackpad drag to move across the infinite surface
- **Camera zoom** — pinch gesture or +/− buttons (0.25× to 4×)
- **Frame resize** — bottom-right corner grows/shrinks the viewport without scaling content; top-right and bottom-left corners zoom the content inside the frame
- **Format snapping** — top-left corner snaps the frame to standard cinematic aspect ratios (2.39:1, 2:1, 1.85:1, 16:9, 1:1, 4:3, 9:16) with elastic rubber-band animation
- **Focus ring** — when the frame drifts off-center, a highlight ring appears; click it to smoothly dock the frame back to the center of the viewport
- **Locate button** — when the frame is completely off-screen, the pen button glows to signal you can click it to find the frame again

---

## 🚀 Open it

**[▶ lexbayart.github.io/sagacanvas](https://lexbayart.github.io/sagacanvas/)**

No install. No account. Works offline.

Or download `index.html` from this repo and open it locally — fully standalone, works without internet.

---

## 📖 Documentation

- [**Complete User Guide**](docs/GUIDE.md) — tools, interactions, all features explained

---

## 🛠️ Tech

Vanilla JS · HTML5 Canvas · Zero dependencies · Zero build step · Single HTML file

---

## 🔮 Roadmap

What's being built next:

- **Scene storyboarding** — switching between frames, drawing full storyboards for individual scenes
- **Director's view** — a top-down scene planning mode where you place cameras, characters, and visual annotations as comments on the frames you draw
- **References** — drop in GIFs, images, and script pages alongside your drawings
- **Audio** — attach sound references to frames and scenes
- **Dynamic timeline** — arrange your storyboards into a living timeline for the entire film (secret work in progress)

The philosophy stays the same: the tool follows your process, not the other way around.

---

## 💬 Feedback & Contact

This project is in active development.
Found a bug or have an idea? Reach out:

- **Telegram:** [@lexbay](https://t.me/lexbay)
- **GitHub Issues:** [Open an issue](https://github.com/lexbayart/sagacanvas/issues)

---

## 📄 License

© 2025 lexbayart — [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)

Free to use and share for non-commercial purposes with credit.
Commercial use requires explicit permission from the author.
