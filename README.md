# Windows 11 Dark Mode Web OS

A lightweight, single-file web application that simulates a **Windows 11 Dark Mode Desktop Environment** using pure HTML, CSS, and Vanilla JavaScript. It features an interactive desktop, dynamic window management, custom folder structures, multi-tab web browsing, desktop utilities, and a split-screen media player integrated with an AI assistant.

---

## Key Features

- **Windows 11 Mica & Dark UI**: Styled using CSS design tokens for backdrop blur (`mica`), custom wallpaper radial gradients, fluid window shadows, start menu, quick settings, taskbar, and live system clock.
- **Dynamic Window & Taskbar Manager**: 
  - Open, minimize, maximize, bring-to-front (z-index focus), drag-to-move, and close app windows.
  - Taskbar previews and interactive window tooltips.
- **Microsoft Edge Clone**: Built-in tabbed browser supporting multi-tab navigation, custom quick-access links, and external URL rendering via iframe.
- **Desktop Applications**:
  - **Calculator**: Functional arithmetic calculator with interactive keypad.
  - **Calendar**: Interactive monthly grid displaying the current month and date highlights.
  - **Dynamic Media Folders**: Load custom video libraries into simulated desktop folders.
- **Split-Screen Cinema View**: Double-clicking a video inside a folder opens a full-screen dual pane:
  - Left pane: Interactive HTML5 video player.
  - Right pane: Embedded AI Assistant panel.
- **Quick Settings & System Controls**: Dynamic wallpaper switcher, brightness filter control, volume control for media elements, and a system shutdown simulation.

---

## File Structure

This project is fully self-contained in a single file:

```text
index.html       # Complete HTML layout, CSS Windows 11 design tokens, and JS logic
```

---

## Getting Started

### Prerequisites
No build tools, node packages, or local web servers are required. A modern web browser (Google Chrome, Microsoft Edge, Mozilla Firefox, Safari) is all you need.

### Running the Project
1. Open `index.html` directly in your web browser.

---

## Configuration

You can customize the start image, custom video folders, and AI assistant link by editing the configuration section in the `<script>` tag of `index.html`:

```javascript
/* =========================================================
   ✨ CONFIGURATION SECTION ✨
========================================================= */

// BROWSER START PAGE IMAGE URL:
const EDGE_START_IMAGE = "https://your-image-url.com/wallpaper.png";

// AI ASSISTANT SIDEBAR URL FOR SPLIT-VIEW:
const AI_ASSISTANT_URL = "https://your-ai-assistant-url.com/";

// CUSTOM FOLDERS AND VIDEOS:
const USER_FOLDERS = [
    {
        name: "LHC Experiments",
        icon: "🗂️",
        videos: [
            { title: "The LHCb Experiment", src: "The_LHCb_Experiment.mp4" }
        ]
    }
];
```

---

## Tech Stack

- **HTML5**: Semantic elements, structural UI containers, and embedded media controls.
- **CSS3**: Custom properties (tokens), CSS Grid/Flexbox layouts, glassmorphism (`backdrop-filter`), animations, and media constraints.
- **JavaScript (ES6+)**: Vanilla DOM manipulation, window dragging algorithms, tab lifecycle management, and event-driven state updates.
