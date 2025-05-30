# 🚧 Road Damage Classification with MobileNetV2

Automatically detecting road damage using image classification.

---

## 📌 Introduction

Road infrastructure plays a crucial role in transportation and economic development. However, road damage such as potholes and cracks can pose serious safety risks and increase maintenance costs if not addressed promptly.

This project leverages the power of deep learning with model like MobileNetV2, a lightweight  neural network to classify road surface images into distinct types of damage. It's aim is to build a foundation for real-time, scalable road monitoring systems.

---

## ❗ Problem Statement & Project Purpose

### The Problem:
Manual inspection of road damage is time-consuming, expensive, and prone to human error. Many regions lack sufficient resources to constantly monitor road conditions, leading to delays in maintenance and increasing risks to drivers.

### The Purpose:
- Building a deep learning model to detect and classify road damage types (such as potholes, cracks, and severe damage) based on images.
- Applying transfer learning techniques with MobileNetV2 to improve classification efficiency and accuracy.
- If creating an image classification model using the MobileNetV2 model is good for classifying road damage.

---

## 🔍 Methodology

### 1. **Dataset Preparation**
- Source: [Road Damage Dataset]([https://www.kaggle.com/](https://www.kaggle.com/datasets/alvarobasily/road-damage))
- Classes:
  - `Pothole`
  - `Longitudinal Crack`
  - `Lateral Crack`
  - `Alligator Crack`
- Images were preprocessed and organized into folders per class.

### 2. **Model Preperation**
- Dataset was split into `train` (80%) and `test` (20%) using `splitfolders`.
- Ensured balance across categories for unbiased model learning.

### 3. **Model Processing**
- Daaset:
  - Images stored in `/content/clustered_images`
  - Organized by class folders
  - Split: `80% training, 20% validation`
- Image Processing:
  - Resized to 224x224
  - Rescaled pixel values `(1./255)`
  - Batch size: 32
- Model Architecture & Training:
  - Loss: `categorical_crossentropy`
  - Optimizer: `Adam`
  - Metric: `accuracy`
  - Trained for 5 epochs
- Model Output:
  - `road_damage_classifier.keras`

### 4. **Model Evaluation**
- Loss Function: Categorical Crossentropy
- Metrics: `Accuracy, Confusion Matrix, Precision/Recall`

---

## ✅ Results

| Class       | Precision | Recall | F1-Score | Support |
| ----------- | --------- | ------ | -------- | ------- |
| `cluster_0` | 0.30      | 0.39   | 0.34     | 59      |
| `cluster_1` | 0.16      | 0.21   | 0.18     | 29      |
| `cluster_2` | 0.28      | 0.18   | 0.22     | 56      |
| `cluster_3` | 0.20      | 0.15   | 0.17     | 26      |



