# Deep Learning for Cardiovascular Disease Detection Using ECG

This project implements a deep learning pipeline for detecting cardiovascular diseases (CVDs) using ECG signals. It utilizes hybrid convolutional neural networks (CNNs) for feature extraction and classification, achieving high accuracy in identifying various heart conditions.

---

## **Table of Contents**
- [Overview](#overview)
- [Dataset](#dataset)
- [Approach](#approach)
- [Results](#results)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)
- [File Structure](#file-structure)
- [Acknowledgments](#acknowledgments)

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
| 1D CNN     | 98.72%   | 0.0421 |
| 2D CNN     | 98%      | 0.065  |

---

## **How to Run**

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/ECG-CVD-Detection.git
   cd ECG-CVD-Detection
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Preprocess the dataset (if not already done):
   - Extract ECG signals and generate scalogram images.
   - Update the dataset paths in the script.

4. Train the models:
   - Run the 1D CNN:
     ```bash
     python train_1d_cnn.py
     ```
   - Run the 2D CNN:
     ```bash
     python train_2d_cnn.py
     ```

5. Evaluate the models:
   ```bash
   python evaluate.py
   ```

---

## **Dependencies**
- Python 3.8+
- TensorFlow
- NumPy
- SciPy
- Matplotlib
- PyWavelets
- PIL (Pillow)

---

## **File Structure**
```
ECG-CVD-Detection/
├── data/
│   ├── raw_ecg_signals/
│   ├── scalograms/
├── models/
│   ├── 1d_cnn_model.h5
│   ├── 2d_cnn_model.h5
├── train_1d_cnn.py
├── train_2d_cnn.py
├── evaluate.py
├── requirements.txt
├── README.md
```

---

## **Acknowledgments**
- The **MIT-BIH Arrhythmia Dataset** provided the foundation for this work.
- Scalograms were generated using **PyWavelets**.
- Special thanks to the open-source community for frameworks like TensorFlow.
