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

The dataset used in this project was obtained from Kaggle:

- **Name:** Pothole Detection Dataset  
- **Kaggle:** https://www.kaggle.com/datasets/atulyakumar98/pothole-detection-dataset, https://www.kaggle.com/datasets/mahyeks/pothrgbd-rgb-and-depth-images-of-potholes
- **hugging face:** Ryukijano/Pothole-detection-Yolov8, keremberke/pothole-segmentation, manot/pothole-segmentation


The raw images and labels are **not included** in this GitHub repository in order to
respect dataset licensing and keep the repo size small.

To reproduce the experiments:

1. Download the dataset from Kaggle.
2. Extract it into the local `data/` folder at the root of this project, e.g.:

   ```text
   Pothole-detection/
   ├── pothole_detection_yolov8_rtdetr.ipynb
   ├── README.md
   └── dataset/
       ├── images/
       └── labels/

