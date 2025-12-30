# Audio-Based Emotion Recognition Experiments

This repository contains **audio-only emotion recognition experiments**
conducted using the **CREMA-D dataset**.  
The focus is on building and evaluating **audio expert models** that can later
be used independently or as part of a multimodal emotion recognition system.

---

## 🎯 Project Objective
- Perform emotion recognition using **speech/audio signals**
- Compare **classical feature-based** and **deep learning–based** approaches
- Conduct systematic experiments with controlled training protocols
- Provide reproducible and well-documented experimental notebooks

---

## 🧠 Modeling Approaches

Two distinct audio modeling strategies are explored:

### 1️⃣ MFCC-Based Audio Models
- Classical signal-processing features (MFCC)
- Clean and reproducible training pipeline
- Used as a strong and interpretable baseline

### 2️⃣ Wav2Vec2-Based Audio Models
- Pretrained self-supervised speech representations
- Fine-tuning with different configurations (FAST / FULL modes)
- Extensive experimentation with unfreeze depth, learning rates, and input length

---

## 📂 Notebook Overview

### `AUDIO_00_raw_CREMA-D_dataset_sanity_v01.ipynb`
- Initial dataset inspection
- Sanity checks on CREMA-D audio samples
- Early feature extraction trials

---

### `AUDIO_04_experiments_CREMA-D_wav2vec2_gridsearch_v01.ipynb`
- Main experimental notebook
- Wav2Vec2-based Speech Emotion Recognition (SER)
- FAST vs FULL training strategies
- Hyperparameter exploration:
  - Unfreeze depth
  - Learning rates (head / backbone)
  - Maximum audio duration
  - SpecAugment configurations

This notebook serves as the **audio expert experiment log**.

---

### `AUDIO_05_final_audio_emotion_results_v01.ipynb`
- Final and consolidated results
- MFCC-based audio emotion recognition
- Clean training and evaluation pipeline
- Final performance metrics and analysis

---

## 📦 Model Checkpoints
Due to GitHub file size limitations, trained model checkpoints
(`.pt` / `.pth`) are **not included** in this repository.

Model files can be provided upon request or hosted on external storage.

---

## 🔬 Dataset
- **CREMA-D (Crowd-sourced Emotional Multimodal Actors Dataset)**
- Audio-only modality is used in this repository

---

## 👩‍💻 Author
**Arzu Selda Avcı**  
Computer Engineering – Deep Learning / Speech Emotion Recognition
