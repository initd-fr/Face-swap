# Face-Swap

A **face detection and face swap** project using OpenCV and pre-trained Haar cascade classifiers.  
This project was created to explore computer vision basics: detecting faces (and eyes) in images and swapping two faces within a single photo.

---

## 🚀 Overview

The repo contains two main scripts:

- **Face detection** — Detects faces and eyes in an image and draws bounding boxes (green for faces, blue for eyes).
- **Face swap** — Takes an image with exactly two faces, extracts each face region, and swaps them to produce a single output image.

The goal was to practice:

- OpenCV for image loading, grayscale conversion, and display
- Haar cascade classifiers for object detection
- Image cropping, resizing, and in-place replacement

---

## 🧠 Key Features

- **Face detection** — Detects faces and eyes using pre-trained Haar cascades
- **Visual feedback** — Draws rectangles around detected faces (green) and eyes (blue)
- **Face swap** — Swaps two faces in one image (image must contain exactly 2 faces)
- **Pure OpenCV** — No deep learning; uses classic computer vision only
- **Included cascades** — Uses `haarcascade_frontalface_default.xml` and `haarcascade_eye.xml`

---

## 🛠 Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python" />
</p>

- **Python** — Scripting and logic
- **OpenCV (cv2)** — Image I/O, grayscale conversion, cascade detection, drawing, display
- **Haar cascades** — Pre-trained classifiers for face and eye detection

---

## 🗂 Project Structure

```
Face-swap/
├── README.md
├── app.py                          # Face swap: swap two faces in one image
├── face-detection.py               # Face + eye detection with bounding boxes
├── haarcascade_frontalface_default.xml
└── haarcascade_eye.xml
```

- `app.py` — Face swap pipeline (expects an image with exactly 2 faces)
- `face-detection.py` — Face and eye detection with visual overlay
- `haarcascade_*.xml` — OpenCV Haar cascade model files

---

## 📦 Installation

To run the project locally:

1. Clone the repo:
   ```bash
   git clone https://github.com/initd-fr/Face-swap.git
   cd Face-swap
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install opencv-python
   ```

4. Place your image in the project folder and set the filename in the script (e.g. replace `'votreimage.jpg'` with your image path).

5. Run a script:
   ```bash
   python face-detection.py   # Face + eye detection
   # or
   python app.py              # Face swap (image must contain exactly 2 faces)
   ```

---

## 📌 Notes

- **Face swap** (`app.py`) requires an image with **exactly two faces**; otherwise the script exits with a message.
- Input image path is hardcoded as `'votreimage.jpg'` in both scripts — update it to your image path before running.
