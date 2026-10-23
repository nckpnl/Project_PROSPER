# Project PROSPER - Strict TFLite Static Web Application

This package contains a purely static web application for **Project PROSPER** that is **100% dependent on the TensorFlow Lite model file (`model/ourmodel.tflite`)**.

If the `.tflite` model file is missing or invalid, the prediction interface remains strictly disabled and displays an error message.

---

## 📁 Required Directory Layout

```text
project-prosper-tflite/
├── index.html              # Static Dashboard UI with WebAssembly TFLite Runtime
├── README.md               # Setup and deployment guide
└── model/
    └── ourmodel.tflite     # REQUIRED: Your TensorFlow Lite model file
```

---

## 🚀 How to Run Locally

Because browser security policies block loading local binary files (`.tflite`) via direct `file://` double-clicking, you must launch a local HTTP server:

```bash
# Inside the root folder:
python -m http.server 8000
```
Then navigate to `http://localhost:8000`.

---

## 🌐 Deploy Directly to GitHub Pages / Render / Netlify

1. Place your exported `ourmodel.tflite` file into the `model/` folder.
2. Push this repository to **GitHub**.
3. Enable **GitHub Pages** (or link to Render/Netlify Static Site).
4. Your website will execute browser-side TFLite inference via WebAssembly!
