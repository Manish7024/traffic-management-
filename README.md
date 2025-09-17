# 🚦 Real-Time Vehicle Detection with YOLOv8 and OpenCV

This project demonstrates **real-time detection and counting of specific vehicles (cars and motorbikes)** using [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) and [OpenCV](https://opencv.org/).  
The model runs directly on your webcam feed, draws bounding boxes, and displays live counts on the screen.

---

## ✨ Features
- ✅ Real-time object detection with YOLOv8
- ✅ Tracks **cars** and **motorbikes** only (customizable)
- ✅ Live bounding boxes with confidence scores
- ✅ Vehicle count overlay on video feed
- ✅ Press `q` to quit gracefully

---

## 📂 Project Structure
traffic-management/
│── traffic.py # Main script
│── yolov8s.pt # Pre-trained YOLOv8 model (downloaded automatically if missing)
│── README.md # Project documentation

yaml
---

## ⚙️ Requirements

Make sure you have Python **3.8+** installed.  
You can install dependencies using `pip`.

### 1️⃣ Install Python packages
```powershell
pip install ultralytics opencv-python
If you also want extra OpenCV features:

powershell

pip install opencv-contrib-python
2️⃣ Verify installation
powershell
Copy code
python -c "import cv2; print(cv2.__version__)"
python -c "import ultralytics; print(ultralytics.__version__)"
▶️ Usage
Run the script
In PowerShell or terminal, navigate to the project folder:

powershell
Copy code
cd "C:\Users\manis\Desktop\traffic management"
python traffic.py
A window will open showing your webcam feed.

Bounding boxes appear around cars and motorbikes.

The top-left corner shows the count of detected vehicles.

Press q to close the program.

🖼️ Example Output
(Example frame with bounding boxes and counts — add your own screenshot here)

🛠️ Code Overview
Main components:
YOLO('yolov8s.pt') → loads YOLOv8 small model

cv2.VideoCapture(0) → opens webcam feed

Detection loop:

Run YOLO on each frame

Filter detections for car and motorbike

Draw bounding boxes + labels

Update count overlay

🧩 Customization
Change detected vehicles
Edit this line in traffic.py:

python
Copy code
specific_vehicles = ['car', 'motorbike']
Add or remove YOLO class names (e.g., bus, truck, person).

Confidence threshold
Default: 0.4
Change in this line:

python
Copy code
if box.conf[0] > 0.4:
Camera source
Default: 0 (webcam).
For video file:

python
Copy code
videoCap = cv2.VideoCapture("video.mp4")
🚀 Future Improvements
Add FPS (frames per second) display

Support multiple video streams (traffic CCTV)

Save detections to CSV or database

Integrate traffic light automation system

📜 License
This project is licensed under the MIT License – you’re free to use, modify, and distribute.

🙌 Acknowledgements
Ultralytics YOLOv8

OpenCV

yaml
---

👉 Would you like me to also add a **badges section** (Python version, license, OpenCV, YOLOv8) at the top for a more professional GitHub look?







Ask ChatGPT
