# Face-Detection

## Overview
This project focuses on distinguishing real images from fake ones within a dataset using the concept of disparity maps. The method involves comparing standard deviations between disparity maps of real and fake images, with a focus on the non-planar nature of human faces.

## Method
Utilized a HAAR Cascade Object Detection to isolate faces in images.
Generated three sets of disparity maps for each group of images (left, center, right) for both real and fake datasets.
Calculated standard deviation for each disparity map and compared them to identify real images with higher standard deviation.

## Implementation
Detected faces using a HAAR Cascade, creating separate lists for real and fake datasets.
Ensured all image faces were isolated, replacing empty arrays with values from other images in the group.
Calculated disparity maps using SIFT and Lowe’s Matching method, iterating through variations (left, right, center).
Compared standard deviations to classify images as real or fake.

## Experimentation
Tested on provided dataset with a Confusion Matrix of:
True Negative (TN): 6
False Positive (FP): 6
False Negative (FN): 6
True Positive (TP): 6
Precision: 0.5, Recall: 0.5.
