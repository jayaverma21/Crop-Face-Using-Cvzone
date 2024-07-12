# Crop-Face-Using-Cvzone
This project demonstrates an application that detects human faces from a webcam feed, crops the detected faces, and saves the cropped face images to a folder using OpenCV.

## Requirements

- Python 3.x
- OpenCV

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/yourusername/face-extraction.git
    cd face-extraction
    ```

2. Install the required package:

    ```bash
    pip install opencv-python
    ```

3. Make sure you have the Haar Cascade classifier file (`myhaarcascade_frontalface_default.xml`) in the project directory.

## Usage

1. Create a folder named `img` in the project directory to save the cropped face images.

    ```bash
    mkdir img
    ```

2. Run the script:

    ```bash
    python face_extraction.py
    ```

3. The webcam feed will open in a new window, and the detected faces will be cropped and saved as images in the `img` folder. The script will save up to 100 face images.

4. Press the 'Enter' key to exit the application.

## Code Overview

The main script performs the following steps:

1. Initializes the Haar cascade classifier for face detection.
2. Defines a function `face_extract(pic)` that:
    - Converts the input image to grayscale.
    - Detects faces in the grayscale image.
    - Crops and returns the detected face.
3. Opens the webcam feed and continuously reads frames.
4. For each frame, calls the `face_extract(pic)` function to detect and crop the face.
5. Resizes the cropped face to 200x200 pixels and saves it to the `img` folder with a sequential filename.
6. Displays the cropped face with a count of the saved images.
7. Exits the loop when the 'Enter' key is pressed or 100 face images are saved.


