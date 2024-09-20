# face-regoc
Face Recognition System
This project implements a real-time eye blink detection and alert system using OpenCV, face_recognition, and Google Colab's camera interface. It can help monitor drowsiness by analyzing eye aspect ratio (EAR) and triggering an alert when the EAR falls below a certain threshold for a specified number of consecutive frames.

Features
Eye Aspect Ratio Calculation: Measures the eye aspect ratio using landmarks of the eyes to detect if the eyes are closed.
Drowsiness Alert: Triggers an alert if the eyes are closed for a certain number of frames.
Real-Time Video Capture: Captures video in real-time using a webcam and processes each frame to detect facial landmarks and eye closure.
Custom Thresholds: Adjustable minimum EAR and frame thresholds for fine-tuning the system's sensitivity.
Google Colab Integration: Utilizes Google Colab's ability to capture images from the webcam in a browser-based environment.
Requirements
To run this project, ensure the following libraries are installed:

Python 3.x
OpenCV
NumPy
Scipy
face_recognition
Google Colab Patches (cv2_imshow)
IPython
You can install the dependencies using the following:

bash
Copy code
pip install opencv-python-headless numpy scipy face_recognition google-colab ipython
How It Works
Eye Aspect Ratio (EAR): The EAR is calculated using the Euclidean distance between the vertical eye landmarks divided by the horizontal eye distance. When the eyes are closed, the EAR decreases significantly.

Alert Mechanism: If the EAR is below a predefined threshold (min_aer) for a specific number of consecutive frames (eye_ar_cosec_frames), an alert is triggered (in this case, a text message in the console).

Image Capture in Google Colab: The system uses JavaScript to capture frames via webcam in Google Colab and processes each frame for facial landmarks.

Usage
Clone the Repository:

bash
Copy code
git clone <repo_url>
cd eye-blink-detection
Run the Script: Open the project in Google Colab, and run the Python script in the notebook.

Adjust Parameters:

min_aer: Minimum EAR threshold (default 0.30)
eye_ar_cosec_frames: Number of consecutive frames with EAR below threshold to trigger the alert (default 10)
Stopping the Script: Press q to stop the script.

Example Code
python
Copy code
min_aer = 0.30
eye_ar_cosec_frames = 10
Future Enhancements
Add sound alerts for better real-time feedback.
Improve accuracy with more advanced facial recognition models.
Implement a graphical user interface (GUI) for ease of use.
Contributing

