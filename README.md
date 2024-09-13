# Facial Recognition Attendance System

This project is a **Facial Recognition-based Attendance System** that leverages computer vision techniques to recognize students' faces and mark their attendance. It integrates with Google Firebase for real-time data storage and retrieval. 

## Features
- **Face Detection & Recognition**: Uses `dlib`-based facial recognition through `face_recognition` and `cv2` for real-time detection.
- **Bounding Box**: Utilizes `bbox` and `cvzone` for face detection and drawing bounding boxes around detected faces.
- **Attendance Tracking**: Automatically logs attendance based on facial recognition and stores data in Google Firebase.
- **Real-Time Updates**: Attendance data is updated instantly using Firebase Realtime Database and Firebase Cloud Storage.

## Technologies Used
The project is built using Python and the following libraries:

- **OpenCV (cv2)**: For image and video processing.
- **face_recognition**: For detecting and recognizing faces.
- **cvzone**: Used to simplify drawing bounding boxes around recognized faces.
- **NumPy**: For efficient numerical operations.
- **Firebase Admin SDK**: For connecting with Firebase services (Realtime Database and Cloud Storage).
- **bbox**: To work with bounding boxes in images.
- **dlib**: As part of `face_recognition` for face detection.
- **CMake**: For compiling dependencies like dlib.
  
## File Structure
The project consists of three main Python scripts:

1. **`main.py`**:  
   The core of the project where real-time video capturing and facial recognition take place. It processes the video stream, detects faces, and checks them against the existing database to mark attendance.

2. **`Encodegenerator.py`**:  
   This script is responsible for encoding images of faces, which are stored in a database for recognition. It generates facial encodings that will later be compared during the recognition process.

3. **`AddDataToDatabase.py`**:  
   This script allows you to add new students' data (including facial encodings) into the Firebase database. It interacts with Firebase Admin SDK to upload image encodings and store relevant student information.

## Setup Instructions

### Prerequisites
Ensure you have the following installed on your system:

- Python 3.6+
- **Python Libraries**:
  ```bash
  pip install opencv-python
  pip install face_recognition
  pip install numpy
  pip install cvzone
  pip install firebase-admin
  pip install cmake
  pip install dlib
