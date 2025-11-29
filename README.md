# Pothole Detection and Segmentation using YOLOv8 and RT-DETR

## 1. Project Overview

This repository contains a computer vision project that detects and segments potholes from road images using deep learning. The goal is to support road maintenance and safety by automatically identifying pothole locations, comparing different object detection architectures, and producing metrics that can guide model selection for real-world deployment.

We compare **YOLOv8m-seg** and an **RT-DETR** variant on a Kaggle pothole dataset. The project includes:
- End-to-end training pipelines
- Evaluation on a held-out test set
- Benchmarking using **mAP**, **IoU**, **precision/recall**, **F1-score**, and runtime/resource usage

> This repository is structured as a **team-ready, production-style** project with clear code organization, comments, and documentation, but can also be used by a single developer.

---

## 2. Dataset

- **Source:** [Kaggle – Pothole Detection Dataset](https://www.kaggle.com/datasets/atulyakumar98/pothole-detection-dataset)
- **Content:** Road images captured in real-world conditions with visible potholes.
- **Annotations:**
  - Bounding boxes in YOLO format for pothole detection.
  - (Optional) Segmentation masks or conversion for YOLOv8 segmentation and RT-DETR.

### 2.1. Data Organization

After downloading the dataset, organize it as:

```text
data/
├── raw/              # original Kaggle download
├── processed/        # resized / cleaned images
└── annotations/      # YOLO labels, segmentation masks
