# Car Number Plate Detection and Recognition

This project focuses on **automatic license plate detection and recognition** using **YOLOv8** for object detection and **EasyOCR** for text extraction. By leveraging **Roboflow’s License Plate Detection Dataset**, the model accurately identifies number plates in images and extracts alphanumeric characters from them.  

## Overview

This project focuses on detecting and recognizing car number plates from images and video streams using YOLOv8 for object detection and EasyOCR for text recognition. It is implemented in Google Colab and uses the Roboflow License Plate Detection Dataset.

## Installation & Setup

Since this project is designed to run on Google Colab, there is no separate requirements file. To set up:

* Open Google Colab.

* Install dependencies:

      !pip install ultralytics easyocr opencv-python

* Download the dataset from Roboflow and load it into Colab.

* Run the provided code cells step by step.

## Features

* Detects car number plates in images and video streams.

* Recognizes and extracts text from detected number plates.

* Uses YOLOv8 for object detection and EasyOCR for Optical Character Recognition (OCR).

* Displays bounding boxes around detected plates and recognized text.

## Dataset

The project uses Roboflow's License Plate Detection Dataset for training YOLOv8. The dataset consists of images labeled with bounding boxes around license plates.

## Code Explanation

The project follows these steps:

* Load YOLOv8 Model: The pre-trained YOLOv8 model is used for detecting number plates.

* Preprocess Input: Images are resized and normalized before passing them to the model.

* Detect Number Plates: YOLOv8 predicts bounding boxes around number plates.

* Extract Region of Interest (ROI): The detected plates are cropped from the original image.

* Recognize Text with EasyOCR: The cropped number plate images are passed to EasyOCR to extract text.

* Display Results: The detected number plate and recognized text are visualized.

## Library Usage & Functions

**(1) ultralytics (YOLOv8)**

* YOLOv8.detect() → Detects objects in images.

**(2) OpenCV (cv2)**

* cv2.imread() → Reads an image.

* cv2.rectangle() → Draws bounding boxes.

* cv2.putText() → Overlays detected text on images.

**(3) EasyOCR**

* Reader.readtext() → Extracts text from images.

## Usage

* Upload Image/Video: Run the code in Colab and upload an image or video containing a car number plate.

* Run Detection: Execute the provided script to detect and recognize the plate.

* View Results: The output image will show a bounding box around the detected plate with the recognized text displayed.

## Results

**Presicion**: 95.13%

**Recall**: 85.88%

## Example Output

Image:📷 (Car image with a visible Bounding Box on number plate)

![image](https://github.com/user-attachments/assets/26c6257f-dfc7-4cb3-9c94-fd7cd6060805)

Detected Output:📷 (Image with a Text on bounding box around the number plate)

![image](https://github.com/user-attachments/assets/cada5d9e-adb8-402b-ac30-512fd6e4a943)

## Future Enhancements

* Improve OCR accuracy using advanced preprocessing techniques.

* Extend support for video streams with real-time detection.

* Train YOLOv8 on a custom dataset for better region-specific performance.

## Conclusion  

The **Car Number Plate Detection and Recognition** project successfully implements **YOLOv8** for object detection and **EasyOCR** for text recognition, enabling accurate extraction of vehicle license plate information from images. Using **Roboflow’s License Plate Detection Dataset**, the model efficiently detects number plates and recognizes text from them.  
