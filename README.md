
# Intrusion Detection using Deep Learning in IoT-based Smart Healthcare
MS Computer Science thesis project, National University of Modern Languages (NUML), Islamabad, 2023
Supervisor: Dr. Sajjad Haider

## Overview
IoT-based smart healthcare systems connect sensors and medical devices to software applications, which makes them an easy target for intruders. This project proposes a **hybrid intrusion detection model** that combines **Random Forest (RF), Support Vector Machine (SVM), Long Short-Term Memory (LSTM) and a Gradient Boosting (GB) classifier**. The model is built to generalize well by handling overfitting and underfitting, and it is compared with state-of-the-art schemes.

## Dataset
[MQTT-IoT-IDS 2020](https://ieee-dataport.org/open-access/mqtt-iot-ids2020-mqtt-internet-things-intrusion-detection-dataset) with 5 classes: normal, MQTT brute force, scan A, scan sU and Sparta (SSH brute force).
The dataset is not included in this repository.

## Approach
1. Data reading and cleaning (missing-value handling)
2. New feature generation (same-subnet vs different-subnet traffic from source and destination IPs)
3. Label encoding of features and one-hot encoding of attack classes
4. Min-Max normalization
5. Train/test split (70% / 30%)
6. Hyperparameter tuning for the base learners (RF, SVM, LSTM)
7. Hybridization: base-model predictions are combined and classified by Gradient Boosting
8. Evaluation and comparison with benchmark models (SVM, LR, DNN, RNN)

## Proposed Model
![Proposed model architecture](images/architecture.png)

## Results
| Metric | Training | Testing |
|--------|----------|---------|
| Accuracy | 98.89% | 99.8% |
| Precision | 99.87% | 99.83% |
| Recall | 98.99% | 98.98% |
| F1-Score | 98.71% | 98.67% |

**Confusion matrix (test set)**

![Confusion matrix](images/confusion_matrix.png)

**Training and validation loss**

![Training loss](images/training_loss.png)

**Top 10 important features**

![Feature importance](images/feature_importance.png)

## Tech Stack
Python, TensorFlow / Keras, scikit-learn, pandas, NumPy

## Status
Research paper in preparation. Source code and detailed methodology will be released after publication.

## Author
**Ana Shahid**
MS Computer Science, NUML Islamabad
[LinkedIn](https://www.linkedin.com/in/your-profile) | ana.shahid@numl.edu.pk
