# Image Classification Notebook

## Overview
This repository contains a Jupyter notebook for training and evaluating an image classification model.
It is implemented in **TensorFlow/Keras**.
The architecture used is a **Custom CNN**.
Training is configured for 20 epochs with a batch size of 32.

## Features
- Image data loading and preprocessing
- Custom CNN model for classification
- Training and evaluation with accuracy and loss tracking
- Easily adjustable hyperparameters
- Compatible with transfer learning extensions

## Dataset
The notebook expects an image dataset organized in classification folders:

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

Detected dataset path:
- `data`

## Setup
Requires Python 3.9+ and the following packages:
```
imghdr
matplotlib
numpy
opencv-python
os
tensorflow
```

Install with:
```bash
pip install imghdr matplotlib numpy opencv-python tensorflow
```

## Usage
1. Create and activate a virtual environment.
2. Install dependencies.
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open `img_classification.ipynb`.
5. Update dataset paths in the notebook.
6. Run all cells to train and evaluate the model.

## Configuration
- `BATCH_SIZE` = 32
- `EPOCHS` = 20

## Results
| Metric | Value |
|---|---|
| Epochs | 20 |
| Train Accuracy | 0.9844 |
| Train Loss | 0.0128 |

![Accuracy Curve](/mnt/data/accuracy_curve.png)

![Loss Curve](/mnt/data/loss_curve.png)
