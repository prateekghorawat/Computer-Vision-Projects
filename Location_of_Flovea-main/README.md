# Location_of_Flovea
I explored the exciting world of computer vision and deep learning to tackle the task of locating a single object within an image. Single-object detection is a crucial problem in various domains, from autonomous vehicles to surveillance systems and more.

# Single-Object Detection with PyTorch

## Data Exploration
- **Loading Data:** The project begins by loading the dataset from a file named "Fovea_location.xlsx" on Kaggle. This file contains information about images and their corresponding object locations.

- **Data Visualization:** The data is visualized using matpllot to create a scatter plot of object locations in the images.

- **Data Transformation:** The code further explores the dataset by analyzing the dimensions (height and width) of the images.

## Data Transformation for Object Detection
- **Resizing Images:** A function is defined to resize images and their corresponding labels, ensuring they have the same target size.

- **Data Augmentation:** Functions for random horizontal and vertical flips, as well as random shifts, are provided for data augmentation, enhancing the model's robustness.

## Custom Datasets
- **Creating Custom Datasets:** A custom dataset class called AMD_dataset is introduced for object detection. This class loads and transforms the data according to the defined transformations and parameters.

- **Dataset Splitting:** The dataset is split into training and validation subsets using techniques like shuffle split.

- **Data Loading:** Data loaders are set up for the training and validation subsets to facilitate model training and evaluation.

## Model Creation
- **Defining the Model:** A custom neural network model for object detection is defined. The model architecture includes convolutional layers for feature extraction and a fully connected layer for predicting the object's location.

## Loss, Optimizer, and Metric
- **Loss Function:** The project utilizes a Smooth L1 Loss function to optimize the model.

- **Optimizer:** The Adam optimizer is employed for training the model.

- **Learning Rate Scheduling:** Learning rate scheduling is used to adjust the learning rate during training.

- **Metric Calculation:** Intersection over Union (IOU) is calculated as a metric for object detection accuracy.

## Training and Evaluation
- **Training and Validation Loop:** A training and validation loop is defined, including functions to compute loss and metrics for both training and validation datasets.

- **Best Model Saving:** The best model weights are saved during training for future use.

- **Training and Validation Progress:** The training and validation loss and accuracy are visualized over epochs.
