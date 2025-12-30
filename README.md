# Audio-Based Speech Emotion Recognition (SER)

This repository contains **audio-only speech emotion recognition experiments**
conducted on the **CREMA-D dataset**.  
The goal is to systematically evaluate different **audio modeling strategies**
and **data splitting protocols**, and to provide reproducible audio expert
models that can later be integrated into a multimodal emotion recognition system.

---

## 🎯 Project Objectives
- Perform emotion recognition using speech/audio signals
- Compare different **data splitting strategies** (random vs speaker-independent)
- Evaluate both **classical feature-based** and **deep learning–based** audio models
- Report results in a transparent and reproducible manner

---

## 🧠 Audio Modeling Approaches

The repository explores two main audio modeling paradigms:

### 1️⃣ Classical Feature-Based Models (MFCC)
- Mel-Frequency Cepstral Coefficients (MFCC)
- Clean and interpretable pipelines
- Used as strong baselines and for final consolidated results

### 2️⃣ Deep Learning–Based Models (Wav2Vec2)
- Pretrained self-supervised speech representations
- Fine-tuning with different configurations
- Extensive experimentation with training strategies and hyperparameters

---

## 🔀 Data Splitting Strategies

Two different evaluation protocols are intentionally included to highlight
their impact on emotion recognition performance:

### 🔹 Speaker-Independent Split
**`AUDIO_03_modeling_SER_speaker_independent_v01.ipynb`**

- Ensures that speakers appearing in the training set do **not** appear in the test set
- Prevents speaker leakage
- Provides a more realistic and challenging evaluation scenario
- Considered the **academically preferred** protocol

---

### 🔹 Random Split
**`AUDIO_03_modeling_SER_random_split_v01.ipynb`**

- Randomly splits the dataset without enforcing speaker separation
- Often yields higher performance
- Included as a **baseline for comparison**
- Demonstrates the effect of speaker leakage on reported results

Both approaches are retained for **methodological comparison and transparent reporting**.

---

## 📂 Notebook Overview

### `AUDIO_00_raw_CREMA-D_dataset_sanity_v01.ipynb`
- Initial inspection of the CREMA-D dataset
- Sanity checks on audio samples
- Early exploratory feature extraction

---

### `AUDIO_03_modeling_SER_speaker_independent_v01.ipynb`
- Final speaker-independent SER model
- Actor-independent train/test split
- Core reference notebook for realistic evaluation

---

### `AUDIO_03_modeling_SER_random_split_v01.ipynb`
- SER modeling with random train/test split
- Baseline comparison notebook

---

### `AUDIO_04_experiments_CREMA-D_wav2vec2_gridsearch_v01.ipynb`
- Comprehensive deep learning experiment notebook
- Wav2Vec2-based SER
- FAST vs FULL training strategies
- Hyperparameter exploration:
  - Unfreeze depth
  - Learning rates (head / backbone)
  - Maximum audio duration
  - SpecAugment configurations

This notebook serves as the **main experimental log** for audio deep learning models.

---

### `AUDIO_05_final_audio_emotion_results_v01.ipynb`
- Final consolidated results
- MFCC-based audio emotion recognition
- Clean and reproducible evaluation pipeline
- Final performance metrics and analysis

---

## 📦 Model Checkpoints
Due to GitHub file size limitations, trained model checkpoints
(`.pt` / `.pth`) are **not included** in this repository.

Model files can be provided upon request or accessed via external storage.

---

## 🔬 Dataset
- **CREMA-D (Crowd-sourced Emotional Multimodal Actors Dataset)**
- Only the **audio modality** is used in this repository

---

## 👩‍💻 Author
**Arzu Selda Avcı**  
Computer Engineering – Deep Learning / Speech Emotion Recognition
