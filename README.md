# Object Detection and Pose Estimation Pipeline

This project implements a complete pipeline for object detection and pose estimation using YOLO and PoseNet models. The pipeline processes both RGB and depth data to detect objects and estimate human poses.

## Prerequisites

- Python 3.6+
- Jupyter Notebook


## Project Structure

The project consists of the following Jupyter notebooks, which should be executed in order:

1. `yolo-object-detection-training.ipynb`
   - Trains a YOLO model for object detection
   - Output: Trained YOLO model weights

2. `cropping-object-from-rgb.ipynb`
   - Processes RGB images to detect and crop objects
   - Uses the trained YOLO model for detection
   - Output: Cropped RGB images of detected objects

3. `SimplePoseNet.ipynb`
   - Implements the SimplePoseNet model for object pose estimation
   - Processes the cropped RGB images
   - Output: Pose estimation results

4. `SimplePoseNetEvaluation.ipynb`
   - Evaluates the performance of the SimplePoseNet model
   - Output: Performance metrics and visualizations

5. `cropping-object-from-depth.ipynb`
   - Processes depth data corresponding to the RGB images
   - Uses the same object detections to crop depth data
   - Output: Cropped depth maps

6. `extension.ipynb`
   - Implements extended functionality 
   - Output: Pose estimation results

7. `extensionevaluation.ipynb`
   - Evaluates the performance of the extension
   - Output: Evaluation metrics and results

## Getting Started

1. Clone this repository
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the required packages
   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebooks in the specified order using Jupyter:
   ```bash
   jupyter notebook
   ```
   Then open and run each notebook in the order listed above.

## Data Organization

Please organize your data in the following structure:
```
data/
├── rgb/
│   ├── train/
│   └── test/
├── depth/
│   ├── train/
│   └── test/
└── annotations/
    ├── train/
    └── test/
```

## Notes

- Make sure to update the file paths in each notebook according to your system configuration.
- The training process might require significant computational resources, especially for the YOLO and PoseNet models.
- For best results, ensure your training data is well-balanced and representative of your use case.


