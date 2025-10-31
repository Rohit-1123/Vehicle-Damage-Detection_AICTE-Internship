# Vehicle-Damage-Detection_AICTE-Internship
### Internship Project — Automotive Domain | Object Detection using Deep Learning  

---

## Overview  

The **Vehicle Damage Detection System** is an AI-powered project that detects and classifies damages on vehicles from images.  
Using **Computer Vision** and **Deep Learning**, it automates the process of identifying scratches, dents, and other external damages — reducing the need for manual inspection.  

This system can be useful for:
- **Insurance claim assessments**
- **Automotive service centers**
- **Vehicle inspection and resale evaluations**

---

## Objective  

To develop a model that can:  
- **Detect** damaged regions on vehicles.  
- **Classify** the type of damage (e.g., scratch, dent, crack).  
- **Highlight** the damaged areas with bounding boxes and confidence levels.

---

## Workflow  

1. **Input**: User uploads an image of a vehicle.  
2. **Preprocessing**: Image is resized and normalized for model compatibility.  
3. **Detection**: YOLOv8 model identifies and classifies damaged areas.  
4. **Output**: Bounding boxes with labels (e.g., “Scratch - 92%”) are drawn on the image.

---

## Tech Stack  

| Component | Tool / Library |
|------------|----------------|
| Programming Language | Python |
| Deep Learning Framework | YOLOv8 (Ultralytics) / PyTorch |
| Image Processing | OpenCV |
| Dataset Handling | Roboflow / Kaggle |
| Data Labeling | LabelImg / Roboflow |
| Optional Web Interface | Flask |
| IDE / Environment | VS Code / Google Colab |

---

## Project Modules  

1. **Data Collection & Labeling**  
   - Collect car images with visible damages.  
   - Label damaged areas using Roboflow or LabelImg.  

2. **Model Training**  
   - Train YOLOv8 on the labeled dataset.  
   - Adjust hyperparameters (epochs, image size, batch size).  

3. **Model Testing & Evaluation**  
   - Test the model on unseen images.  
   - Evaluate accuracy, precision, recall, and mAP.  

4. **Interface (Optional)**  
   - Create a simple Flask web app to upload an image and view results in real time.  

---

## Output Example  

**Input:**  
An image of a damaged car.  

**Output:**  
An image with bounding boxes showing labels such as:  

Scratch (94%)
Dent (88%)


---

## Folder Structure  

```bash
Vehicle-Damage-Detection/
│
├── dataset/                        # All your images and labels go here
│   ├── images/
│   │   ├── train/                    # Training images
│   │   ├── val/                      # Validation images
│   │   └── test/                     # (Optional) Test images
│   │
│   ├── labels/
│   │   ├── train/                    # Bounding box labels for training
│   │   ├── val/                      # Bounding box labels for validation
│   │   └── test/                     # (Optional) Labels for test set
│   │
│   └── data.yaml                     # YOLO configuration file for dataset
│
├── models/                         # YOLO weights and configurations
│   ├── yolov8n.pt                    # Pretrained model (base)
│   └── best.pt                       # Your trained weights
│
├── runs/                           # YOLO saves results automatically here
│   ├── detect/
│   │   ├── train/                    # Training results (plots, weights, etc.)
│   │   └── predict/                  # Test results (annotated images)
│
├── app/                            # Optional Flask Web App
│   ├── static/
│   │   ├── results/                  # Stores output images after detection
│   │   └── style.css                 # Optional styling
│   │
│   ├── templates/
│   │   ├── index.html                # Upload page
│   │   └── result.html               # Display detection result
│   │
│   ├── uploads/                      # Uploaded test images
│   └── app.py                        # Flask app main file
│
├── notebooks/                      # Jupyter notebooks for experiments
│   ├── training.ipynb
│   └── testing.ipynb
│
├── utils/                          # Helper scripts (optional)
│   ├── preprocess.py                 # Resize / clean images
│   ├── split_data.py                 # Split dataset into train/val/test
│   └── visualize.py                  # Plot detection results or stats
│
├── requirements.txt                # All dependencies (YOLO, OpenCV, Flask)
├── README.md                       # Project overview + usage guide
├── main.py                         # Quick test script for running detections
└── report/                         # Project report and screenshots
    ├── results.png
    ├── accuracy_chart.png
    └── final_report.pdf

```
