# Image Processing Lab
---
## Overview
This repository contains a comprehensive image processing laboratory covering fundamental computer vision techniques including convolution operations, binarization, morphological operations, feature detection, and shape analysis. The lab demonstrates both manual implementations of core algorithms and optimized OpenCV functions for practical image processing tasks.

![Original Test Image](/imgs/morphNemo.png)
*Original test image used throughout the lab exercises*

## Lab Exercises

### 1. Convolution Operations
Implemented 2D convolution from scratch and applied various kernels for image enhancement:

![Convolution Animation](3D_Convolution_Animation.gif)
*Visualization of the convolution operation showing how kernels slide across images*

**Kernels Applied:**
- **Sharpening**: Enhances image details using a 3×3 sharpen kernel
- **Edge Detection**: Identifies edges using Laplacian-based kernel  
- **Blurring**: Smooths images with averaging kernel

**Key Functions:**
- Custom `convolution2D()` implementation with zero-padding
- Comparison with `scipy.signal.convolve2d()` and `cv2.filter2D()`

---
### 2. Image Binarization & Color Selection

![Binarization Example](/imgs/binAngela.png)
*Binary segmentation result showing threshold-based separation of foreground and background*

- **Grayscale Conversion**: RGB to grayscale using perceptual weights
- **Threshold-based Binarization**: Binary segmentation using intensity thresholds
- **HSV Color Selection**: Isolating specific colors using OpenCV's `inRange()` function

---
### 3. Connected Components Labeling

![Red Mask Results](/imgs/redmasknemo.png)
*Color selection results: original Nemo (left) vs red color mask applied (right)*

- **Object Counting**: Using `cv2.connectedComponents()` to identify distinct regions
- **Red Area Detection**: Applied to `nemo.jpg` to count red-colored regions
- **Noise Reduction**: Morphological operations (opening/closing) to clean binary masks

![Connected Components](/imgs/unprocessedAreaDetection.png)
*Connected components analysis showing 17 distinct red regions detected in Nemo image*

---
### 4. Morphological Operations

![Morphological Cleaning](morphNemo.png)
*Morphological operations for noise removal: original mask (left), after cleaning (middle), final detected areas (right)*

- **Noise Removal**: Used opening (erosion + dilation) and closing (dilation + erosion) to clean binary images
- **Structure Elements**: 3×3 and 15×15 kernels for different noise removal tasks
- **Results**: Reduced red areas from 17 to 6 after morphological cleaning
- 
---
### 5. Feature Detection

**Harris Corner Detection:**

- Implemented corner detection on chessboard images
- Used `cv2.cornerHarris()` with optimal parameter tuning

**Hough Transform:**

![Hough Line Detection](/imgs/propHoughLines.png)
*Probabilistic Hough transform detecting straight lines in chessboard image*

- **Line Detection**: Identified straight lines in chessboard using probabilistic Hough transform
- **Circle Detection**: Detected circular objects (coins) using Hough circle transform

---
### 6. Coin Detection & Analysis

![Coin Processing](/imgs/connectedAreaCoins.png)
*Coin detection pipeline: original image (left), binarized version (middle), connected components result (right)*

![Circle Detection](coins_circle_detection.png)
*Hough circle detection successfully identifying circular coin shapes*

- **Coin Counting**: Automatic detection and counting of coins in `coins.jpg`
- **Binary Segmentation**: Intensity-based thresholding combined with morphological cleaning
- **Component Analysis**: Area-based filtering to distinguish real coins from noise
- **Results**: Detected 7 coins using connected components analysis

---
### 7. Automate Lab1 behaviour using Harris Corner Detection Algorithm
...
...

---

## Technical Implementation

### Libraries
- `OpenCV` - Computer vision functions
- `NumPy` - Numerical computations
- `Matplotlib` - Visualization
- `SciPy` - Signal processing

## Results Summary
The lab successfully demonstrates:
- **Image Filtering**: Effective convolution operations with custom and predefined kernels
- **Object Segmentation**: Robust color-based and intensity-based object isolation
- **Feature Detection**: Accurate corner and line detection in structured images
- **Morphological Processing**: Significant noise reduction through opening/closing operations
- **Practical Applications**: Real-world object counting and geometric analysis

---

## Disclaimer :
This lab serves as a comprehensive introduction to fundamental image processing techniques with practical implementations and real-world applications. All images shown are processed results from the actual laboratory exercises.

