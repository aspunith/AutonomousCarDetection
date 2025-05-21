# Autonomous Driving - Car Detection

This project demonstrates object detection using the YOLO (You Only Look Once) model. The notebook implements various techniques for detecting objects in images, specifically focusing on car detection.

## Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [YOLO Model Overview](#yolo-model-overview)
    - [Model Details](#model-details)
    - [Filtering with a Threshold on Class Scores](#filtering-with-threshold)
    - [Non-max Suppression](#non-max-suppression)
    - [YOLO Non-max Suppression](#yolo-non-max-suppression)
    - [Wrapping Up the Filtering](#wrapping-up-filtering)
4. [Testing YOLO Pre-trained Model](#testing-yolo)
    - [Defining Classes, Anchors, and Image Shape](#defining-classes)
    - [Loading a Pre-trained Model](#loading-model)
    - [Converting Model Output to Bounding Box Tensors](#converting-output)
    - [Filtering Boxes](#filtering-boxes)
    - [Running YOLO on an Image](#running-yolo)
5. [Summary](#summary)
6. [References](#references)

---

## 1. Introduction <a name="introduction"></a>
This project is part of a programming assignment to implement object detection using the YOLO model. The techniques and ideas are inspired by the YOLO papers:
- [Redmon et al., 2016](https://arxiv.org/abs/1506.02640)
- [Redmon and Farhadi, 2016](https://arxiv.org/abs/1612.08242)

### Key Objectives:
- Detect objects in a car detection dataset.
- Implement non-max suppression for accuracy improvement.
- Handle bounding boxes for image annotation.

---

## 2. Problem Statement <a name="problem-statement"></a>
The goal is to build an object detector capable of identifying cars in images using the YOLO model. The project involves implementing various components of the YOLO pipeline, including filtering, non-max suppression, and bounding box handling.

---

## 3. YOLO Model Overview <a name="yolo-model-overview"></a>
### 3.1 Model Details <a name="model-details"></a>
The YOLO model divides an image into a grid and predicts bounding boxes and class probabilities for each grid cell.

### 3.2 Filtering with a Threshold on Class Scores <a name="filtering-with-threshold"></a>
This step involves filtering out predictions with low confidence scores.

### 3.3 Non-max Suppression <a name="non-max-suppression"></a>
Non-max suppression is used to eliminate redundant bounding boxes for the same object.

### 3.4 YOLO Non-max Suppression <a name="yolo-non-max-suppression"></a>
Combines filtering and non-max suppression to refine predictions.

### 3.5 Wrapping Up the Filtering <a name="wrapping-up-filtering"></a>
Finalizes the filtering process to produce usable bounding boxes.

---

## 4. Testing YOLO Pre-trained Model <a name="testing-yolo"></a>
### 4.1 Defining Classes, Anchors, and Image Shape <a name="defining-classes"></a>
Defines the classes, anchor boxes, and image dimensions for the YOLO model.

### 4.2 Loading a Pre-trained Model <a name="loading-model"></a>
Loads a pre-trained YOLO model for inference.

### 4.3 Converting Model Output to Bounding Box Tensors <a name="converting-output"></a>
Processes the model's raw output into bounding box tensors.

### 4.4 Filtering Boxes <a name="filtering-boxes"></a>
Applies filtering to remove low-confidence predictions.

### 4.5 Running YOLO on an Image <a name="running-yolo"></a>
Runs the YOLO model on a sample image to detect objects.

---

## 5. Summary <a name="summary"></a>
This project demonstrates the implementation of the YOLO model for car detection, covering key concepts like filtering, non-max suppression, and bounding box handling.

---

## 6. References <a name="references"></a>
- [YOLO: You Only Look Once](https://arxiv.org/abs/1506.02640)
- [YOLOv2: Better, Faster, Stronger](https://arxiv.org/abs/1612.08242)

---