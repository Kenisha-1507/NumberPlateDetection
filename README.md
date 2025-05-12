
This Python-based project performs real-time license plate detection and recognition from videos and images using OpenCV and EasyOCR. The program is optimized for Google Colab, supporting file uploads since direct webcam access isn't available. It identifies license plate regions using contour detection and extracts text using optical character recognition (OCR) with EasyOCR.

The output is an annotated video or image showing the recognized license plate number overlaid on the frame, along with a cropped view of the plate region if available.

Workflow Overview

1. Initialization
Required libraries like cv2, numpy, easyocr, imutils, and re are imported.

An EasyOCR reader is initialized (easyocr.Reader) with English as the recognition language.

2. License Plate Detection
detect_plate(image):

Converts the image to grayscale.

Applies a bilateral filter to reduce noise.

Uses Canny edge detection to identify contours.

Searches for rectangular contours (typically 4 corners) to find license plate candidates.

Returns the bounding polygon (location) of the detected plate.

3. Text Recognition
recognize_plate_text(image, location):

Uses the plate location to crop the license plate region from the image.

Applies EasyOCR to extract the text.

Cleans the result by removing unwanted characters.

Returns the recognized text and the cropped license plate region.

4. Image Processing
process_image(image):

Calls the detection and recognition functions.

Draws bounding boxes and overlays recognized text.

Returns the final annotated image and cropped plate region.

5. Video Processing
process_video():

Supports video or image uploads in Colab (.mp4, .avi, .jpg, .png).

For videos:

Processes every 5th frame for efficiency.

Detects and annotates license plates.

Writes frames to a new output video file.

Displays progress with FPS and latest plate text.

Converts the result to .mp4 using ffmpeg for compatibility and downloads the file.

For images:

Processes the image.

Displays the annotated image and cropped license plate.

Allows downloading of the processed image.

6. Execution
main():

Starts the app, specifically tailored for Google Colab use.

Prompts users to upload a video or image and runs detection on it.

