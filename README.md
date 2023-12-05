# Drowsiness Detection

## Introduction
This Python script utilizes the dlib library for face detection and facial landmark localization to detect drowsiness in a person. It calculates the average eye closure distance over a few frames and triggers an alarm if the closure distance exceeds a predefined threshold.

## Requirements
- Python 3.x
- OpenCV
- Dlib
- imutils
- Pygame (for sound alerts)

## Installation
Install the required libraries using the following commands:
```bash
pip install opencv-python dlib imutils pygame
```

## Usage
1. Download the shape predictor file "shape_predictor_68_face_landmarks.dat" from [dlib.net](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2) and place it in the same directory as your script.
2. Download an alarm sound file (e.g., "alarm.wav") and place it in the same directory as your script.

3. Run the script:
```bash
python drowsiness_detection.py
```

## Script Explanation
- The script captures video from the default camera (you can modify the `cap = cv2.VideoCapture(0)` line to use a different video source).
- It uses dlib to detect faces and facial landmarks.
- The eye closure distance is calculated based on the distances between specific facial landmarks.
- If the average closure distance exceeds a threshold, an alarm sound is played using Pygame.

## Customization
- You can adjust the `thres` variable to set the eye closure threshold.
- Modify the `sound = mixer.Sound('alarm.wav')` line to use a different sound file.

## Dependencies
- [imutils](https://github.com/jrosebr1/imutils): A collection of convenience functions for OpenCV.
- [dlib](http://dlib.net/): A toolkit for machine learning and computer vision.
- [OpenCV](https://opencv.org/): An open-source computer vision and machine learning software library.
- [Pygame](https://www.pygame.org/): A set of Python modules designed for writing video games.

## Note
Ensure that you have the necessary permissions to access the camera, and the required audio output for the alarm sound.

Feel free to reach out for any questions or improvements!
