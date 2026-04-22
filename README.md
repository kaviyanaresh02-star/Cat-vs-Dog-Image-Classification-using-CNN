# Cat vs Dog Image Classification using CNN

## Overview

This project implements a Convolutional Neural Network (CNN) for binary image classification to distinguish between images of cats and dogs. The model is built using TensorFlow and Keras, trained on a dataset of cat and dog images, and can predict whether a given image contains a cat or a dog.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Prediction](#prediction)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Features

- Binary classification of cat and dog images
- CNN model with multiple convolutional and pooling layers
- Data preprocessing including normalization
- Training and validation on separate datasets
- Prediction on new images
- Visualization of training history (if implemented)

## Requirements

- Python 3.7+
- TensorFlow 2.x
- Keras (included in TensorFlow)
- Matplotlib (for visualization)
- NumPy
- Pillow (for image processing)

## Dataset

The project uses a dataset of cat and dog images, typically organized into 	rain and 	est directories with subdirectories for each class (cats and dogs).

- **Source**: The dataset is expected to be in a ZIP file (e.g., rchive (17).zip).
- **Structure**:
  `
  data/
  ├── train/
  │   ├── cats/
  │   └── dogs/
  └── test/
      ├── cats/
      └── dogs/
  `
- **Image Size**: Images are resized to 128x128 pixels.
- **Note**: The dataset paths in the notebook are set for Google Colab environment. Adjust paths if running locally.

## Installation

1. Clone or download this repository.
2. Install the required dependencies:
   `
   pip install tensorflow matplotlib numpy pillow
   `
3. Ensure you have the dataset ZIP file and update the paths in the notebook accordingly.

## Usage

1. Open the Jupyter notebook Cat vs Dog Image Classification using CNN.ipynb.
2. Run the cells in order:
   - Import libraries
   - Extract the dataset
   - Load and preprocess data
   - Define and compile the model
   - Train the model
   - Make predictions on sample images

### Running in Google Colab

The notebook is designed to run in Google Colab. Upload the notebook and dataset to Colab for execution.

### Running Locally

- Update file paths to local directories.
- Ensure GPU support if available for faster training.

## Model Architecture

The CNN model consists of:

- **Input Layer**: 128x128x3 images
- **Conv2D Layer 1**: 32 filters, 3x3 kernel, ReLU activation
- **MaxPooling2D Layer 1**: 2x2 pool size
- **Conv2D Layer 2**: 64 filters, 3x3 kernel, ReLU activation
- **MaxPooling2D Layer 2**: 2x2 pool size
- **Conv2D Layer 3**: 128 filters, 3x3 kernel, ReLU activation
- **MaxPooling2D Layer 3**: 2x2 pool size
- **Flatten Layer**
- **Dense Layer 1**: 128 units, ReLU activation
- **Output Layer**: 1 unit, Sigmoid activation (for binary classification)

## Training

- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Metrics**: Accuracy
- **Epochs**: 25
- **Batch Size**: 32
- **Validation**: Performed on test dataset

The model is trained using model.fit() with training and validation data.

## Evaluation

After training, evaluate the model's performance on the test dataset. The notebook includes training history which can be used to plot accuracy and loss curves.

## Prediction

The notebook demonstrates predictions on sample images:

- Load an image using Keras preprocessing
- Preprocess the image (resize, normalize)
- Use model.predict() to get prediction
- Interpret result: >0.5 for Dog, <=0.5 for Cat

Example images used: download (6).jpg, download (3).jpg, download (11).jpg, images (2).jpg

## Results

- **Training Accuracy**: Varies based on dataset and epochs
- **Validation Accuracy**: Varies
- The model achieves reasonable accuracy for cat vs dog classification after training.

(Note: Actual results depend on the dataset quality and training parameters.)

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Dataset source: [Mention if known, e.g., Kaggle Cats and Dogs dataset]
- Inspired by various CNN tutorials for image classification

## Contact

For questions or feedback, please open an issue in the repository.
