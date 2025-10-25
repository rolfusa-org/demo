# ROLF Demo

A simplified demo version of ROLF with focused QR code functionality.

## Features

- **My QR** 🔳: Generate QR codes from any text or URL
  - Enter text or URL
  - Generate QR code instantly
  - Visual display of generated QR code
  
- **Scan** 📷: Scan QR codes using your device camera
  - Auto-starts camera (back camera on mobile)
  - Real-time QR code scanning
  - Clickable URLs
  - Copy scan results to clipboard

## Structure

This demo version has been simplified from ROLF-docs with the following changes:

1. Removed the status bar (time, signal, wifi, battery indicators)
2. Simplified navigation bar - removed search, kept notification bell
3. Banner displays placeholder content
4. Only 2 apps available: My QR and Scan
5. Bottom navigation has 4 inactive icons: Home, Events, Workflow, Profile
6. Apps open in the grid area with back button navigation

## QR Code Implementation

The QR functionality is implemented using libraries from [rolfusa-org](https://github.com/rolfusa-org):

- **QR Generator**: Uses `qrcode.min.js` for generating QR codes
- **QR Scanner**: Uses `html5-qrcode.min.js` for camera-based scanning

Each app loads independently without cross-navigation between them, making them truly separate mini-apps within the demo.

## How to Run

This is a static web application:

1. Open `index.html` in any modern web browser
2. Or use a simple HTTP server:
   ```bash
   python3 -m http.server 8000
   ```
   Then visit http://localhost:8008

**Note**: Camera access is required for the Scan feature and works best on HTTPS or localhost.

## Files

- `index.html` - Main page with simplified navigation and 2-app grid
- `styles.css` - Styling with modifications for simplified layout
- `script.js` - Interactive functionality for loading app content with QR generation/scanning
- `js/qrcode.min.js` - QR code generation library
- `js/html5-qrcode.min.js` - QR code scanning library
- `README.md` - This file

