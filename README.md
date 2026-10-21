# -MNIST-Digit-Recognition-Dataset

# MNIST Digit Recognition using Deep Learning

This repository contains a Python-based implementation of a Feedforward Neural Network built using **TensorFlow** and **Keras** to classify handwritten digits from the **MNIST dataset**.

##  Tech Stack & Libraries

* **Programming Language:** Python
* **Deep Learning Framework:** TensorFlow / Keras
* **Numerical Computations:** NumPy
* **Data Visualization:** Matplotlib

##  Project Workflow 

1. **Data Acquisition:** Loaded the standard **MNIST dataset** consisting of 60,000 training images and 10,000 testing images of handwritten digits ($28 \times 28$ pixels).
2. **Exploratory Data Analysis & Visualization:** Inspected tensor shapes and visualized individual digit samples using Matplotlib to verify data integrity.
3. **Data Preprocessing & Normalization:** Scaled the raw pixel intensity values from the range $[0, 255]$ down to $[0.0, 1.0]$ by dividing by `255.0`. This normalization ensures faster convergence and stable gradient updates during training.
4. **Model Architecture (`Sequential`):** Designed a fully connected Deep Neural Network with three primary layers:
* **Flatten Layer:** Reshapes the $28 \times 28$ 2D image matrices into a 1D vector of $784$ features.
* **Hidden Layer:** A Dense layer with $128$ neurons utilizing the **ReLU** (Rectified Linear Unit) activation function to capture non-linear patterns.
* **Output Layer:** A Dense layer with $10$ neurons using the **Softmax** activation function to output probability distributions across the 10 digit classes ($0$ through $9$).


5. **Model Compilation:** Configured the model with the following settings:
* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Crossentropy
* **Metrics:** Accuracy


6. **Training & Validation:** Trained the network over $10$ epochs with a `batch_size` of $64$ and a $20\%$ validation split (`validation_split=0.2`), closely monitoring loss and accuracy metrics to prevent overfitting.
7. **Evaluation & Inference:** Evaluated the trained model on unseen test data, achieving a high classification accuracy (~97.96%), followed by generating predictions using `np.argmax`.
8. **Performance Tracking:** Plotted training and validation loss/accuracy curves across epochs to evaluate model stability and convergence behavior.
  
