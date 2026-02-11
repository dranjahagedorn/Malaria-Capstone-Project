# Malaria Detection using Deep Learning  
Computer Vision for Medical Diagnostics

## Overview

This project develops and evaluates deep learning models for automated malaria detection from microscopic blood smear images.  
The goal is to assess how convolutional neural networks can support large-scale screening in high-burden regions.

Rather than optimizing for accuracy alone, the project emphasizes clinically meaningful metrics such as recall (sensitivity) and deployment feasibility.

---

## Problem Context

Malaria remains a major global health challenge:

- 229 million cases worldwide  
- ~400,000 deaths annually  
- Manual microscopy diagnosis is time-consuming and error-prone  

In high-volume or low-resource environments, automated pre-screening can significantly reduce diagnostic load while improving consistency.

---

## Dataset

- 24,958 training images  
- 2,600 test images  
- Balanced classes:
  - Parasitized
  - Uninfected  
- Colored microscopy images of individual red blood cells  

Due to dataset size and licensing constraints, raw image data is not included in this repository.

---

## Modeling Strategy

### 1. Exploratory Data Analysis
- Class balance verification  
- Image distribution analysis  
- Visual inspection of infection patterns  
- HSV vs. RGB color comparison  

### 2. Preprocessing
- Normalization  
- Data augmentation  
- Image resizing and standardization  

### 3. Model Development
Multiple architectures were evaluated:

- Baseline CNN  
- Regularized CNN variants  
- Transfer Learning with pre-trained networks  

### Final Model
Fine-tuned **VGG16 (ImageNet weights)**

---

## Final Model Performance (Test Set)

- **Accuracy:** 96.5%  
- **Recall (Sensitivity):** 96.8%  
- **Precision:** 96.2%  
- **Inference time:** <50ms per image  

High recall is particularly important in medical screening, as missed infections carry significant clinical risk.

---

## Why This Matters

This model:

- Reduces diagnostic time dramatically  
- Minimizes missed infections  
- Maintains low false-positive rates  
- Enables near real-time inference  

Performance exceeds typical manual microscopy accuracy (70–90%) while providing consistent output.

---

## Deployment Considerations

Potential rollout strategy:

- Pilot implementation in selected diagnostic centers  
- Continuous dataset expansion to reduce bias  
- Integration into smartphone microscopy tools  
- Early regulatory alignment (FDA / WHO frameworks)  

This system is designed to **augment**, not replace, clinical expertise.

---

## Repository Structure

- `Malaria_Detection_Notebook.ipynb` – Full training & evaluation pipeline  
- `Malaria_Detection_Notebook.html` – Exported notebook for quick review  

---

## Technologies

Python  
TensorFlow / Keras  
NumPy  
Matplotlib  
scikit-learn  

---

Dr. Anja Hagedorn  
Applied AI & Data Science
