# Robust Multimodal Vehicle Detection in Foggy Weather

**CSC490H5 — StormSight**

This project investigates robust vehicle detection under adverse weather conditions, with a focus on foggy environments. We build upon **MVDNet (Multimodal Vehicle Detection Network)**, which combines LiDAR and radar information to improve vehicle detection when visibility is degraded.

## Team

* Madeeha Khan
* Mahak Mishra
* Samaah Abdullah

## Problem

Vehicle detection becomes more challenging in adverse weather conditions such as fog because environmental conditions can reduce the quality and reliability of sensor observations.

Our project focuses on multimodal vehicle detection using **LiDAR and radar**. We are interested in whether sensor fusion can improve robustness when one of the sensors contains noisy data or becomes partially unavailable.

## Baseline

Our primary baseline is:

**Robust Multimodal Vehicle Detection in Foggy Weather Using Complementary LiDAR and Radar Signals (MVDNet)**

**Paper:**
https://openaccess.thecvf.com/content/CVPR2021/papers/Qian_Robust_Multimodal_Vehicle_Detection_in_Foggy_Weather_Using_Complementary_Lidar_CVPR_2021_paper.pdf

**Original implementation:**
https://github.com/qiank10/MVDNet

## Dataset

We plan to use the **Oxford Radar RobotCar Dataset**, which contains synchronized radar and other sensor data collected from a vehicle operating in different weather and traffic conditions.

**Dataset website:**
https://oxford-robotics-institute.github.io/radar-robotcar-dataset/

## Proposed Improvements

We will investigate the robustness of multimodal vehicle detection by introducing controlled sensor degradation.

Our experiments will focus on:

### 1. Missing or Noisy Sensor Data

* Simulate situations where one sensor is unavailable or its measurements are corrupted.
* Evaluate how detection performance changes under different levels of degradation.

### 2. Different Fusion Strategies

* Compare different ways of combining LiDAR and radar information.
* Determine whether alternative fusion strategies improve robustness.

### 3. Modified Loss/Cost Functions

* Investigate whether changing the training objective can improve detection performance when sensor inputs are unreliable.

## Evaluation

We will primarily use **Average Precision (AP)** and, where applicable, **mean Average Precision (mAP)** to evaluate vehicle detection performance.

We will compare:

* LiDAR-only detection
* Radar-only detection
* Multimodal LiDAR + radar detection
* Multimodal detection with noisy sensor inputs
* Multimodal detection with missing sensor inputs

The change in AP across these conditions will be used to measure the robustness of the system.

## Repository Structure

The repository will contain the implementation of the baseline model, our proposed modifications, experiment configurations, and documentation.

```text
robust-multimodal-vehicle-detection/
│
├── README.md
├── data/
├── models/
├── configs/
├── scripts/
├── experiments/
└── results/
```

The exact structure may change as development progresses.

## References

Qian, K., Zhu, S., Zhang, X., & Li, L. E. (2021). *Robust Multimodal Vehicle Detection in Foggy Weather Using Complementary LiDAR and Radar Signals*. Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR).

Oxford Radar RobotCar Dataset:
https://oxford-robotics-institute.github.io/radar-robotcar-dataset/
