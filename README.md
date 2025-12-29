# Violence Detection Using Deep Learning (YOLOv8 & DenseNet121)

## 📌 Project Overview
Violence detection is a critical computer vision task with applications in public safety, surveillance systems, and automated monitoring. This project focuses on detecting **violent and non-violent activities from images** using deep learning techniques.

We experiment with **two different modeling approaches**:
- **YOLOv8** → Object detection–based violence localization
- **DenseNet121** → Image classification–based violence recognition

The dataset used in this project is sourced from **Roboflow**, containing labeled images categorized as *Violence* and *Non-Violence*.

---

## 🧠 Motivation
Manual monitoring of surveillance footage is inefficient and error-prone. Automated violence detection systems can:
- Assist security personnel
- Enable real-time alerts
- Improve public safety
- Reduce human workload

This project aims to compare **detection-based** and **classification-based** approaches for violence detection.

---

## 📂 Dataset Description
- **Dataset Name**: Violence Detection Dataset  
- **Source**: Roboflow Universe  
- **Link**: https://universe.roboflow.com/sihtest/violence-detection-ufkio  
- **Type**: Image Dataset  
- **Classes**:
  - `Violence`
  - `Non-Violence`
- **Annotations**:
  - Bounding box annotations (used for YOLOv8)
  - Image-level labels (used for DenseNet121)

---

## 🏗️ Methodology
This project follows two parallel deep learning approaches to detect violence from images:
- **Object detection–based approach** using YOLOv8
- **Image classification–based approach** using DenseNet121

Both models are trained and evaluated on the same dataset to ensure a fair comparison.

---

## 🔍 Model 1: YOLOv8 (Object Detection)
YOLOv8 is employed to detect violent regions within an image using bounding box annotations.

### Key Characteristics
- Single-stage object detector  
- Real-time inference capability  
- Predicts bounding boxes with class confidence scores  
- Suitable for surveillance and security applications  

### Workflow
1. Input image preprocessing  
2. Feature extraction using YOLOv8 backbone  
3. Feature aggregation via neck layers  
4. Bounding box and class prediction  

---

## 🧠 Model 2: DenseNet121 (Image Classification)
DenseNet121 is used to classify the entire image as **Violence** or **Non-Violence**.

### Key Characteristics
- Deep convolutional neural network  
- Dense connectivity between layers  
- Efficient feature reuse  
- Reduced vanishing gradient problem  

### Workflow
1. Input image preprocessing  
2. Feature extraction using DenseNet121  
3. Global average pooling  
4. Binary classification output  

---

## ⚙️ Training Strategy

### YOLOv8
- Trained using bounding box annotations  
- Loss components include:
  - Classification loss  
  - Bounding box regression loss  
- Trained for multiple epochs until convergence  

### DenseNet121
- Transfer learning with ImageNet-pretrained weights  
- Final classification layer modified for binary output  
- Optimizer: Adam  
- Loss Function: Binary Cross-Entropy  

---

## 📊 Evaluation Metrics
The performance of both models is evaluated using standard metrics:
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- Confusion Matrix (DenseNet121)  
- Detection confidence scores (YOLOv8)  

---

## 📊 Results

Both **YOLOv8** and **DenseNet121** were evaluated on the test dataset to analyze their effectiveness in detecting violent and non-violent activities.

- YOLOv8 successfully detected and localized violent regions using bounding box predictions.
- DenseNet121 demonstrated reliable performance for image-level violence classification.
- Detection-based approaches provide better interpretability for surveillance applications.
- Classification-based approaches are computationally efficient and easier to deploy.

---

## 🧠 Comparative Analysis

A comparison of the two models highlights their strengths and limitations.

### 🔍 YOLOv8
- Performs object detection with spatial localization
- Suitable for real-time surveillance systems
- Provides bounding box confidence scores
- Requires higher computational resources

### 🧠 DenseNet121
- Performs binary image classification
- Faster inference on low-resource systems
- Simpler training and deployment pipeline
- Does not provide region-level localization

---

## 🔎 Key Observations

- Object detection models are more effective when spatial understanding is required.
- Image classification models are sufficient when only a binary decision is needed.
- Dataset quality and annotation accuracy significantly impact model performance.
- Transfer learning improves convergence and generalization.

---

## 🔮 Future Work

- Extend the system to video-based violence detection.
- Integrate temporal modeling techniques such as LSTM or 3D CNN.
- Improve robustness using larger and more diverse datasets.
- Deploy the system in real-time surveillance environments.

---

## 🛠️ Technologies Used

- Python
- PyTorch
- TensorFlow / Keras
- Ultralytics YOLOv8
- OpenCV
- Roboflow
- NumPy
- Matplotlib

---

## 👤 Author

**Yash Kumbhawat**  
Department of Information Technology,
NITK

---

## 📜 License

This project is intended for academic and research purposes.  
You are free to use, modify, and distribute this project with proper attribution.


