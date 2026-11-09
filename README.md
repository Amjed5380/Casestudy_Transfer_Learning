
# Transfer Learning for Image Classification

## Project Overview
This project implements image classification using **Transfer Learning with EfficientNetB0**, a pretrained Convolutional Neural Network (CNN). The model is trained on the CIFAR-10 dataset using feature extraction and fine-tuning techniques to achieve improved classification performance.

## Objective
To build a high-performance image classification model using:
- Pretrained CNN (EfficientNetB0)
- Transfer Learning and Fine-Tuning
- Batch Normalization
- L2 Regularization and Dropout
- He Weight Initialization
- Early Stopping
- Learning Rate Scheduling
- GPU Training

## Dataset
**CIFAR-10 Dataset**

The dataset contains 60,000 color images belonging to 10 different classes.

Classes:
- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

## Model Architecture

**EfficientNetB0 → Global Average Pooling → Dense (512) → Batch Normalization → ReLU → Dropout (0.5) → Dense (10, Softmax)**

## Implementation Steps

1. Import required libraries.
2. Load the CIFAR-10 dataset.
3. Perform image preprocessing and resizing.
4. Apply data augmentation.
5. Load pretrained EfficientNetB0.
6. Perform feature extraction by freezing the backbone.
7. Build the custom classification head.
8. Train the model using appropriate callbacks.
9. Perform fine-tuning by unfreezing selected layers.
10. Evaluate the final model.

## Training Configuration

| Parameter | Feature Extraction | Fine-Tuning |
|---|---|---|
| Optimizer | AdamW | AdamW |
| Learning Rate | 0.001 | 0.00001 |
| Batch Size | 16 | 16 |
| Epochs | 20 | 15 |
| Weight Decay | 0.0001 | 0.0001 |

## Results

| Training Phase | Validation Accuracy | Validation Loss |
|---|---:|---:|
| Feature Extraction | 91.04% | 0.3887 |
| Fine-Tuning | 93.60% | 0.2991 |

Fine-tuning improved the validation accuracy by allowing selected pretrained layers to adapt to the CIFAR-10 dataset.

## Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- EfficientNetB0

## Key Learning Outcomes

- Understanding Transfer Learning.
- Implementing Feature Extraction and Fine-Tuning.
- Working with pretrained CNN architectures.
- Applying regularization techniques.
- Improving model generalization.
- Evaluating multi-class image classification models.
