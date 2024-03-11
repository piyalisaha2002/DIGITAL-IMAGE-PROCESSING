# Lane Detection using Digital Image Processing

Lane detection is a crucial technology for enabling autonomous navigation in vehicles. This project demonstrates a lane detection system implemented using digital image processing techniques, specifically designed for cars equipped with front-facing cameras. This system, a part of Advanced Driver Assistance Systems (ADAS), detects lane markings, measures curve radius, and monitors the vehicle's offset from the center, significantly improving safety and comfort for drivers.

## Overview

Lane detection systems are traditionally designed for roads with clear lane markings. However, this project focuses on detecting lanes on unmarked roads, presenting an improved approach using digital image processing techniques.

## Features

- Detects lane lines on unmarked roads.
- Measures curve radius and monitors vehicle offset from the center.
- Utilizes front-facing camera footage for real-time analysis.
- Improves safety and comfort for drivers.

## Methodology

The project follows a pipeline structure for implementation:

1. **Image Processing**: 
   - Applies HSL color selection to isolate white and yellow lane lines.
   - Utilizes Canny Edge detection for edge detection.
   - Implements region of interest to focus on the area facing the camera.

2. **Lane Detection & Curve Fitting**:
   - Plots a histogram to identify the starting points of left and right lanes.
   - Uses sliding window and general search approaches for lane detection.
   - Performs second-degree polynomial fitting for curve fitting.

3. **Visualization and Main Function**:
   - Visualizes detected lanes and other information on the final image.
   - Calculates vehicle offset and displays it in meter space.
   - Adds text to the final image for information display.

## Usage

1. **readVideo()**: Accesses the video file located in the same directory.
2. **processImage()**: Performs processing techniques to isolate lane lines.
3. **perspectiveWarp()**: Applies perspective warp for a bird's eye view of the lanes.
4. **draw_lane_lines()**: Visualizes detected lanes on the final image.
5. **offCenter()**: Calculates and displays the vehicle offset.
6. **addText()**: Adds informative text to the final image.
7. **main()**: Calls all functions in the correct order for video processing.

## Requirements

- Python 3.x
- OpenCV
- NumPy

## Installation

1. Clone the repository:

```
git clone [<repository_url>](https://github.com/piyalisaha2002/Lane-detection-using-digital-image-processing)
```

2. Install dependencies:

```
pip install opencv-python numpy
```

## Running the Project

Execute the main Python script:

```
python laneDetection.py
```
