#  Fully-Connected Neural Network

This project implements a fully-connected feed-forward neural network built entirely from scratch using NumPy— without deep learning frameworks like TensorFlow or PyTorch.  
It includes training, evaluation, and hyperparameter tuning functionalities on both MNIST digit recognition and a custom MB tabular dataset.

---

##  Overview
The network supports:
- Multiple hidden layer* with customizable sizes.  
- ReLU** activation for hidden layers and Softmax for output.  
- Mini-batch gradient descent with learning rate decay and early stopping.  
- Kaiming initialization for stable weight distribution.  
- Experimentation tools for analyzing performance across parameters (epochs, batch size, learning rate, etc.).

---

##  Key Features

###  Neural Network Architecture
- Customizable layer sizes via constructor parameter.  
- Fully vectorized forward and backward propagation.  
- Supports ReLU and Softmax activations.  
- Built-in accuracy evaluation (`score`) and class prediction (`predict`).

###  Training Functionality
- Mini-batch gradient descent with optional validation tracking.  
- Learning rate decay across epochs for smoother convergence.  
- Early stopping based on validation performance (patience parameter).  

###  Experimentation Tools
Includes plotting utilities to evaluate how different hyperparameters affect accuracy and training time, such as:
- Number of layers  
- Number of epochs  
- Batch size  
- Learning rate  
- Decay rate  

Generated graphs are saved under a `graphs/` directory.

---

##  Datasets

###  MNIST
The MNIST dataset is used for digit classification:
- `MNIST-train.csv`
- `MNIST-test.csv`

Each image (28×28) is flattened into 784 features and normalized between 0 and 1.

### 🧬 MB Dataset
A secondary dataset (`MB_data_train.csv`) is used for binary classification tasks.
- Labels are converted to `0`/`1` via preprocessing.
- Features are standardized using `StandardScaler`.

