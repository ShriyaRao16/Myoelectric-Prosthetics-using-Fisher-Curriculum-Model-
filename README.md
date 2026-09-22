# Edge-Based Subject Profiling for Low-Cost Myoelectric Prosthetics

### Fisher Stratification and Curriculum Learning on Arduino–Raspberry Pi Architecture

> **Research Project | Edge AI | Myoelectric Control | Assistive Technology | Embedded Machine Learning**

---

## 📌 Overview

This repository contains the implementation, experimental analysis, and embedded-system development associated with the research work:

**“Edge-Based Subject Profiling for Low-Cost Myoelectric Prosthetics: Fisher Stratification and Curriculum Learning on Arduino–Raspberry Pi Architecture”**

The project investigates a **low-cost edge-based myoelectric prosthetic control architecture** that combines surface electromyography (sEMG), embedded processing, subject profiling, and machine learning for controlling a tendon-driven prosthetic hand.

The primary objective is to investigate whether **subject-aware signal stratification** and **progressive training through Curriculum Learning** can improve the reliability and practical deployment of myoelectric control systems under resource-constrained conditions.

The system combines:

- Surface EMG signal acquisition
- Time-domain feature extraction
- Fisher-based subject stratification
- Curriculum Learning
- Random Forest classification
- Raspberry Pi edge processing
- Arduino-based control
- Real-time prosthetic hand actuation

---

# 🎯 Research Objectives

The project focuses on the following objectives:

1. Acquire and process surface EMG signals from forearm muscles.
2. Extract meaningful time-domain EMG features.
3. Characterize differences between subjects using Fisher-based stratification.
4. Develop subject-aware data organization and profiling.
5. Apply Curriculum Learning by progressively training the model using easier and more difficult signal samples.
6. Deploy the machine-learning pipeline on an edge-computing architecture.
7. Control a physical prosthetic hand using predicted muscle-intent classes.
8. Evaluate classification performance across subjects and difficulty levels.
9. Measure computational requirements and real-time response.
10. Investigate the feasibility of low-cost embedded myoelectric prosthetic control.

---

# 🧠 Research Motivation

Surface electromyography (sEMG) provides a non-invasive method for interpreting muscle activity and generating control commands for myoelectric prostheses.

However, EMG signals are highly variable due to factors such as:

- Inter-subject variability
- Electrode placement
- Muscle activation patterns
- Contraction intensity
- Limb position
- Muscle fatigue
- Signal noise
- Anatomical differences
- Recording conditions

Therefore, this research investigates whether **subject-aware signal stratification combined with Curriculum Learning** can provide a more structured approach to training machine-learning models for myoelectric control.

The central research question is:

> **Can subject-level EMG characteristics be used to organize learning difficulty and progressively train an edge-based classifier for robust prosthetic control?**

---

# 🔬 Proposed Research Framework

```text
              Surface EMG
                   │
                   ▼
        ┌────────────────────┐
        │ Signal Acquisition │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Preprocessing &    │
        │ Segmentation       │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Feature Extraction │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Fisher-Based       │
        │ Subject            │
        │ Stratification     │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Curriculum         │
        │ Learning           │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Random Forest      │
        │ Classifier         │
        └──────────┬─────────┘
                   │
                   ▼
           Predicted Intent
                   │
                   ▼
        ┌────────────────────┐
        │ Raspberry Pi       │
        │ Edge Processing    │
        └──────────┬─────────┘
                   │
                   ▼
        ┌────────────────────┐
        │ Arduino Control    │
        └──────────┬─────────┘
                   │
                   ▼
           Prosthetic Hand\
```
# Hardware Architecture 
```text
              ┌─────────────────┐
              │ MyoWare EMG     │
              │ Sensor          │
              └────────┬────────┘
                       │
                       │ EMG Signal
                       ▼
              ┌─────────────────┐
              │ Arduino Uno     │
              │ Acquisition /   │
              │ Interface       │
              └────────┬────────┘
                       │
                       │ Serial Communication
                       ▼
              ┌─────────────────┐
              │ Raspberry Pi 4  │
              │ Edge AI         │
              └────────┬────────┘
                       │
                       │ Predicted Motion
                       ▼
              ┌─────────────────┐
              │ Arduino Uno     │
              │ Actuator Control│
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Prosthetic Hand │
              └─────────────────┘
```
# Machine Learning Pipeline 
``` text
Raw EMG Signal
      │
      ▼
Signal Filtering
      │
      ▼
Windowing
      │
      ▼
Feature Extraction
      │
      ├── RMS
      ├── MAV
      ├── WL
      ├── ZC
      └── CV
      │
      ▼
40-Dimensional Feature Vector
      │
      ▼
Fisher Stratification
      │
      ▼
Subject Profiling
      │
      ▼
Difficulty Estimation
      │
      ▼
Curriculum Construction
      │
      ▼
Random Forest Training
      │
      ▼
Motion Classification
      │
      ▼
Prosthetic Actuation
```
# Classification Flow 
```text
              EMG Signal
                  │
                  ▼
             Preprocessing
                  │
                  ▼
          Feature Extraction
                  │
                  ▼
        Fisher-Based Profiling
                  │
                  ▼
        Curriculum-Based Model
                  │
                  ▼
           Random Forest
                  │
                  ▼
          Predicted Motion
                  │
        ┌─────────┼─────────┐
        ▼         ▼         ▼
     Motion 1   Motion 2   Motion 3
        │         │         │
        └─────────┼─────────┘
                  ▼
          Prosthetic Hand
```
# Research Contribution
``` text
Fisher Stratification
        ↓
Subject Profiling
        ↓
Difficulty Estimation
        ↓
Curriculum Learning
        ↓
Random Forest
        ↓
Edge Inference
        ↓
Real-Time Prosthetic Control
```
The work investigates the relationship between subject variability, EMG signal characteristics, learning difficulty, and embedded machine-learning performance.
# Technology Stack
```text
Hardware
├── Arduino Uno
├── Raspberry Pi 4
├── MyoWare EMG Sensor
├── EMG Electrodes
└── 3D-Printed PLA Prosthetic Hand

Software
├── Python
├── C/C++
├── Arduino IDE
├── Scikit-learn
├── NumPy
└── Pandas

Machine Learning
├── Random Forest
├── Fisher Stratification
├── Curriculum Learning
└── Feature Engineering
```
Potential extensions include:

-Personalized EMG calibration<br>
-Adaptive Curriculum Learning<br>
-Cross-session validation<br>
-Lightweight neural networks<br>
-TinyML deployment<br>
-Multi-channel EMG<br>
-Online learning<br>
-Lower-power embedded deployment<br>
# Publication
Edge-Based Subject Profiling for Low-Cost Myoelectric Prosthetics: Fisher Stratification and Curriculum Learning on Arduino–Raspberry Pi Architecture

IEEE INDISCON 2026
# Keywords
> Myoelectric Prosthetics| EMG| Edge AI | Fisher Stratification | Curriculum Learning | Random Forest
> | Arduino| Raspberry Pi| Embedded ML| Assistive Technology| Prosthetic Hand | Biomedical Engineering | Real-Time Classification

