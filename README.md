# 🎯 2D Object Tracker & Trajectory Analyzer

![Language](https://img.shields.io/badge/Language-Python-blue.svg)
![Computer Vision](https://img.shields.io/badge/Domain-Computer%20Vision-orange.svg)
![Algorithm](https://img.shields.io/badge/Algorithm-Template%20Matching-success.svg)

## 📌 Overview
This is a Computer Vision project that implements **Template Matching** via **2D Cross-Correlation**. It allows users to manually select a Region of Interest (ROI) on the first frame of a video, automatically tracks the target object's position throughout the remaining frames, and visualizes its movement trajectory.

## 🚀 Key Features
* **Interactive ROI Selection:** Users can draw a bounding box to select the target object directly on the first frame using `matplotlib.widgets`.
* **Robust Tracking Algorithm:** Utilizes `scipy.signal.correlate2d` with zero-mean normalization to maintain tracking stability even under varying lighting conditions.
* **Comprehensive Data Extraction:**
    * Exports individual frames with bounding boxes and center coordinates.
    * Plots and saves a 2D Trajectory Map of the object's movement.
    * Automatically compiles the processed frames into a final output video (.mp4) using `moviepy`.

## 🛠️ Tech Stack & Libraries
* **Numpy & SciPy:** Image matrix operations and 2D cross-correlation calculations.
* **Matplotlib:** Trajectory plotting and interactive ROI selection GUI.
* **Pillow (PIL):** Image processing, bounding box rendering, and text overlays.
* **MoviePy:** Original video frame extraction and final result rendering.
