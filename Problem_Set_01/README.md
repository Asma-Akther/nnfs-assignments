# Pneumonia Detection using CNN

## Overview
This project implements a Convolutional Neural Network (CNN) to classify chest X-ray images into two categories:
- Pneumonia
- Normal

The objective is to assist in medical diagnosis by automatically identifying pneumonia from chest X-ray images using deep learning techniques.

---

## Dataset
The dataset consists of 5,863 chest X-ray images categorized into:
- Train
- Validation (val)
- Test

Each folder contains two subcategories:
- Pneumonia
- Normal

These images are anterior-posterior chest X-rays collected from pediatric patients aged one to five years as part of routine clinical care.

---

## Methodology

### Data Preprocessing
- Images resized to 224x224 pixels
- Pixel values normalized using rescaling (1./255)
- Data augmentation techniques applied:
  - Rotation
  - Width and height shifting
  - Zoom
  - Horizontal flipping

---

### Model Architecture
The CNN model consists of:
- Convolutional layers (Conv2D) for feature extraction
- MaxPooling layers for dimensionality reduction
- Flatten layer to convert feature maps into vectors
- Fully connected Dense layers
- Dropout layer to reduce overfitting
- Sigmoid activation function for binary classification

---

### Training Strategy
- Loss Function: Binary Crossentropy
- Optimizer: Adam
- Evaluation Metrics:
  - Accuracy
  - Precision
  - Recall
  - AUC (Area Under Curve)

Additional techniques:
- EarlyStopping to prevent overfitting
- ModelCheckpoint to save the best-performing model

---

## Results

### Model Performance on Test Set

- Loss        : 0.2505  
- Accuracy    : 92.15%  
- Precision   : 92.73%  
- Recall      : 94.87%  
- AUC Score   : 95.82%  

---

### Classification Report

| Class       | Precision | Recall | F1-Score | Support |
|------------|----------|--------|----------|--------|
| Normal     | 0.91     | 0.88   | 0.89     | 234    |
| Pneumonia  | 0.93     | 0.95   | 0.94     | 390    |

---

### Overall Metrics

- Accuracy        : 92%  
- Macro Avg F1    : 0.92  
- Weighted Avg F1 : 0.92  

---

## Analysis

- The model achieves high accuracy and a strong AUC score, indicating excellent classification capability.
- Recall for Pneumonia (94.87%) is particularly high, which is critical in medical diagnosis to minimize false negatives.
- The model performs slightly better on Pneumonia cases compared to Normal cases.
- Balanced precision and recall indicate that the model is not biased toward any single class.

---

## Conclusion

The CNN model successfully classifies chest X-ray images with high accuracy and reliability. Its strong recall for pneumonia cases makes it suitable for assisting in medical diagnosis scenarios.

---

## Future Work

- Implement transfer learning using pre-trained models such as VGG16 or ResNet
- Perform hyperparameter tuning to further improve performance
- Deploy the model as a web application for real-world use
- Use larger and more diverse datasets to improve generalization
