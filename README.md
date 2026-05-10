# Website Fingerprinting Library CNS Project

## Introduction

This project focuses on Website Fingerprinting attacks using Deep Learning techniques for encrypted traffic analysis.

Website Fingerprinting is a cyber attack technique used to identify which website a user is visiting by analyzing encrypted internet traffic. Even though Tor encrypts the data, attackers can still study packet direction, timing, and traffic patterns.

This project uses Deep Learning models to identify websites from encrypted traffic.

---

## Problem Statement

Existing Website Fingerprinting attacks:

- need complete traffic data
- fail under network changes
- perform poorly with defenses
- cannot detect websites early

The goal of this project is to detect websites during the early stage of page loading.

---

## Objectives

- Understand Website Fingerprinting attacks
- Analyze encrypted traffic patterns
- Train Deep Learning models
- Detect websites using early traffic
- Test attack performance on datasets

---

## What is Holmes?

Holmes is a Deep Learning based Website Fingerprinting attack.

It uses:

- Spatial Analysis
- Temporal Analysis
- Contrastive Learning

Holmes can identify which website a user is visiting by analyzing network traffic patterns even before the webpage fully loads.

---

## Technology Stack

| Technology | Purpose |
|---|---|
| Python 3.8 | Programming |
| PyTorch | Deep Learning |
| NumPy | Data Processing |
| Scikit-learn | Dataset Splitting |
| VS Code | Development |
| WSL Ubuntu | Linux Environment |

---

## Dataset Used

Dataset Used:

```text
NCDrift_inf.npz
```

Dataset Details:

- 93 website classes
- 6882 traffic samples
- sequence length = 5000

Traffic data contains:

- packet direction
- packet timing information

---

## Dataset Splitting

| Dataset | Samples |
|---|---|
| Training | 5573 |
| Validation | 620 |
| Testing | 689 |

Purpose:

1. Training → model learning
2. Validation → tuning
3. Testing → final evaluation

---

## Project Workflow

```text
Traffic Dataset
        ↓
Preprocessing
        ↓
Dataset Splitting
        ↓
Feature Extraction
        ↓
DF Model Training
        ↓
Testing & Evaluation
```

---

## Model Used

### Deep Fingerprinting (DF)

The project uses the DF model.

DF is:

- a CNN-based Deep Learning model
- designed for Website Fingerprinting attacks

Functions:

- extracts traffic patterns
- learns encrypted traffic behavior
- classifies websites

---

## Training Process

Steps performed:

- loaded dataset
- split dataset
- trained DF model
- generated checkpoint file

Generated Model File:

```text
max_f1.pth
```

---

## Evaluation Metrics

The following metrics were used:

- Accuracy
- Precision
- Recall
- F1-score

These metrics help measure model performance.

---

## Final Results

| Metric | Result |
|---|---|
| Accuracy | 47.61% |
| Precision | 21.75% |
| Recall | 25.86% |
| F1-score | 20.89% |

The model successfully classified encrypted traffic patterns.

---

## How to Run

### Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Dataset Splitting

```bash
python exp/dataset_process/dataset_split.py --dataset NCDrift_inf
```

### Train Model

```bash
bash scripts/DF.sh
```

### Test Model

```bash
python exp/test.py --dataset NCDrift_inf --model DF --device cpu
```

---

## Novelty Work

The novelty of this project is early-stage website fingerprinting detection.

Unlike traditional methods that require complete traffic data, this system can identify websites during the initial loading phase.

The project improves early detection capability using spatial-temporal distribution analysis and Deep Learning techniques.

---

## Repository Structure

```text
Website-Fingerprinting-Library-CNS-Project/
│
├── checkpoints/
├── datasets/
├── exp/
├── figures/
├── scripts/
├── WFlib/
├── README.md
└── requirements.txt
```

---

## Acknowledgement

This project is based on the open-source WFlib framework developed by Xinhao Deng and contributors.

The project was further used and analyzed for CNS academic purposes.

---

## Author

Saurabh Kumar  
B.Tech CSE 3rd Year  
MNIT Jaipur  
CNS Project
