# Mars Terrain Semantic Segmentation

This project tackles a **semantic segmentation task on Mars surface images**, aiming to classify each pixel into one of multiple terrain categories.

The solution is based on a **deep learning pipeline** built with convolutional neural networks, including data preprocessing, augmentation, training, and evaluation.

---

## Overview

Semantic segmentation is a fundamental problem in computer vision where each pixel in an image is assigned a class label.

In this project:
- input: grayscale Mars surface images  
- output: pixel-wise classification into terrain classes  
- goal: maximize segmentation accuracy (Mean IoU)  

The project was developed as part of a course challenge with a hidden test set evaluated via a Kaggle-style competition.

---

## Approach

The pipeline includes:

- **Data preprocessing**
  - normalization of grayscale images  
  - handling low-quality inputs  

- **Data augmentation**
  - brightness and contrast variations  
  - horizontal flips  
  - geometric transformations  

- **Model architecture**
  - U-Net–style convolutional neural network  
  - encoder-decoder structure  
  - attention mechanisms for improved feature selection  

- **Training**
  - loss: sparse categorical cross-entropy  
  - learning rate scheduling  
  - validation monitoring  

- **Evaluation**
  - Mean Intersection over Union (Mean IoU)  
  - qualitative inspection of predictions  

---

## Results

The model successfully learns meaningful terrain segmentation despite:
- low-resolution images  
- noisy labels  
- limited dataset size  

### Example Predictions

<p align="center">
  <img src="results/prediction_example_1.png" width="300"/>
  <img src="results/prediction_example_2.png" width="300"/>
</p>

*(Add your prediction images here if available)*

---

## Repository Structure

```text
mars-segmentation/
├── README.md
├── LICENSE
├── .gitignore
├── notebooks/
│   └── segmentation.ipynb
├── src/                  # optional (if you extract code later)
├── results/
│   ├── predictions/
│   ├── metrics/
│   └── plots/
└── docs/
    └── report.pdf

## Dataset

The dataset used in this project consists of Mars surface images provided as part of a university course assignment.

Due to licensing restrictions, the dataset is not included in this repository.

## Credits

This project is based on starter code provided by Alberto Archetti, licensed under the Apache License 2.0.

The original code has been significantly modified and extended for this project.

This project has been done in collaboration with Luis Felipe Realpe. 

## Key Learnings
- Designing segmentation models for low-quality data
- Handling noisy labels and class imbalance
- Improving performance with data augmentation
- Evaluating models using Mean IoU
- Iterating on architectures and training strategies

## Future Improvements
- Hyperparameter tuning
- Advanced architectures (e.g. DeepLab, transformers)
- Better handling of class imbalance
- Post-processing techniques for smoother predictions