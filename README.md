# Kaggle Recursion Cellular Image Classification Challenge

The competition has an objective of image classification in experimantal noise of biological signals. Here the proposed algorithms detects different genetic perturbations.

## Hardware/ Software
- GPU: 1xTesla K80
- PyTorch, albumentations

## Training
As the cellular images have origin from 4 types of experiments (HEPG2, HUVEC, RPE, U2OS) we have trained 4 different models in parallel for each experiment and then concatenated the predictions.

## Solution
The solution represents:
- models: 
  - EfficientNet-B0
- augmentations: 
  - [Albumentations](https://github.com/albu/albumentations) library 
  - Rotate90, HorizontalFlip, Brightness, Contrast, ColorJitter
- optimizer: Adam
- loss: CrossEntropyLoss
- batch size: 16

