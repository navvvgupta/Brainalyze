# 🧠 Brainalyze: Harmful Brain Activity Classification

**Brainalyze** is a deep learning research project focused on classifying harmful brain activity from EEG signals using advanced ensemble models. The project explores various spectrogram-based preprocessing techniques, transfer learning models, and post-processing methods to reduce the KL divergence and improve classification performance.

---

## 🚀 Project Objective

To enhance EEG-based classification of harmful brain activity (e.g., seizures, LPDs, GPDs) by minimizing the KL divergence score using a robust ensemble approach.

---

## 📂 Dataset

- Publicly available EEG datasets with annotations for seizure, LPD, GPD, and other patterns.
- Multichannel recordings (e.g., 10–20 system) with sampling rates between 128Hz and 1024Hz.
- Preprocessed using STFT and CWT to generate spectrograms.

---

## 🧠 Models Used

### 1. **HMS ResNet1D-GRU**
- Hybrid model processing raw EEG signals
- Achieved initial KL score: `0.473656`
- Improved to `0.468036` with Adan optimizer and hyperparameter tuning

### 2. **[Inference] Features + Head Starter [K+E+KE]**
- EfficientNetB0 Starter: `0.513482`
- WaveNet Starter: `0.520000`
- Combined: `0.419259`

### 3. **Final Ensemble Model**
- EfficientNetB0 on:
  - Raw Spectrograms
  - Optimized Spectrograms (with augmentation)
  - Custom-Generated Spectrograms
- Final KL Score: `0.3855`

---

## 🛠 Techniques Applied

- **Transfer Learning** with EfficientNetV2 and Vision Transformers
- **Signal Preprocessing**: STFT & CWT
- **Post-processing**: Temperature Scaling, Power Tuning
- **Optimizers**: Adan, Adam, SGD comparison

---

## 📊 Evaluation Metric

- **Kullback–Leibler Divergence (KL Score)** used as the primary metric

---
