# Automated Mechanical Surface Inspection

Computer vision and deep learning project for automated classification of
steel surface defects using image processing and a CNN.

## Project Overview

The system processes mechanical surface images and classifies them into
six surface-defect categories.

### Pipeline

Camera / Surface Image
        ↓
OpenCV Preprocessing
        ↓
CLAHE Contrast Enhancement
        ↓
Gaussian Filtering
        ↓
Canny Edge Detection
        ↓
2-Channel CNN
        ↓
Defect Classification
        ↓
Performance Evaluation

## Defect Classes

- Crazing
- Inclusion
- Patches
- Pitted Surface
- Rolled-in Scale
- Scratches

## Technologies

- Python
- OpenCV
- PyTorch
- NumPy
- Pandas
- Scikit-learn
- Matplotlib
- Convolutional Neural Networks (CNN)

## Running the Project

### Google Colab

1. Open `Automated_Mechanical_Surface_Inspection.ipynb`.
2. Upload the notebook to Google Colab.
3. Select:

   `Runtime → Change runtime type → T4 GPU`

4. Run all cells from top to bottom.

The notebook automatically:

- Downloads the NEU Surface Defect Dataset.
- Extracts and prepares the images.
- Applies OpenCV preprocessing.
- Splits the dataset into training, validation, and test sets.
- Trains the CNN using PyTorch.
- Evaluates the trained model.
- Generates accuracy, precision, recall and F1-score.
- Generates the confusion matrix.
- Runs automated inspection on test images.
- Saves the trained model as:

  `models/surface_inspection_cnn.pth`

No dataset needs to be manually downloaded.

## Running Locally in VS Code

Install Python and create a virtual environment if required.

Install the dependencies:

```bash
pip install torch torchvision opencv-python numpy pandas matplotlib scikit-learn jupyter