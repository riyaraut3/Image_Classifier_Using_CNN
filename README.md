# Image Classification Notebook

## Overview
This repository contains a Jupyter notebook for training and evaluating an image classification model.

It is implemented in **TensorFlow/Keras**.

The current architecture detected: **Custom CNN**.

Default batch size: **32**.

Default training epochs: **20**.

## Features
- Data loading and preprocessing
- Model definition and training loop
- Evaluation with metrics and plots
- Easily switchable hyperparameters
- Ready to extend with transfer learning

## Dataset
The notebook expects an image dataset organized in typical classification folders, e.g.:

```
DATASET_ROOT/
  train/
    class_a/
    class_b/
  valid/
    class_a/
    class_b/
  test/           # optional
```

Detected dataset path hints in the notebook:

- data


## Setup
Install Python 3.9+ and the following packages:

```
imghdr
matplotlib
numpy
opencv-python
os
tensorflow
```


## Usage
1. Create and activate a virtual environment.
2. Install dependencies listed above.
3. Launch Jupyter and open `img_classification.ipynb`.
4. Update dataset paths inside the notebook to point to your local dataset.
5. Run cells top to bottom to train and evaluate the model.


## Configuration
Key hyperparameters detected:

- `BATCH_SIZE` = 32
- `EPOCHS` = 20
- `loss` = tf.losses.BinaryCrossentropy
- `metrics` = ["accuracy"]

## Notebook Guide
- **Imports & setup**: installs and seeds
- **Data pipeline**: reads images, applies resizing/augmentation
- **Model**: builds a Custom CNN and compiles
- **Training**: fits for 20 epochs with callbacks (if any)
- **Evaluation**: accuracy/loss plots, per-class metrics
- **Inference**: predict on new images

## Results (fill in after you train)
The notebook likely logs accuracy and loss per epoch. Add your final metrics and confusion matrix screenshots here after training.

## Reproducibility
- Seed random generators (NumPy, framework) for consistent runs
- Log exact package versions (`pip freeze > requirements.txt`)
- Capture hardware info (CPU/GPU) if performance matters

## Troubleshooting
- **OOM / CUDA errors**: Lower batch size or image size.
- **Class imbalance**: Consider class weights or augmentation.
- **Poor accuracy**: Verify data directory structure and label mappings; try a pretrained backbone.


---
*Generated automatically from the notebook structure. Review and customize as needed.*
