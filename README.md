# 🐶🐱 Real-Time Cat vs Dog Classifier with Voice Feedback (TensorFlow + OpenCV)

A real-time computer vision project that classifies live camera footage into **Cat**, **Dog**, or **Uncertain** using a custom-trained CNN model in TensorFlow.  
Includes voice feedback using `pyttsx3`, and supports mobile camera input via **iVCam**.

---

## 🚀 Features

- 🎥 Real-time video classification from webcam or mobile camera (via iVCam)
- 🧠 Custom-trained Convolutional Neural Network (CNN) with TensorFlow
- 🔊 Voice announcements for detected labels using `pyttsx3`
- ❓ Handles uncertain predictions when input is unclear (e.g. human or background)
- 🖼️ Prediction overlay on video stream

---

## 🛠️ Installation

Clone the repository and install the dependencies:

```bash

tensorflow
opencv-python
numpy
pyttsx3

▶️ How to Run
Simply run the script:

bash
Copy
Edit
python main.py
Note: The default webcam is accessed with cv2.VideoCapture(0).
If using iVCam (mobile camera), change the camera index to 1, 2, or as detected by your system.


cap = cv2.VideoCapture(1)  # Use the correct index for iVCam
To detect the correct index, run this snippet:


import cv2
for i in range(5):
    cap = cv2.VideoCapture(i)
    if cap.isOpened():
        print(f"Camera index {i} is available.")
        cap.release()
📱 Using iVCam (Mobile Camera)


Install iVCam on both your PC and mobile device.

Connect your phone and computer to the same Wi-Fi network or use USB.

Launch the iVCam app on your phone.

Use the detected iVCam index in the code.

🗣️ Voice Feedback
The model uses pyttsx3 to announce the prediction result:

"Dog detected" if prediction > 0.75

"Cat detected" if prediction < 0.25

"Uncertain detected" if confidence is in between

Voice is only triggered when the prediction label changes.


🧠 Model Information
The CNN model was trained on 150x150 RGB images for binary classification (Cat vs Dog). It uses several convolutional layers, batch normalization, dropout, and a sigmoid output activation.


📖 License
This project is licensed under the MIT License.
Feel free to use, modify, and share with credit.


🙌 Acknowledgments
TensorFlow for model training and inference

OpenCV for real-time video processing

pyttsx3 for text-to-speech support

iVCam for mobile camera integration


---

Would you like me to save this as a ready-to-upload `README.md` file for your GitHub repo?








