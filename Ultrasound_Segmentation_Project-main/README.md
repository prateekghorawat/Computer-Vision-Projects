# Ultrasound_Segmentation_Project
The aim of this project is to develop an algorithm for automatic single-object segmentation, specifically targeting the segmentation of fetal heads in ultrasound images. The primary goal is to predict a binary mask that accurately outlines the fetal head, a crucial task in medical imaging for measuring fetal head circumference. 
The implementation is based on a deep learning approach using the SegNet architecture.

## Project Components

### Dataset Handling

- Two datasets (`fetal_ds1` and `fetal_ds2`) are created using the `FetalDataset` class, with different transformations for training and validation.
- Dataset sizes are printed for verification.
- Random samples are chosen and displayed with corresponding masks to visualize the data.

### Data Splitting

- The dataset is split into training and validation sets using ShuffleSplit.
- Subset datasets (`train_ds` and `val_ds`) are created for training and validation.

### Data Loaders

- DataLoader objects (`tin_dl` and `val_dl`) are created for efficient batch processing during training.

### Model Architecture

- A custom SegNet model is implemented for segmentation tasks.
- The architecture consists of encoder and decoder layers with skip connections.
- The model is initialized and summary information is printed.

### Loss Function

- A combination of Binary Cross Entropy (BCE) and Dice Loss is used as the loss function.
- The Dice Loss measures the overlap between the ground truth and the predicted mask.

### Training Loop

- The training loop consists of functions for batch-wise loss calculation and model optimization.
- An Adam optimizer is used, and a learning rate scheduler is implemented.
- The training loop also includes a "sanity check" option for quick debugging on a subset of the data.

### Training and Validation

- The `train_val` function is implemented to run the training and validation loops for multiple epochs.
- Model weights are saved if the validation loss improves.
- Learning rate scheduling and early stopping are incorporated for efficient training.

## Execution and Results

- The entire pipeline is executed for a specified number of epochs.
- Training and validation losses, as well as Dice metrics, are monitored and saved.
- Model weights are stored for the best-performing model on the validation set.


## How to Use

### Dataset Preparation

- Organize the ultrasound images in the `train` folder and their corresponding masks in the `masks` folder.

### Notebook Execution

- Open and run the `Fetal_Head_Segmentation.ipynb` notebook in a Jupyter environment.
- Follow the code cells for dataset creation, model implementation, training, and validation.

### Results and Model Weights

- The final model weights will be saved in the `Models` folder.
- Evaluation metrics and loss curves are available for analysis.

## Conclusion

This project provides a comprehensive solution for automatic fetal head segmentation in ultrasound images. The developed SegNet model, along with the implemented training pipeline, aims to accurately predict fetal head masks for medical applications, particularly in measuring fetal head circumference.


