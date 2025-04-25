# Pothole Detection and Severity Classification

This project implements a robust end-to-end system for detecting potholes and classifying their severity using deep learning. The final model integrates a detection stage (YOLOv11) with a dedicated severity classification model, designed to work together as a pipeline.

## Final Model

The final model is a two-stage pipeline:

1. Detection using YOLOv11 (`detection_best.pt`)
2. Severity Classification using YOLOV8 (`classifier_best.pt`)

This modular architecture helps isolate detection from classification, allowing use of different training datasets and improving performance on severity estimation.

## How to Run

### Step-by-Step Instructions

1. Run Dataset Transformation
   - Open and run the `dataset_transformation` notebook
   - This loads and preprocesses data, including test samples with clean and rainy pothole conditions

2. Run Final Pipeline
   - Open the `pipeline` notebook
   - This executes the full model: detection followed by severity classification
   - Outputs are saved and visualized

## Additional Tools

### Detection Model Training

- To train new YOLO models, use the `detection` Jupyter notebook
- This was used to test various YOLOv11 configurations

### Large Dataset Training

- The zipped folder was used to train a larger pothole detection model on a more extensive dataset

## Results

- Realistic detection and severity classification on both clean and rainy conditions
- Visual examples available in `detection_classification_results.png`

## Notes

- Severity labels: `major`, `medium`
- Designed to be modular, scalable, and realistic for deployment
- Trained and validated on data with real-world camera perspectives

