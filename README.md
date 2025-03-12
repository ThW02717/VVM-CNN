# 1D CNN for Hindcasting Potential Temperature Changes

This project uses a simple 1D Convolutional Neural Network (CNN) built with PyTorch to hindcast (predict backward in time) changes in potential temperature.

## What It Does

- **Data Loading & Preprocessing:**  
  Loads data from a NumPy file (`data.npy`) that contains several features (like tke, enst, and θ) and prepares them for the model. The target is the change in θ over time.

- **Model Architecture:**  
  The 1D CNN has:
  - Two convolutional layers (with ReLU activations and max pooling) to extract features from the input sequence.
  - A flatten layer that converts the multi-dimensional features into a 1D vector.
  - Two fully connected layers to output a 50-dimensional prediction, which corresponds to the hindcasted change in potential temperature.

- **Training Process:**  
  The model is trained using the Adam optimizer with Mean Squared Error (MSE) as the loss function. The training process saves the best model based on loss reduction.
