# CNN-MNIST Handwritten Digit Classification

A Convolutional Neural Network (CNN) implementation using TensorFlow/Keras for classifying handwritten digits from the MNIST dataset.

## Overview

This project demonstrates a deep learning approach to handwritten digit recognition, achieving **99.26% accuracy** on the MNIST test dataset. The model successfully predicts all custom test images.

## Model Performance

- **Training Accuracy:** 99.96%
- **Test Accuracy:** 99.26%
- **Test Loss:** 0.1015

## Model Architecture

```
Sequential CNN Model:
- Conv2D (32 filters, 3x3 kernel) + ReLU
- MaxPooling2D (2x2)
- Conv2D (64 filters, 3x3 kernel) + ReLU
- MaxPooling2D (2x2)
- Flatten
- Dense (128 units) + ReLU
- Dense (10 units, output)

Total Parameters: 421,642
```

## Requirements

- Python 3.7+
- TensorFlow 2.10+
- TensorFlow Datasets 4.6+
- NumPy
- Matplotlib
- OpenCV (cv2)
- Jupyter Notebook

Install all dependencies:
```bash
pip install -r requirements.txt
```

## Dataset

The MNIST dataset contains:
- **Training samples:** 60,000
- **Test samples:** 10,000
- **Image size:** 28x28 grayscale pixels
- **Classes:** 10 (digits 0-9)

The dataset is automatically downloaded via TensorFlow Datasets on first run.

## Usage

### Running the Notebook

1. Clone this repository:
```bash
git clone https://github.com/Kandil7/CNN-MNIST-Handwritten-Digit-Classification.git
cd CNN-MNIST-Handwritten-Digit-Classification
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook "CNN MNIST Classification.ipynb"
```

4. Run all cells sequentially to:
   - Load and explore the MNIST dataset
   - Build the CNN model
   - Train for 10 epochs (~13 minutes)
   - Evaluate on test set
   - Test on custom digit images

### Using the Trained Model

The notebook includes functionality to:
- Save the trained model (`mnist_cnn_model.h5`)
- Load and reuse the model for predictions
- Test on custom 28x28 grayscale PNG images

## Training Details

- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **Batch Size:** 32
- **Epochs:** 10
- **Training Time:** ~13 minutes (on standard CPU)

## Custom Image Prediction

The repository includes 5 test images:
- `cv.png` - Digit 0 ✓
- `cv2.png` - Digit 2 ✓
- `cv4.png` - Digit 4 ✓
- `cv6.png` - Digit 6 ✓
- `cv7.png` - Digit 7 ✓

All custom images are correctly predicted by the model.

## Project Structure

```
.
├── CNN MNIST Classification.ipynb    # Main implementation notebook
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── .gitignore                         # Git ignore file
├── cv.png                             # Test image (digit 0)
├── cv2.png                            # Test image (digit 2)
├── cv4.png                            # Test image (digit 4)
├── cv6.png                            # Test image (digit 6)
└── cv7.png                            # Test image (digit 7)
```

## Results

The model achieves excellent performance on both the standard MNIST test set and custom handwritten digit images, demonstrating strong generalization capabilities.

**Test Set Results:**
- Accuracy: 99.26%
- Loss: 0.1015

**Custom Image Results:**
- 5/5 correctly predicted (100%)

## Future Improvements

- Add data augmentation
- Implement batch normalization and dropout
- Add early stopping and learning rate scheduling
- Create confusion matrix and per-class metrics
- Refactor into Python modules for production use
- Add unit tests

## License

This project is available for educational purposes.

## Acknowledgments

- MNIST dataset: Yann LeCun, Corinna Cortes, and Christopher J.C. Burges
- TensorFlow/Keras framework
