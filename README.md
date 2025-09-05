# License_Plate_Detection
🚗 Smart Vehicle Detection & License Plate Recognition System 🔍📸

A real-time surveillance system developed using YOLOv8 object detection and EasyOCR for automatic vehicle and number plate recognition. Designed for smart city enforcement and traffic monitoring, the system detects vehicles and extracts license details from live video feeds with 92% accuracy.

🔑 Key Features

🧠 YOLOv8 + EasyOCR pipeline for object and text detection

🖥 Custom Tkinter-based annotation GUI, cutting labeling time by 60%

📊 Confidence thresholding + error handling for robustness

🧪 Validated across diverse traffic datasets and lighting conditions


🛠 Tools & Techniques

Python, OpenCV, YOLOv8, EasyOCR, Tkinter

Multi-stage inference → Detection → Cropping → OCR

Edge deployment optimization for smart traffic systems


📈 Applications & Impact

🚦 Traffic surveillance, toll automation, parking analytics

📉 60% annotation workload reduction with GUI automation

🎯 Achieved 92% real-time accuracy



---

⚙️ Installation

1. Clone the repository

git clone https://github.com/Hindhuja07/License_Plate_Detection.git
cd Smart-Vehicle-Detection


2. Create & activate virtual environment (recommended)

python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows


3. Install dependencies

pip install -r requirements.txt


4. Download YOLOv8 weights

Download from Ultralytics YOLOv8

Place the .pt file inside the weights/ directory (e.g., yolov8n.pt or custom trained weights).





---

▶️ Usage

1. Run Detection on Video

python detect.py --source sample_videos/traffic.mp4 --weights weights/yolov8n.pt

2. Live CCTV Feed

python detect.py --source 0 --weights weights/yolov8n.pt

(Replace 0 with camera index or RTSP URL for IP cameras)

3. Automatic License Plate Recognition (OCR)

python recognize.py --input runs/detect/exp/frame.jpg

4. Annotation Tool (GUI for labeling)

python annotation_tool.py

Use to quickly draw bounding boxes & auto-save labels.

Reduces manual labeling time by ~60%.



---

📂 Project Structure

Smart-Vehicle-Detection/
│── data/                  # Training datasets
│── weights/               # YOLOv8 model weights
│── sample_videos/         # Test traffic videos
│── detect.py              # Vehicle detection script
│── recognize.py           # OCR-based license plate recognition
│── annotation_tool.py     # Tkinter GUI for labeling
│── requirements.txt       # Python dependencies
│── README.md              # Project documentation


---

📖 Example Output

✅ Detects vehicles in real-time from CCTV footage

✅ Extracts license plate text with EasyOCR

✅ Saves annotated frames + OCR results in runs/
