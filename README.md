# TF-PiSinger: Time–Frequency Domain Pitch Control for Expressive Singing Voice Synthesis

> Official demo page: [TF-PiSinger Demo](https://shjang97.github.io/TF-PCSingerDemo/)  
> **Note:** The source code will be released in the near future.

---

## ✨ Overview

**TF-PiSinger** is a novel end-to-end **singing voice synthesis (SVS)** model that enhances **pitch expressiveness** by jointly modeling pitch information in both the **time and frequency domains**.  
Unlike previous methods that rely on explicit F₀ modeling and fixed harmonic structures, TF-PiSinger introduces:
- a **diffusion-based F₀ predictor** for natural pitch trajectories, and  
- an **adaptive harmonic network** for expressive spectral representation.  

Evaluations on a Korean singing dataset show that TF-PiSinger significantly outperforms existing SVS models in both **audio quality** and **pitch expressiveness**.

---

## 🧠 Motivation

While end-to-end SVS models have improved naturalness and stability, expressive singing techniques such as **vibrato**, **pitch bending**, and **dynamic control** remain challenging.  
TF-PiSinger addresses this by introducing **joint time–frequency pitch modeling**, capturing both temporal and spectral nuances for emotionally rich singing synthesis.

---

## 🏗️ Model Architecture

### 1️⃣ Time Module
- **Diffusion-based F₀ predictor** with **FiLM conditioning** that captures fine-grained and continuous pitch variations.

### 2️⃣ Frequency Module
- **Adaptive DDSP-based harmonic network** that dynamically models **phoneme-dependent harmonic structures**.

### 3️⃣ Decoder
- Utilizes **HiFi-GAN** for high-fidelity waveform generation.

---

## 🔊 Experimental Results

| Model | MOS-Q ↑ | MOS-P ↑ | F₀ RMSE ↓ | Mel RMSE ↓ |
|:------|:--------:|:--------:|:----------:|:------------:|
| Ground Truth | 4.50 ± 0.11 | 4.20 ± 0.14 | – | – |
| VITS | 3.55 ± 0.24 | 3.12 ± 0.16 | 0.45 | 0.52 |
| VISinger2 | 3.85 ± 0.35 | 3.56 ± 0.20 | 0.35 | 0.42 |
| **TF-PiSinger (proposed)** | **3.91 ± 0.18** | **3.84 ± 0.21** | **0.28** | **0.35** |

Spectrogram comparisons show that TF-PiSinger produces **stable, natural vibrato** and smooth pitch transitions.

---

## 🎧 Demo

- Listen to the samples: [TF-PiSinger Demo](https://shjang97.github.io/TF-PCSingerDemo/)  
- Includes comparisons with baseline models and expressive pitch control demonstrations.

---

## 🧩 Dataset

- Korean Singing Voice Dataset (AI-Hub)  
- Single professional female singer, 2 hours total, 44.1 kHz recordings.  
- Preprocessing: mel-spectrograms (window=1024, hop=256)

---
