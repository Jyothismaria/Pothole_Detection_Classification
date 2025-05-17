# Pothole Detection and Severity Classification

This project implements a robust end-to-end system for detecting potholes and classifying their severity using deep learning. The final model integrates a detection stage (YOLOv11) with a dedicated severity classification model, designed to work together as a pipeline.

## Final Model

The final model is a two-stage pipeline:

1. Detection using YOLOv11 (`detection_best.pt`)
2. Severity Classification using YOLOV8 (`classifier_best.pt`)

This modular architecture helps isolate detection from classification, allowing use of different training datasets and improving performance on severity estimation.

## How to Run

### Step-by-Step Instructions
Run Final Pipeline
   - Open the `pipeline` notebook
   - This executes the full model: detection followed by severity classification
   - Outputs are saved and visualized

## Additional Tools

### Detection Model Training

- To train new YOLO models, use the `detection` Jupyter notebook
- This was used to test various YOLOv configurations
- This file needs to be run in Google Colab

##  Run Dataset Transformation
   - Open and run the `dataset_transformation` notebook
   - This loads and preprocesses data for the classification model training 

### Large Dataset Training

- The zipped folder (`Pothole Detection.v1i.yolov11.zip`) was used to train a larger pothole detection model on a more extensive dataset. Not uploaded in github due to large size. But can be loaded through roboflow. Look at `detection` for the code.

## Results

- Realistic detection and severity classification on both clean and rainy conditions
- Visual examples available in `detection_classification_results.png`

## Notes

- Severity labels: `major`, `medium`
- Designed to be modular, scalable, and realistic for deployment
- Trained and validated on data with real-world camera perspectives

## Citations
@software{yolov8_ultralytics,
  author = {Glenn Jocher and Ayush Chaurasia and Jing Qiu},
  title = {Ultralytics YOLOv8},
  version = {8.0.0},
  year = {2023},
  url = {https://github.com/ultralytics/ultralytics},
  orcid = {0000-0001-5950-6979, 0000-0002-7603-6750, 0000-0003-3783-7069},
  license = {AGPL-3.0}
}

@software{yolo11_ultralytics,
  author = {Glenn Jocher and Jing Qiu},
  title = {Ultralytics YOLO11},
  version = {11.0.0},
  year = {2024},
  url = {https://github.com/ultralytics/ultralytics},
  orcid = {0000-0001-5950-6979, 0000-0002-7603-6750, 0000-0003-3783-7069},
  license = {AGPL-3.0}
}

@software{yolov5,
  title = {Ultralytics YOLOv5},
  author = {Glenn Jocher},
  year = {2020},
  version = {7.0},
  license = {AGPL-3.0},
  url = {https://github.com/ultralytics/yolov5},
  doi = {10.5281/zenodo.3908559},
  orcid = {0000-0001-5950-6979}
}

https://medium.com/data-science/the-comprehensive-guide-to-training-and-running-yolov8-models-on-custom-datasets-22946da259c3
