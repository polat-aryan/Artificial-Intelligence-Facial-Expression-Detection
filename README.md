# 🤖 Artificial Intelligence Facial Expression Detection  
A real-time facial expression recognition project using MediaPipe Face Landmarker and an SVM classifier.

This project extracts 478 facial landmark points using **MediaPipe Face Landmarker v2**, stores them as a dataset, trains an SVM model, and performs real-time facial expression prediction through the webcam.

The main goal was to explore how artificial intelligence can interpret human facial expressions — and collecting the dataset by making different expressions was especially fun 😄

---

## 📌 Project Overview

The project consists of three main components:

### 1️⃣ Facial Landmark Collection (Dataset Creation)
`yuz_algila.py`  
Captures real-time landmarks via webcam and stores each sample in `veriseti.csv` as:


### 2️⃣ Training the SVM Model
`egitim.py`  
- Reads the dataset  
- Builds an SVM + StandardScaler pipeline  
- Trains the model  
- Evaluates accuracy  
- Saves the model as `model.pkl`

### 3️⃣ Real-Time Facial Expression Prediction
`yuz_algila_test.py`  
Loads the trained model and predicts facial expressions live via webcam.

---

## 🔧 Technologies Used

- Python 3.11  
- MediaPipe Face Landmarker v2  
- OpenCV  
- NumPy  
- Matplotlib  
- Scikit-learn  
- SVM Classifier  
- StandardScaler + Pipeline  

---

## 📂 Project Structure

| File | Description |
|------|-------------|
| `yuz_algila.py` | Captures facial landmarks & creates dataset |
| `egitim.py` | Trains the SVM model |
| `yuz_algila_test.py` | Real-time facial expression prediction |
| `veriseti.csv` | Dataset file |
| `model.pkl` | Trained SVM model |
| `face_landmarker_v2_with_blendshapes.task` | MediaPipe model file |

---

## 🤖 How It Works

### 🔹 MediaPipe Facial Mesh (478 points)
For each detected face, MediaPipe returns 478 landmark points.  
Only **x** and **y** coordinates are used — a total of **956 features** per sample.

### 🔹 Labeling
Each row in the dataset ends with an expression label:


### 🔹 Model Training
The SVM classifier learns patterns from the facial landmark distribution and predicts expressions based on these features.

---

## 🚀 Installation & Setup

### 1. Download the Project
Download the repository as a ZIP file.

### 2. Extract the ZIP into this folder:


> ⚠️ IMPORTANT  
> Extract **directly** into your **Documents** folder.  
> Placing the project elsewhere may cause file path issues and prevent proper execution.

### 3. Recommended Editor  
Visual Studio Code

---

## 🐍 Python Version Requirement

This project **requires Python 3.11**.

> Reason:  
> The libraries used officially support **up to Python 3.11**.  
> Newer Python versions may cause compatibility issues.

---

## 📦 Install Dependencies

After installing Python 3.11, run:

```bash
pip install opencv-python mediapipe matplotlib numpy scikit-learn
▶️ Running the Project
Collect facial landmark data:
python yuz_algila.py

Train the model:
python egitim.py

Run real-time facial expression detection:
python yuz_algila_test.py


To quit:

Q

🎉 Conclusion

This project demonstrates how facial expressions can be recognized in real time using a combination of MediaPipe geometry and classical machine learning.
It’s a fun and hands-on way to explore computer vision and facial expression recognition.

