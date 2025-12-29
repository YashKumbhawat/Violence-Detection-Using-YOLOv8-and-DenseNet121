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

## 🏗️ Project Architecture
This project follows two parallel pipelines:

### 1️⃣ YOLOv8-Based Pipeline (Object Detection)
- Uses bounding box annotations
- Detects violent regions in images
- Suitable for real-time surveillance applications

- 
