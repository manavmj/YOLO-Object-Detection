🚀 YOLO Object Detection Experiments (v8, v9, v10)

This repository contains implementations and experiments using different versions of the YOLO (You Only Look Once) object detection models:

YOLOv8
YOLOv9
YOLOv10

The project demonstrates training object detection models on custom datasets using the Ultralytics YOLO framework.

📌 Project Overview

This project focuses on:

Training YOLO models on custom datasets
Comparing different YOLO versions
Understanding performance and training workflows
Implementing object detection using deep learning

Each notebook corresponds to a specific YOLO version and follows a similar pipeline:

Install dependencies
Load dataset configuration
Initialize model
Train model
📁 Project Structure
├── yolov8.ipynb     # Training using YOLOv8
├── yolov9.ipynb     # Training using YOLOv9
├── yolov10.ipynb    # Training using YOLOv10
└── README.md
⚙️ Installation

Install required libraries:

pip install ultralytics opencv-python numpy pillow
📊 Dataset

The project uses custom datasets defined using .yaml configuration files.

Example:

path_dataset1_config = '/path/to/dataset/data.yaml'

Each dataset should follow YOLO format:

dataset/
├── images/
│   ├── train/
│   ├── val/
├── labels/
│   ├── train/
│   ├── val/
└── data.yaml
🧠 Model Training
YOLOv8
from ultralytics import YOLO

model = YOLO('yolov8s.pt')
model.train(data=path_dataset1_config, epochs=40)
YOLOv9
model = YOLO('yolov9c.pt')
model.train(data=path_dataset1_config, epochs=40)
YOLOv10
model = YOLO('yolov10s.pt')
model.train(data=path_dataset1_config, epochs=40)

🔍 Features
Uses Ultralytics YOLO API
Supports multiple datasets
Easy-to-modify training pipeline
Works on Kaggle/Colab/local environments

📈 Future Improvements
Add model evaluation metrics comparison (mAP, precision, recall)
Hyperparameter tuning
Real-time object detection using webcam
Deployment using Flask/Streamlit

💡 Use Cases
Object detection projects
Academic research
Learning computer vision
Experimenting with latest YOLO versions
