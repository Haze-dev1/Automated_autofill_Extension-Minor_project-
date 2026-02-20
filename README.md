# Form Fill Mini

A small browser extension (Chrome) for quickly filling forms and testing form-related scripts. Includes a popup UI, content/background scripts, and an example test form.

## Features
- Lightweight popup for quick form actions
- Content and background scripts for page integration
- Example form for manual testing at `examples/test-form.html`

## Installation (development / local)
1. Open your browser's extensions page:
   - Chrome: `chrome://extensions` (enable Developer mode)
   - Firefox: `about:debugging#/runtime/this-firefox`
2. Click "Load unpacked" (Chrome) or "Load Temporary Add-on" (Firefox) and select this project folder (the one containing `manifest.json`).
3. Open `examples/test-form.html` to try the extension on a known test page.

## Usage
- Click the extension icon to open the popup (`popup/popup.html`).
- The extension injects content scripts (`content.js`) into pages as defined in `manifest.json`.
- Background logic runs from `background.js` where event listeners and message routing can be placed.

## Project Structure
- `manifest.json` — extension manifest and permissions
- `background.js` — background/service worker logic
- `content.js` — scripts injected into web pages
- `popup/` — popup UI (`popup.html`, `popup.js`, `popup.css`) and `window.html`
- `scripts/resumeUploader.js` — example script for handling/resuming uploads
- `examples/test-form.html` — local HTML page to test form-filling behavior
- `icons/` — extension icons

## Development
- Edit files directly and reload the extension from the extensions page to see changes.
- There is no build step required unless you add one; keep source files in this folder for Load Unpacked testing.

