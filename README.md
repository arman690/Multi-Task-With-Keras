# Multi-Task Model with Keras

This project demonstrates how to build and train a multi-task model using Keras to classify handwritten digits and detect a randomly assigned color channel for each image. The model is built on the MNIST dataset, which consists of grayscale images of handwritten digits (0-9).

## Project Overview

- **Multi-Task Learning**: The model simultaneously learns to classify both the digit and a color channel (red or green) that has been randomly assigned.
- **Dataset**: Uses the MNIST dataset with additional transformations to convert grayscale images into RGB format.
- **Model Architecture**: A convolutional neural network (CNN) with shared layers and two separate output heads for each task (digit classification and color detection).
- **Evaluation**: Visual evaluation of model predictions, with TensorBoard logging for tracking performance.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/multi-task-model-keras.git
   ```
2. Install the required libraries:
   ```bash
   pip install tensorflow numpy matplotlib
   ```

## Notebook Structure

1. **Import Libraries**: Loads required libraries for data processing, model building, and visualization.
2. **Load and Preprocess Data**: Loads MNIST dataset and transforms grayscale images into RGB format, assigning a random color channel.
3. **Define Model**: Builds a multi-task CNN model with shared and separate layers for each task.
4. **Compile and Train Model**: Compiles the model with Adam optimizer, specifying separate loss functions and metrics for each output.
5. **Evaluation**: Tests model predictions on individual and multiple samples, displaying the results using matplotlib.
6. **TensorBoard Logging**: Uses TensorBoard to visualize training metrics and monitor model performance in real-time.

## Usage

- Run the Jupyter notebook to execute each cell in order. You can modify the batch size, number of epochs, or architecture as needed.
- The `Logger` callback class displays the model's performance after each epoch.
- To visualize training metrics, run TensorBoard:
  ```bash
  %tensorboard --logdir ./logs
  ```

## Example Results

- **Digit Classification**: Model outputs a digit label (0-9) for each image.
- **Color Detection**: Model predicts the color channel assigned to each image (red or green).
  
The notebook also includes a grid of test images, displaying ground truth (GT) and predicted (Pr) values, allowing a quick assessment of model accuracy.

