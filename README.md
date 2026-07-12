# ShieldSight-PPE-Detection
Detect PPE Compliance 
# ShieldSight: PPE Compliance Detection System

## Team Members

**Brandi Green**

---

# Project Tier

**Tier 2 – Object Detection**

**Tier Justification:**
This project uses object detection to identify workers and personal protective equipment (PPE) in construction site images. The system will detect hard hats and safety vests to help identify potential PPE compliance issues.

---

# Problem Statement

Construction sites, warehouses, and manufacturing facilities require workers to wear personal protective equipment (PPE) to reduce the risk of injuries. Monitoring every worker manually can be difficult, especially on large job sites. Missed PPE violations can lead to workplace accidents, OSHA violations, and increased costs.

This project aims to develop an automated computer vision system that detects workers and required PPE to assist with workplace safety monitoring.

---

# Solution Overview

ShieldSight uses the YOLO11 object detection model to analyze construction site images and detect workers wearing hard hats and safety vests. The system displays detected objects with bounding boxes and confidence scores while helping identify potential PPE compliance issues.

---

# Technical Approach

**CV Technique**
- Object Detection

**Model**
- YOLO11

**Framework**
- Ultralytics
- PyTorch

**Development Environment**
- Google Colab

**Why this approach**

YOLO11 is designed for fast and accurate real-time object detection. It can detect multiple objects within a single image while providing bounding boxes, class labels, and confidence scores. This makes it well suited for identifying workers and PPE simultaneously in construction environments.

---

# Dataset

**Source**
- Construction Site Safety Image Dataset (Roboflow) – Kaggle

**Size**
- Approximately 2,800 labeled images

**Labels**
- Person
- Hardhat
- NO-Hardhat
- Safety Vest
- NO-Safety Vest

**Dataset Link**
- https://www.kaggle.com/datasets/snehilsanyal/construction-site-safety-image-dataset-roboflow

---

# Success Metrics

**Primary Metric**
- 85% accuracy

**Secondary Metrics**
- Image processing time less than one second per image
- High precision and recall for detecting workers wearing hard hats and safety vests

---

# Week-by-Week Plan

### Week 5
- Select dataset
- Create GitHub repository
- Complete project proposal
- Set up Google Colab environment

### Week 6
- Download dataset
- Run pretrained YOLO11 model
- Verify object detection pipeline

### Weeks 7-8
- Train YOLO11 using the Construction Site Safety dataset
- Fine-tune model parameters
- Evaluate model performance

### Week 9
- Improve detection accuracy
- Record evaluation metrics
- Test on unseen construction images

### Week 10
- Create demonstration
- Finalize README
- Prepare presentation slides
- Submit final project

---

# Resources Needed

**Compute**
- Google Colab (Free)

**Cost**
- $0

**Software**
- Python
- Ultralytics
- PyTorch
- GitHub

---

# Risks & Mitigation

| Risk | Probability | Mitigation |
|------|-------------|------------|
| Dataset may not contain enough examples of all PPE scenarios | Medium | Supplement with another public PPE dataset or collect a small number of additional images |
| Model accuracy may not meet the target | Medium | Apply data augmentation, tune hyperparameters, increase training epochs, or use a larger YOLO11 model |

---

# AI Usage Log

| Date | AI Tool | Purpose |
|------|---------|---------|
| July 2026 | ChatGPT | Brainstormed project ideas, organized the README, and assisted with project timeline. I will complete all coding, training, testing, evaluation, and final implementation. |

---

# Current Status

- ✅ Repository created
- ✅ Proposal completed
- ⬜ Dataset downloaded
- ⬜ Model training started
- ⬜ Model evaluation completed
- ⬜ Demo created
- ⬜ Final presentation completed
