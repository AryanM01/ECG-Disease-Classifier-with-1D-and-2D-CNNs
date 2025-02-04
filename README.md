# Deep Learning for Cardiovascular Disease Detection Using ECG

This project uses ECG signals to implement a deep learning pipeline for detecting cardiovascular diseases (CVDs). It utilizes hybrid convolutional neural networks (CNNs) for feature extraction and classification, achieving high accuracy in identifying various heart conditions.

---

## **Table of Contents**
- [Overview](#overview)
- [Dataset](#dataset)
- [Approach](#approach)
- [Results](#results)
  
---

## **Overview**
This project aims to classify ECG signals into five categories:
1. Normal (N)
2. Left Bundle Branch Block (L)
3. Right Bundle Branch Block (R)
4. Atrial Premature Beat (A)
5. Premature Ventricular Contraction (V)

The model combines:
- **1D CNN** for analyzing raw ECG signals.
- **2D CNN** (using AlexNet architecture) for analyzing scalograms generated from ECG signals.

---

## **Dataset**
The project uses the **MIT-BIH Arrhythmia Dataset**, which contains annotated ECG signals for various arrhythmias. The dataset includes:
- Preprocessed ECG signals for 1D CNN analysis.
- Scalogram images created from the ECG signals for 2D CNN analysis.

---

## **Approach**
1. **1D CNN**:
   - Processes raw ECG signals to learn temporal patterns.
   - Achieves a test accuracy of **98.72%** and test loss of **0.0421**.

2. **2D CNN (AlexNet)**:
   - Converts ECG signals into scalogram images for spatial feature extraction.
   - Achieves a validation accuracy of **98%** and validation loss of **0.065**.

---

## **Results**
| Model      | Accuracy | Loss   |
|------------|----------|--------|
| 1D CNN     | 98.40%   | 0.0545 |
| 2D CNN     | 98%      | 0.065  |
