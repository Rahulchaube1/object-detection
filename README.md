# object-detection
# Real-Time Webcam Object Detection in HTML

## Description

This project is a simple, self-contained HTML file that uses your webcam to perform real-time object detection directly in your browser. It leverages TensorFlow.js and the pre-trained COCO-SSD model to identify and draw bounding boxes around common objects (including people) visible through the camera.

## Features

* **Real-Time Detection:** Identifies objects in the live webcam feed.
* **Browser-Based:** Runs entirely in your web browser; no server-side processing is needed after the initial model load.
* **Multiple Object Recognition:** Uses the COCO-SSD model, which can detect 90 different classes of common objects (e.g., person, car, bottle, chair, laptop, cell phone).
* **Bounding Boxes & Labels:** Draws rectangles around detected objects and labels them with the object class and confidence score.
* **Single File:** All necessary HTML, CSS, and JavaScript code is contained within a single `.html` file for ease of use.

## Technology Used

* **HTML5:** Structure and content markup.
* **CSS3:** Styling for layout and appearance.
* **JavaScript (ES6+):** Core logic for webcam access, model interaction, and drawing on canvas.
* **TensorFlow.js (`@tensorflow/tfjs`):** Core machine learning library for JavaScript.
* **TensorFlow.js Models (`@tensorflow-models/coco-ssd`):** Pre-trained COCO-SSD model for object detection.
* **WebRTC API (`getUserMedia`):** Standard browser API to access the webcam feed.
* **HTML Canvas API:** Used to draw the bounding boxes and labels over the video feed.

## How to Run

1.  **Save the Code:** Save the complete HTML code provided previously into a file named `object_detection.html` (or any other name ending in `.html`).
2.  **Open in Browser:** Open the saved `.html` file using a modern web browser (like Google Chrome, Mozilla Firefox, Microsoft Edge, Safari). Simply double-clicking the file should work, or use your browser's "File > Open" menu.
3.  **Grant Permissions:** Your browser will prompt you for permission to access your webcam. You **must click "Allow"** for the application to function.

## Prerequisites

* A modern web browser that supports WebRTC (`getUserMedia`) and HTML Canvas.
* A functional webcam connected to or built into your computer.
* An internet connection (required initially to download the TensorFlow.js library and the COCO-SSD model from the CDN). The model may be cached by your browser for subsequent uses.

## Usage

* Once the page loads and you grant camera permission, the model will initialize (you'll see a loading message).
* Your webcam feed should appear in the video element.
* The application will automatically start detecting objects.
* Detected objects will have a cyan bounding box drawn around them, along with a label showing the object's name and the detection confidence percentage (e.g., "person (95%)").

## Troubleshooting

* **Camera Not Opening:**
    * Ensure you clicked "Allow" when prompted for camera permission.
    * Check browser site settings (click the icon near the address bar) to make sure the camera isn't blocked for the page.
    * Make sure no other application (Zoom, Teams, Camera app, etc.) is currently using the camera. Close other apps and reload the page.
    * Verify your camera works in other applications.
    * Check OS camera permissions (Windows Settings or macOS System Settings) allow your browser access.
    * Try a different browser.
* **Errors:** Check the browser's Developer Console (usually opened by pressing F12, then clicking the "Console" tab) for specific error messages.
* **Slow Performance:** Object detection can be resource-intensive. Performance depends on your computer's CPU/GPU. Closing other demanding applications might help.

## Limitations

* **Performance:** Detection speed depends heavily on the user's hardware. Lower-end devices may experience lag.
* **Accuracy:** The COCO-SSD model is good but not perfect. Accuracy depends on lighting, object distance, angle, and visibility. It may misclassify objects or fail to detect them sometimes.
* **Object Classes:** The model can only detect the 90 object classes it was trained on. It won't recognize objects outside this set.

---

*Self-contained object detection demo using TensorFlow.js.*
