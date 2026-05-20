# walnut-detection-counting
Walnut detection using YOLOv5 for automated counting in agriculture

## Overview
This project implements an automated computer vision pipeline to detect, track, and count walnuts in video footage. A custom-trained YOLO model is used for object detection, and the SORT (Simple Online and Realtime Tracking) algorithm assigns unique IDs to detected objects across frames to enable reliable counting. The system processes a video of a walnut tree and produces an output video where detected walnuts are highlighted and counted. This project serves as a proof-of-concept for agricultural monitoring applications, such as automated fruit counting and yield estimation.

## Features
Custom-trained YOLO model for walnut detection
Object tracking using SORT
Automatic counting of detected walnuts
Video processing pipeline with bounding boxes and IDs
Output video generation with visualized results

## Project Structure
walnut-detection-counting
│
├── data/
│   └── data.yaml
│
├── models/
│
├── notebooks/
│   └── Walnut_Counting.ipynb
│
├── videos/
│   ├── input_sample.mp4
│   └── counted_output.mp4
│
├── requirements.txt
└── README.md


## Model Weights
The trained model weights are not included in this repository due to file size limitations.

You can download the trained model (best.pt) here:
https://drive.google.com/file/d/1tRob_BDCT8rWPhyHK83rbJ2yRIOnmXbH/view?usp=sharing

Place the downloaded file in the following directory:
models/best.pt

## How It Works
A custom YOLO model detects walnuts in each video frame.
Detected objects are passed to the SORT tracker.
Each walnut receives a unique tracking ID.
The system counts each unique object only once.
A processed video is generated showing bounding boxes, IDs, and the total count.

## Installation
Clone the repository:
git clone https://github.com/your-username/walnut-detection-counting.git
cd walnut-detection-counting

### Install dependencies:
pip install -r requirements.txt

### Usage
Open the notebook:
notebooks/walnut-detection-counting

## Run the cells to:

Load the YOLO model
Run detection on the input video
Track objects using SORT
Generate the counted output video
The final processed video will show detected walnuts with bounding boxes and the total count.

## Example Output
The processed output video with detection and counting is available in:
videos/counted_output.mp4

## Limitations
Small or partially occluded walnuts may not always be detected.
Dense clusters of walnuts can make detection more challenging.
Detection accuracy depends on the diversity and size of the training dataset.

## Future Improvements
Increase dataset size for better detection robustness
Use higher resolution inference for small objects
Replace SORT with ByteTrack for improved tracking stability
Optimize performance for real-time processing

## Applications
This type of system can be used for:

Agricultural fruit counting
Crop yield estimation
Automated orchard monitoring
Smart farming systems

## Technologies Used
Python
YOLO (Ultralytics)
OpenCV
SORT Tracker
Google Colab
NumPy

## License
This project is provided for educational and research purposes

