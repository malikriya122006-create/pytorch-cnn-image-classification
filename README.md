# CNN Image Classification using PyTorch

A deep learning project implementing a Convolutional Neural Network (CNN) from scratch using PyTorch to classify images from the CIFAR-10 dataset.

## Overview

This project explores image classification using a custom-built CNN architecture. The model is trained on the CIFAR-10 dataset to classify images into 10 different categories.

The complete implementation is provided in a Jupyter Notebook.

## Dataset

**CIFAR-10**

- 60,000 colour images
- 10 image classes
- 50,000 training images
- 10,000 testing images
- Image dimensions: 32 × 32 pixels

The dataset is downloaded automatically using Torchvision.

## Tech Stack

- Python
- PyTorch
- Torchvision
- Jupyter Notebook

## Implementation

### 1. Data Preprocessing
- Loaded CIFAR-10 using Torchvision.
- Converted images into tensors.
- Applied image normalization using a mean and standard deviation of 0.5 for each RGB channel.

### 2. Data Loading
- Used PyTorch DataLoaders.
- Set batch size to 64.
- Enabled shuffling for the training dataset.

### 3. CNN Architecture

Designed and implemented a CNN from scratch using `torch.nn.Module`.

| Layer | Configuration |
|---|---|
| Convolutional Layer 1 | 3 → 32 filters |
| Convolutional Layer 2 | 32 → 64 filters |
| Convolutional Layer 3 | 64 → 128 filters |
| Activation | ReLU |
| Pooling | Max Pooling (2 × 2) |
| Fully Connected Layer | 2048 → 256 |
| Output Layer | 256 → 10 |

### 4. Model Training
- Loss Function: Cross Entropy Loss
- Optimizer: Adam
- Training Epochs: 10
- Used backpropagation and gradient descent to update model parameters.

### 5. Model Evaluation
- Evaluated the trained model on the test dataset.
- Used `model.eval()` and `torch.no_grad()` during evaluation.
- Calculated classification accuracy by comparing predicted labels with actual labels.

## Project Structure

```text
pytorch-cnn-image-classification/
│
├── CNN_CIFAR10.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/malikriya122006-create/pytorch-cnn-image-classification.git
```

Navigate to the project directory:

```bash
cd pytorch-cnn-image-classification
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook CNN_CIFAR10.ipynb
```

Run the notebook cells. The CIFAR-10 dataset will be downloaded automatically when the dataset-loading cells are executed.

## Learning Outcomes

- Understanding CNN architecture and feature extraction.
- Implementing convolutional and pooling layers using PyTorch.
- Understanding forward propagation and backpropagation.
- Training deep learning models.
- Evaluating image classification models.