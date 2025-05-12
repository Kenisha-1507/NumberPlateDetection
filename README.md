Automatic License Plate Detection and Recognition
This project detects and recognizes license plates from images and videos using a combination of YOLO-based contour detection and EasyOCR for optical character recognition. It is optimized for real-time or batch processing, and can be run seamlessly in environments such as Google Colab or locally.

📸 Project Features
📷 Image and video input support
🎯 License plate localization using contour detection (YOLO-free)
🔤 Text recognition from license plates using EasyOCR
⏱️ Real-time video processing with frame skipping for performance
🧾 Outputs annotated media with detected license numbers overlaid
🛠️ Tech Stack
Python 3.x
OpenCV
EasyOCR
NumPy
imutils
Google Colab (optional, for cloud execution)
🧑‍💻 How to Run
✅ Google Colab (Recommended)
Open the notebook in Google Colab.
Upload your image or video when prompted.
The processed output (annotated image/video) will be displayed and made available for download.
🖥️ Local Setup
Ensure Python 3.x is installed.
Install dependencies:
pip install opencv-python easyocr imutils numpy
Run the script:
python main.py
🧾 Requirements
Install all required packages using pip:

pip install opencv-python easyocr imutils numpy
⚡ Optional (for GPU acceleration with EasyOCR):
pip install torch torchvision torchaudio
🖼️ Sample Output
Detected license plates will be highlighted with bounding boxes.
The recognized plate numbers will be overlaid on the images or video frames.
