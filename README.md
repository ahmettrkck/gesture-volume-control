 # Hand Gesture Volume Control Application:

 ## Overview

This Python application allows users to control the system volume using hand gestures. It utilizes OpenCV for camera access, MediaPipe for hand gesture recognition, and PyCAW for adjusting the system volume. The volume is controlled by the distance between the thumb tip and the index finger tip: moving them closer or further apart changes the volume level.

## Requirements

Python 3.x
OpenCV
MediaPipe
PyCAW
comtypes

## Installation

To run this application, you need to install the required Python libraries. You can install these using pip:
pip install opencv-python mediapipe pycaw comtypes


## How It Works

The script captures video frames from the webcam using OpenCV.
Each frame is processed by MediaPipe's Hand solution to detect hand landmarks.
The distance between the thumb tip and index finger tip landmarks is calculated.
This distance is mapped to a volume level using PyCAW, and the system volume is adjusted accordingly.

## Notes

The mapping between hand distance and volume level [50, 150] to [minVol, maxVol]) may need adjustment based on your camera setup and personal preference.
The application is designed for use on Windows due to the usage of PyCAW and comtypes for volume control.
