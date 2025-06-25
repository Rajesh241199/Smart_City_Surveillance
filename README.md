# 🚦 Smart City Traffic Surveillance System

A comprehensive **traffic surveillance and analytics solution** leveraging **YOLOv8**, **DeepSORT**, and video analytics for **vehicle classification**, **unique object tracking**, **speed estimation**, and **unique person counting**.

---

## 📌 Project Overview

This project focuses on building a **traffic surveillance pipeline** for **North Carolina, USA**, integrating:

- Vehicle and person detection using YOLOv8.
- Multi-object tracking using DeepSORT.
- Speed estimation per vehicle.
- Exporting results for visualization.

## 📂 Repository Structure

```
├── Training.ipynb               # YOLOv8 model fine-tuning notebook
├── Final_Analysis.ipynb          # Inference, tracking, speed, and person count with video output
├── VisDrone_local.yaml           # Dataset configuration (YOLO format)

## 🚀 Features Implemented

✅ Vehicle and Person Classification  
✅ Multi-class Tracking with DeepSORT  
✅ Speed Estimation using pixel distance and FPS  
✅ Unique Person Counting with Rider Filtering (IoU-based)  
✅ Output video with bounding boxes, IDs, speed labels, and person count overlay  

---

## 🛠️ Technologies Used

- YOLOv8 (Ultralytics)
- DeepSORT for tracking
- OpenCV for video processing
- Python 3.x
- PyTorch and TorchVision
- Optional: Integration with AWS and Power BI (future phase)

---

## ✅ Model Training Details

- Dataset: Custom vehicle detection dataset with classes:
  ```
  ['person', 'car', 'van', 'truck', 'bus', 'motorcycle', 'bicycle', 'threewheel']
  ```
- Model Base: Pretrained YOLOv8 COCO model
- Config File: `VisDrone_local.yaml`
- Training Notebook: `Training.ipynb`

---

## ✅ Post-Processing (Video Analysis)

- Notebook: `Final_Analysis.ipynb`
- Features:
  - DeepSORT tracking
  - Speed calculation
  - Rider filtering
  - Unique person count
  - Output video generation

---

## ✅ Dataset Structure (YOLO Format)

```
vehicle dataset/
├── train/
│   ├── images/
│   └── labels/
├── valid/
│   ├── images/
│   └── labels/
```

---

## ✅ How to Run

1. **Model Training:**
   - Open `Training.ipynb`
   - Update dataset path and YAML if needed
   - Run all cells to train your YOLOv8 model

2. **Video Analysis:**
   - Open `Final_Analysis.ipynb`
   - Set input video path and model path
   - Run all cells to process and save the output video

3. **Results:**
   - Output video saved as: `output_highway_analysis.mp4`
