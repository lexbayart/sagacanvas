# SagaCanvas — Complete User Guide

> Everything you need to know to use the free-form storyboarding canvas. For film and animation creators who want to draw without constraints.

---

## Getting Started

Open the app in your browser. You'll see a dark canvas with a single off-white rectangle in the center — this is your **frame**, the drawing window.

The frame is like a piece of film stock lying on an infinite table. Everything you draw inside it is visible. Everything you draw outside it is hidden, waiting in the margins.

---

## 🖱️ Navigation

### Drawing
Click and drag anywhere on the canvas to draw. Your strokes are stored on the infinite surface, not just inside the frame.

### Panning the camera
- **Mouse wheel** — scroll to pan across the canvas
- **Trackpad** — two-finger drag to pan
- The frame will move with the canvas as you pan. If it drifts off-center, a green highlight ring appears around it.

### Zooming the camera
- **Trackpad pinch** — pinch to zoom in/out (0.25× to 4×)
- **+/− buttons** — bottom-right corner of the screen
- The zoom percentage is displayed between the buttons

### Recentering the frame
When the frame drifts away from the center of your screen:
- A **green focus ring** appears around the frame when your cursor hovers over it
- **Click the ring** to smoothly animate the frame back to the center of the viewport
- Alternatively, click the **pen tool** (✏) in the toolbar — it always recenters the view

When the frame is completely off-screen, the pen button glows green to let you know you can click it to find the frame again.

---

## 🎨 Tools

The toolbar at the top of the screen has three buttons:

| Button | Action |
|--------|--------|
| ✏ Pen | Drawing tool. Also recenters the view when clicked. |
| ⌫ Eraser | Erase strokes. Click and drag over existing ink to remove it. |
| ✕ Clear | Wipe the entire canvas — all strokes, inside and outside the frame. |

---

## 📐 Frame Handles

The frame has four corner handles that appear when you hover near the corners. Each corner does something different:

### Bottom-right corner — Resize the viewport
Drag to grow or shrink the frame window. The content inside stays at the same scale — you're just revealing more or less of the underlying drawing. Think of it as changing the size of the window, not the drawing.

### Top-right & bottom-left corners — Zoom the content
Drag to uniformly scale everything inside the frame (your drawing grows or shrinks with the frame). The frame's aspect ratio is preserved. This is like zooming into your artwork.

### Top-left corner — Change the format (aspect ratio)
Drag to snap the frame to a standard cinematic aspect ratio. As you drag, the app detects the nearest preset and the frame elastically animates to match it. A label shows which ratio is active.

Available presets:
- **2.39:1** — Ultra-wide cinematic
- **2:00:1** — Flat cinema
- **1.85:1** — Standard widescreen
- **16:9** — HD / digital
- **1:1** — Square
- **4:3** — Classic / SD
- **9:16** — Vertical / mobile

The format change is anchored at the frame's center and uses a rubber-band easing animation. The label fades out once the frame settles.

---

## 🔄 How ink works

This is the key concept in SagaCanvas:

- **Inside the frame** — strokes appear in dark ink (visible)
- **Outside the frame** — strokes appear in faint white (hidden, but still there)
- **Resize the frame** — as the edge sweeps over hidden strokes, they turn black in real time. As it moves away, visible strokes turn white.
- **Nothing is ever deleted** by resizing. The drawing lives on the infinite surface; the frame is just a viewport.

This means you can draw freely without worrying about staying inside the lines. If you go outside, just resize or reposition the frame to bring your strokes into view.

---

## ⚠️ Known Limitations

- **Single frame only** — v0.2 has one drawing window. Multi-frame storyboarding is planned.
- **No undo** — there is no undo/redo history. Clear is permanent.
- **No export** — saving your work is not yet implemented.
- **No text tool** — annotations must be drawn by hand.
- **Single file** — all data lives in memory; refreshing the page loses everything.
- **No layers** — everything draws on the same surface.

---

*This guide covers SagaCanvas v0.2. The app is in active development.*
