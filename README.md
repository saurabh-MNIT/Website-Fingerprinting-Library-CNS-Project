# Website Fingerprinting Library CNS Project

## Introduction

This project focuses on Website Fingerprinting attacks using Deep Learning techniques for encrypted traffic analysis.

Website Fingerprinting is a cyber attack technique used to identify which website a user is visiting by analyzing encrypted internet traffic. Even though Tor encrypts the data, attackers can still study packet direction, timing, and traffic patterns.

This project uses Deep Learning models to identify websites from encrypted traffic. :contentReference[oaicite:0]{index=0}

---

## Problem Statement

Existing Website Fingerprinting attacks:

- need complete traffic data
- fail under network changes
- perform poorly with defenses
- cannot detect websites early

The goal of this project is to detect websites during the early stage of page loading. :contentReference[oaicite:1]{index=1}

---

## Objectives

- Understand Website Fingerprinting attacks
- Analyze encrypted traffic patterns
- Train Deep Learning models
- Detect websites using early traffic
- Test attack performance on datasets :contentReference[oaicite:2]{index=2}

---

## What is Holmes?

Holmes is a Deep Learning based Website Fingerprinting attack.

It uses:

- Spatial Analysis
- Temporal Analysis
- Contrastive Learning

Holmes can identify which website a user is visiting by analyzing network traffic patterns even before the webpage fully loads. :contentReference[oaicite:3]{index=3}

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

:contentReference[oaicite:4]{index=4}

---

## Dataset Used

Dataset Used:

```text
NCDrift_inf.npz
