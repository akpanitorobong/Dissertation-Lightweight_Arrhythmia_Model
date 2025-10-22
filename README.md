# Lightweight Deep Learning Model for Multi-Class ECG Arrhythmia Detection

### Author: Itorobong Akpan  
**Supervisor:** David Croft  
**Course:** MSc Data Science and Computational Intelligence, Coventry University  
**Academic Year:** 2025/26  

---

## 🧠 Project Overview
This project presents the design and evaluation of a **lightweight 1D Residual Network (ResNet)** for the **automated classification of ECG arrhythmias** using the **Chapman University ECG dataset**.  
The aim is to develop an efficient deep learning model suitable for **on-device real-time cardiac health monitoring**, especially in **resource-constrained environments** such as wearable devices and mobile health applications.

---

## 🎯 Objectives
1. Review existing literature on ECG analysis and lightweight deep learning models.  
2. Design and develop an efficient 1D ResNet for ECG signal classification.  
3. Train, evaluate, and visualize model performance on the Chapman dataset.  
4. Quantize and export the trained model into a **TensorFlow Lite (.tflite)** format for lightweight deployment.  

---

## ⚙️ System Methodology
The model development follows an **Incremental Development Methodology**, enabling iterative refinement and testing at each stage:

1. **Data Loading:** Import and explore the Chapman ECG dataset.  
2. **Preprocessing:** Denoise, normalize, and segment ECG signals; detect R-peaks.  
3. **Feature Extraction:** Use residual convolutional blocks for hierarchical pattern learning.  
4. **Model Training:** Train the 1D ResNet using class-weighted loss to handle imbalance.  
5. **Evaluation:** Generate confusion matrices, classification reports, and Grad-CAM visualizations.  
6. **Model Optimization:** Quantize and convert to `.tflite` for edge deployment.  

---

## 🧩 Model Architecture
- **Type:** 1D Convolutional Residual Network (ResNet)  
- **Input:** ECG time-series signals (length 500)  
- **Layers:** Stacked residual blocks with batch normalization and ReLU activations  
- **Output:** 4-class softmax classifier (multi-class arrhythmia detection)  
- **Optimizer:** Adam  
- **Loss Function:** Categorical Cross-Entropy  
- **Framework:** TensorFlow / Keras  

---

## 📊 Results Summary
| Metric | Original Model | TFLite Model |
|--------|----------------|---------------|
| Accuracy | **83.00%** | **82.74%** |
| Inference Time | ~6 ms/sample | **~1 ms/sample** |
| Model Size | 9.3 MB | **1.2 MB** |

> The lightweight TensorFlow Lite model retained high diagnostic performance with minimal degradation, validating its deployment readiness for real-time ECG monitoring.

---


---

## 📥 Dataset
The dataset used is the **Chapman University and Shaoxing People’s Hospital ECG Dataset**.  
You can access it via [PhysioNet](https://physionet.org/content/chapman-shaoxing/1.0.0/).

---


