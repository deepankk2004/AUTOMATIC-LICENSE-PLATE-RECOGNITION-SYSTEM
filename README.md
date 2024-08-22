
---

# Automatic License Plate Recognition System (ALPR)

## Description
The Automatic License Plate Recognition (ALPR) system is a computer vision project designed to detect and recognize vehicle license plates from images. The system uses various image processing techniques, including grayscale conversion, edge detection, and contour detection, to isolate and extract the license plate from the image. Optical Character Recognition (OCR) is then applied to read and interpret the text on the plate.

## Getting Started

### Prerequisites
Before running the ALPR system, ensure you have the following libraries installed:
- OpenCV
- EasyOCR
- Imutils
- Matplotlib
- NumPy

### Installation
To install the required dependencies, you can use the following commands:

```bash
!pip install easyocr
!pip install imutils
!pip install opencv-python-headless==4.8.1.78
```

### Workflow

1. **Image Loading and Grayscale Conversion**:
   - The system begins by loading the input image and converting it from a colored image to a grayscale format. This step simplifies the image, making it easier to process.

2. **Noise Reduction and Edge Detection**:
      - A bilateral filter is applied to reduce noise while preserving edges. Following this, the Canny edge detection algorithm is used to highlight the edges in the image, which helps in identifying the contours of the license plate.

3. **Contour Detection and License Plate Localization**:
         - The system detects contours in the edged image and approximates them to identify the rectangular region that likely contains the license plate. Once identified, a mask is applied to isolate this region.

4. **License Plate Extraction**:
            - The isolated region is then extracted from the original grayscale image. This image of the license plate is processed further for text recognition.

5. **Text Recognition using EasyOCR**:
               - The EasyOCR library is used to read the text from the extracted license plate image. The recognized text is then displayed on the original image with a bounding box around the license plate.

    ### Example
    Here's a brief overview of how the process works:

    - **Input Image**: A vehicle image with a visible license plate.
    - **Grayscale Conversion**: The image is converted to grayscale.
    - **Edge Detection**: Edges are detected to highlight the license plate.
    - **Contour Detection**: The contours are analyzed to locate the license plate.
    - **License Plate Extraction**: The license plate is isolated from the image.
    - **OCR**: Text on the license plate is recognized and displayed on the image.

    ### Help
    If you encounter any issues, ensure the following:
    - The input image is clear and the license plate is visible.
    - The required libraries are installed and correctly configured.
    - The OCR engine (EasyOCR) supports the language used on the license plates.

    For additional help, refer to the documentation of the libraries used in this project or consult relevant community forums.

     ## Author
    - **Deepank Yadav** 
    yadavdeepank6@gmail.com

    ---

              