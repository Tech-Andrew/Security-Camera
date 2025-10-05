# ***🔒 Security Camera Recorder***

A lightweight ***Python OpenCV security camera*** that records video automatically whenever motion (face or body) is detected — and stops recording when things go still.

---

### **🎯 Overview**

This script turns your webcam into a smart ***motion-activated security recorder.***  
When it detects a **face** or **body**, it starts recording and saves the footage as a timestamped `.mp4` file.  
If there’s no movement for a few seconds, it stops recording automatically to save space.

---

### **🧩 Features**

_🎥 Automatic Recording_ — Starts and stops based on face/body detection.  
_📦 Timestamped Files_ — Each clip is saved with the current date and time.  
_⏱️ Smart Delay_ — Keeps recording for a few seconds after detection stops (default: `5s`).  
_🧠 Lightweight_ — No databases or servers — just pure OpenCV.  
_🪟 Live Preview_ — See the camera feed in real-time.  
_🧰 Easy to Customize_ — Change recording duration, cascade types, or add bounding boxes.

---

### **⚙️ Requirements**

- ***Python 3.8+***
- ***OpenCV (cv2)***

Install OpenCV:
```bash
pip install opencv-python
```

---

### **🚀 Run It**

1. Save this script as:
   ```bash
   main.py
   ```
2. Run it with:
   ```bash
   python main.py
   ```
3. The webcam feed opens automatically.  
   - When motion (face/body) is detected → recording starts.  
   - When it stops → video is saved as `DD-MM-YYYY-HH-MM-SS.mp4`.  
   - Press **Q** to exit.

---

### **🧠 How It Works**

- Uses **Haar Cascade Classifiers** to detect faces and bodies in real-time.  
- Begins recording once anything is detected.  
- When the scene is empty, starts a countdown.  
- After a few seconds of no movement, stops recording and saves the file.

---

### **📁 Output Example**

```
main.py
├── 05-10-2025-22-15-04.mp4
├── 05-10-2025-22-20-12.mp4
└── ...
```

---

### **🧑‍💻 Author**

Built with ❤️ by ***Tech-Andrew*** — a simple, effective motion-triggered camera using pure Python + OpenCV.

---

### **📜 Notes**

- Press **Q** anytime to quit safely.  
- To visualize detections, uncomment these lines in the code:
  ```python
  cv2.rectangle(frame, (x, y), (x + width, y + height), (255, 0, 0), 3)
  ```
- You can adjust:
  ```python
  SECONDS_TO_RECORD_AFTER_DETECTION = 5
  ```
  to record longer or shorter clips after motion stops.
