# Water Pollution Visual Classification Model

## Project Overview

This project develops a deep learning-based visual classification model to identify whether water images are clean or polluted. The project is part of Machine Learning Project Phase II and focuses on environmental monitoring using Convolutional Neural Networks and transfer learning.

## Dataset

Dataset Name: Water Pollution Classification Dataset  
Dataset Source: Kaggle  
Dataset Link: https://www.kaggle.com/datasets/ferix01/water-pollution-classification-dataset

## Dataset Description

The dataset contains RGB water images organized into two classes:

| Class | Number of Images |
|---|---:|
| Clean | 147 |
| Polluted | 154 |

Total Images: 301  
Number of Classes: 2  
Image Type: RGB colour images  
Task: Binary image classification

## Objective

The objective of this project is to classify water images into clean or polluted categories using deep learning. This can support automated environmental monitoring by reducing dependency on manual inspection.

## Methodology

The project follows these steps:

1. Dataset loading from Kaggle
2. Image resizing to 224 × 224 pixels
3. Train, validation, and test split
4. Image normalization
5. Data augmentation
6. Custom CNN model development
7. MobileNetV2 transfer learning model
8. Model training
9. Model evaluation
10. Model comparison

## Data Augmentation

The following augmentation techniques were applied:

- Random horizontal flip
- Random rotation
- Random zoom
- Random contrast adjustment

## Models Used

### Custom CNN

A custom CNN model was built from scratch using convolutional layers, max pooling layers, dense layers, dropout, and sigmoid activation for binary classification.

### MobileNetV2

MobileNetV2 was used as a transfer learning model with pretrained ImageNet weights. The base model was frozen, and custom classification layers were added for clean and polluted water classification.

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Loss
- Precision
- Recall
- F1-score
- Confusion matrix
- Classification report

## Results

| Model | Test Accuracy | Test Loss |
|---|---:|---:|
| Custom CNN | 62.50% | 0.6031 |
| MobileNetV2 | 96.00% | 0.2108 |

MobileNetV2 achieved the best performance and significantly outperformed the custom CNN model.

## MobileNetV2 Classification Report

| Class | Precision | Recall | F1-score | Support |
|---|---:|---:|---:|---:|
| Clean | 0.96 | 0.96 | 0.96 | 25 |
| Polluted | 0.96 | 0.96 | 0.96 | 23 |

Overall Accuracy: 96%

## Research Questions

1. Can a custom CNN model classify water images as polluted or clean?
2. Does MobileNetV2 perform better than a custom CNN on a small dataset?
3. Can data augmentation improve model generalization?
4. Which evaluation metrics best explain model performance?
5. What are the limitations of deep learning when training data is limited?

## Output Files

The repository includes the following output files:

- cnn_accuracy_curve.png
- cnn_loss_curve.png
- cnn_confusion_matrix.png
- mobilenet_accuracy_curve.png
- mobilenet_loss_curve.png
- mobilenet_confusion_matrix.png
- model_comparison.png

## Instructions for Running the Code

### Run on Kaggle (Recommended)

1. Go to Kaggle and sign in to your account.
2. Click **Create → New Notebook**.
3. Upload the file `cnn-based-water-pollution-classification.ipynb`.
4. Click **Add Data** on the right-side panel.
5. Search for **Water Pollution Classification Dataset** by **ferix01**.
6. Add the dataset to the notebook.
7. Enable GPU acceleration:
   - Click **Settings**
   - Select **Accelerator**
   - Choose **GPU T4**
8. Click **Run All** to execute all notebook cells in sequence.
9. Wait for the training process to complete.
10. The notebook will automatically generate:
    - CNN Accuracy Curve
    - CNN Loss Curve
    - CNN Confusion Matrix
    - MobileNetV2 Accuracy Curve
    - MobileNetV2 Loss Curve
    - MobileNetV2 Confusion Matrix
    - Model Comparison Table
11. Review the final evaluation metrics and output figures.

