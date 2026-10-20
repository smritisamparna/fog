# fog — An Interactive Webcam Experience

**A gesture-controlled fogged-mirror experience built with HTML, CSS, JavaScript, MediaPipe, and the Web Audio API.**

`fog` turns a webcam feed into a simulated fogged-up mirror. Use hand gestures to draw on the glass, wipe away the fog, and reveal the camera image underneath. Microphone input drives a breath-inspired fogging effect, with a keyboard alternative.

## Features

- **Hand tracking:** Uses MediaPipe Hands to track one hand in real time.
- **Pinch-to-draw:** Pinch your thumb and index finger together to draw through the fog.
- **Fist-to-wipe:** Make a fist and move your hand to clear the fog.
- **Breath-inspired fogging:** Microphone input affects the fog effect; holding `Space` provides a manual alternative.
- **Face-aware effect:** MediaPipe Face Detection estimates a mouth position to guide where fog appears.
- **Adjustable brush:** Change the virtual brush size with the on-screen slider.
- **Screenshot export:** Save the current scene as a PNG.
- **Keyboard shortcuts:** Clear the fog, save a screenshot, manually fog the mirror, or exit.
- **Canvas-based rendering:** Uses gradients, alpha compositing, blur, and masking to create the frosted-glass illusion.

## Built With

| Technology | How it is used |
|---|---|
| HTML5 | Page structure |
| CSS3 | Layout and visual styling |
| JavaScript (ES6+) | Application logic and interaction |
| HTML Canvas API | Fog layer, drawing, wiping, and rendering |
| MediaPipe Hands | Hand landmark tracking |
| MediaPipe Face Detection | Face and mouth-position estimation |
| Web Audio API | Microphone input level analysis |
| MediaDevices API | Webcam and microphone access |

## Run Locally

### Requirements

- A modern browser that supports camera and microphone access
- A webcam and microphone
- Internet access to load MediaPipe libraries and model files from jsDelivr
- Python 3 (or another local HTTP server)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/smritisamparna/fog.git
   cd fog
   ```

2. Start a local server:

   ```bash
   python -m http.server 8000
   ```

3. Open [http://localhost:8000/fog.html](http://localhost:8000/fog.html).
4. Click **Start** and allow camera and microphone access when your browser asks.

> **Important:** Browsers generally require HTTPS or `localhost` for camera and microphone access. Opening the file directly with a `file://` URL may not work.

## Controls

| Action | How to use it |
|---|---|
| Start the experience | Click **Start** |
| Draw on the fog | Pinch thumb and index finger together |
| Stop drawing | Release the pinch |
| Wipe the fog | Make a fist and move your hand |
| Add fog manually | Hold `Space` |
| Clear the fog | Press `C` |
| Save a screenshot | Press `S` or click the camera button |
| Change brush size | Move the brush slider |
| Exit | Press `Esc` |

## Privacy Notes

The application code processes the webcam feed and microphone input in the browser and does not implement uploading recordings to an application server. The browser will ask for camera and microphone permission. The project loads third-party MediaPipe scripts and model assets from jsDelivr, so an internet connection is required.

## Current Limitations

- The project is currently implemented as a single HTML file with embedded CSS and JavaScript.
- Gesture tracking and audio response can vary with lighting, camera quality, background noise, and device performance.
- The MediaPipe dependencies are loaded from a CDN, so the app is not fully offline.
- Browser and device support may vary.

## Possible Future Improvements

- Add a loading indicator while the vision models initialize.
- Improve error handling and recovery when camera or microphone access fails.
- Offer a camera-only mode that does not require microphone permission.
- Add more interaction modes and visual themes.
- Improve mobile responsiveness and performance on lower-end devices.
- Separate the HTML, CSS, and JavaScript into maintainable files and add automated tests.

## Author

**Smriti Samparna**  
GitHub: [@smritisamparna](https://github.com/smritisamparna)

---

*Built as a creative coding project exploring browser-based computer vision and gesture interaction.*
