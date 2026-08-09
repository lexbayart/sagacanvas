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
- The frame moves with the canvas as you pan. If it drifts off-center, a green highlight ring appears around it.

### Zooming the camera
- **Trackpad pinch** — pinch to zoom in/out (0.25× to 4×)
- **+/− buttons** — bottom of the toolbar
- The zoom percentage is displayed between the buttons

### Moving the drawing (instead of the camera)
The **move tool** (the grip button in the toolbar) shifts the actual ink of the current scene, not the viewport. Press and hold it and drag anywhere — the drawing slides under your fixed cursor. When the frame is out of view, the button turns red so you know you can use it to reach the drawing.

### Recentring the frame
When the frame drifts away from the center of your screen:
- A **green focus ring** appears around the frame when your cursor hovers over it
- **Click the ring** to smoothly animate the frame back to the center of the viewport
- Alternatively, click the **pen tool** (✏) in the toolbar — it always recenters the view

When the frame is completely off-screen, the pen button glows green to let you know you can click it to find the frame again.

---

## 🎨 Tools

The toolbar has six buttons plus zoom controls:

| Button | Action |
|--------|--------|
| ✏ Pen | Drawing tool. Also recenters the view when clicked. |
| ⌫ Eraser | Erase strokes. Click and drag over existing ink to remove it. |
| ✚ Move | Hold and drag anywhere to shift the drawing itself (left/right/up/down juystick). |
| ↶ Undo | Undo the last stroke or clear (per layer). |
| ↷ Redo | Re-apply a stroke you undid. |
| ✕ Clear | Wipe the current layer — all strokes, inside and outside the frame. |

The `+`/`−` buttons next to them zoom the camera; the label between them shows the current zoom.

---

## 🧱 Layers

Each scene can hold any number of layers — like drawing on stacked transparent sheets. Layers share the same frame window, so a layer never gets its own size or position.

- The **layer rail** appears on the right side of the screen when you need it.
- [**Add layer above**] (top of the rail) creates a new, empty layer above everything already in the scene and switches to it.
- The **bottom** of the rail adds a new layer below everything in the scene.
- Each circle in the rail is one layer and shows a live thumbnail of that layer's lines. Click one to make it the active layer (bigger, white ring). Non-active layers are dimmed.
- **Erasing is layer-safe**: an eraser stroke only ever removes ink from the active layer — it can't eat into a different layer's lines.
- **Undo/Redo is per-layer**: history stays with each layer, so an action taken on one layer cannot be undone from an ongoing draw on a different layer.

---

## 🎞️ Scenes — the storyboard filmstrip

A **scene** is one shot of your film. Each scene owns its own drawing window (frame position, size, format) and its own camera (zoom, pan), plus its own set of layers.

- The **filmstrip** appears at the bottom of the screen.
- **+ / ➕** on the strip adds a new scene after the current one; the strip's left edge adds a scene before the first one, so the storyboard can grow backward as well as forward.
- Each strip card shows a thumbnail of the scene, and every scene is named per its position in the strip (shot 1, 2, …).
- Click a card to switch scenes. Switching restores exactly that shot's own framing — resizing, reformatting or zooming one panel can never bleed into another.
- A newly added scene starts as an empty layer with the same aspect ratio as the current scene, centered at default zoom.

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
- **2.00:1** — Flat cinema
- **1.85:1** — Standard widescreen
- **16:9** — HD / digital
- **1:1** — Square
- **4:3** — Classic / SD
- **9:16** — Vertical / mobile

The format change is anchored at the frame's center and uses a rubber-band easing animation. The label fades out once the frame settles.

---

## ↩️ Undo & Redo

- **Undo** (↶) undoes the previous stroke or clear, one action at a time.
- **Redo** (↷) reapplies the last action you undid.
- Buttons are disabled when there is nothing left to undo or redo.
- History is tracked **per layer per scene**: an action taken on one layer can't be undone while you're on a different layer.

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

- **No export / save** — saving your work to a file is not implemented yet
- **No persistence** — all data lives in memory; refreshing the page loses the project
- **No text tool** — annotations must be drawn by hand
- **Layers share the frame** — a layer doesn't get its own window or size; the scene owns the one frame
- **Single undo history running per layer** — a clear permanently wipes that layer (undo of a clear, then a new stroke, continues from there)

---

*This guide covers the current SagaCanvas build. The app is in active development.*