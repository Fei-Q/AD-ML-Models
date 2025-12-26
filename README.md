# AD MRI CNN Classifier (TensorFlow)

A lightweight convolutional neural network (CNN) trained to classify preprocessed brain MRI images into 4 classes.

## Test Results
- **Accuracy:** 0.968
- **Macro F1:** 0.964

See `figures/` for training curves and the test confusion matrix.

## Dataset
This project uses a preprocessed MRI dataset from Kaggle provided by Hack4Health for a Hackathon.
The dataset itself is not included in this repository.

## Approach
- **Model:** simple CNN (2 convolutional layers, 2 pooling layers, 1 hidden dense layer, softmax classifier)
- **Loss:** Sparse categorical cross-entropy (class-weighted)
- **Train/Val Split:** stratified 80/20 split from the provided training set
- **Class Imbalance:** handled using class-weighted loss
- **Evaluation:** confusion matrix + per-class precision/recall/F1

## Files
- `ad_mri.ipynb`: end-to-end training + evaluation notebook
- `AD_mri_cnn_classifier.keras`: saved model (Keras format)
- figures: accuracy/loss curves and confusion matrix
