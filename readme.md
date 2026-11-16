# 3D, Image & Video ASCII Studio v1.0 Stable

A cool and lightweight web tool that turns your 3D models, pictures, and videos into ASCII art right inside your browser. Built with Three.js and vanilla JavaScript.

## What is this?

This is a single-file web app where you can drop any image, video, or 3D model and instantly watch it turn into text-based ASCII art. You can tweak colors, adjust contrast, change character sets, and export your creations easily.

## Key Features

* **Supports Multiple Formats:** Works with `.glb`, `.gltf`, `.png`, `.jpg`, `.jpeg`, `.webp`, `.mp4`, `.webm`, and `.ogv`.
* **Real-Time Editing:** Adjust brightness, contrast, saturation, hue, sharpness, and edge detection on the fly.
* **Custom Character Sets:** Choose from built-in styles (like standard ASCII, blocks, braille, or binary) or type your own custom characters.
* **Color Themes:** Switch between custom colors, Matrix green, Cyberpunk, or retro Amber.
* **Cool Export Options:** Download your art as a `.txt` file, HTML page, PNG screenshot, React component (`.jsx`), or record it as a WebM video.
* **Drag & Drop:** Just drag any file onto the screen to load it instantly.

## What's Inside the Code?

Everything lives in a single `ascii_editor.html` file using ES modules. Here is a quick breakdown of how the main functions work:

* **`init()`**: Sets up the Three.js scene, camera, lights, renderer, and mouse controls.
* **`rebuildAsciiEffect()`**: Recreates the ASCII filter based on your chosen character set, resolution, and settings.
* **`applyColorTheme()`**: Changes the background and text colors to match your selected theme (like Matrix or Cyberpunk).
* **`updateDomFilters()`**: Applies live CSS filters and transforms (zoom, rotation) for smooth adjustments without lagging.
* **`loadModel()` / `loadImage()` / `loadVideo()`**: Handles loading and parsing your uploaded 3D files, images, or videos into the scene.
* **`centerObject()`**: Automatically centers and scales any 3D model so it fits nicely on the screen.
* **`startRecording()` / `stopRecording()`**: Uses browser recording tools to capture live animations and save them as video files.

## How to Run It Locally

Since the app uses ES modules, you will need a local web server to run it properly (otherwise, browser security blocks loading local files).

1. Clone or download the project files.
2. Open your terminal in the project folder and start a quick server:
   * **Python:** `python -m http.server 8000`
   * **Node.js:** `npx serve`
3. Open your browser and go to: `http://localhost:8000/ascii_editor.html`

## License

MIT License. Feel free to use, modify, and share!