# Bio-Physiological Deepfake Detection

[![Status](https://img.shields.io/badge/Status-Under%20Peer%20Review-orange.svg)]()
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-Framework-red.svg)]()

Research repository for a multimodal deepfake detection framework that leverages **bio-physiological cues**—specifically combining breathing-based audio analysis and multi-scale facial neuromuscular dynamics—for robust fake video and audio identification.

---

## 📌 Overview

Traditional deepfake detectors frequently overfit to visual artifacts or spatial compression anomalies that are easily mitigated by newer generative architectures. This project approaches detection through the lens of human physiological invariants:

* **Audio Physiology (Pillars 1–3):** Analyzes macro-respiratory timing sequences, subglottal pressure decay micro-dynamics, and vocal tract aerodynamic texture .
* **Facial Neuromuscular Dynamics (Pillar 4):** Evaluates multi-scale time-varying coactivation trajectories ($\rho(t)$) across ocular and oral Action Units to catch frame-by-frame generative synthesis incoherence.
* **Cross-Dataset Generalization:** Rigorously tested against uncalibrated in-the-wild corpora and unseen vocoder verification boundaries.

---

## 🚀 Key Features

* **Multimodal Audio-Video Architecture:** Fuses acoustic physiological markers with video-level facial expression trajectories.
* **Multi-Scale Trajectory Analysis:** Tracks coactivation coherence across fast ($0.3\text{ s}$), medium ($0.6\text{ s}$), and slow ($1.2\text{ s}$) temporal windows.
* **Robust Evaluation Workflows:** Extensively benchmarked using stratified 10-fold cross-validation and cross-domain zero-shot setups.

---

## 🛠️ Tech Stack

* **Core:** Python, PyTorch
* **Computer Vision:** OpenCV, dlib / MediaPipe face tracking pipelines
* **Audio Processing:** Librosa, SciPy
* **Modeling & Metrics:** Scikit-learn, XGBoost, Random Forest

---

## 📊 Summary of Results

* **Within-Domain Performance:** Achieved up to **95.00%** single-split accuracy and **93.00%** mean 10-fold cross-validation accuracy ($0.98$ AUC) on benchmark corpora using ensemble classifiers.
* **Feature Ablation Insights:** Proved that vocal tract organic texture metrics provide dominant standalone discriminative capacity ($>93\%$ accuracy), while multi-pillar fusion captures complementary physical properties.
* **Generalization Trade-offs:** Demonstrated high recall bounds on wild holdouts and high precision limits against unseen vocoder architectures.

---

## 📖 Citation & Publication Status

This repository serves as the official companion overview for an ongoing master's research thesis. 

* **Implementation Code and Pre-trained Weights:** Will be fully released publicly following official paper acceptance and publication.
* 

---

## 📝 License

This project is currently protected under restricted academic usage. 
