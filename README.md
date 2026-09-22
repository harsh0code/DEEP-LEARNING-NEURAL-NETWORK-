# MNIST Handwritten Digit Classification

A machine learning project that classifies handwritten digits (0–9) using the **MNIST dataset** and a neural network built with **TensorFlow and Keras**.

## 📌 Project Overview

The **MNIST Handwritten Digit Classification** project demonstrates how a neural network can learn to recognize handwritten digits from grayscale images.

The MNIST dataset contains thousands of handwritten digit images. Each image is represented as a **28 × 28 pixel grayscale image** and belongs to one of ten classes:

`0, 1, 2, 3, 4, 5, 6, 7, 8, 9`

The project covers the complete machine learning workflow:

1. Loading the dataset
2. Exploring the data
3. Preprocessing images
4. Building a neural network
5. Training the model
6. Evaluating model performance
7. Predicting handwritten digits
8. Visualizing predictions and results

---

## 🎯 Objectives

The main objectives of this project are:

* To understand image classification using neural networks.
* To work with the MNIST handwritten digit dataset.
* To preprocess image data for machine learning.
* To build and train a neural network using TensorFlow/Keras.
* To evaluate classification accuracy.
* To visualize predictions made by the trained model.

---

## 🛠️ Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **MNIST Dataset**

---

## 📊 Dataset

The project uses the built-in **MNIST dataset** provided by TensorFlow/Keras.

The dataset contains:

* **60,000** training images
* **10,000** testing images
* Image size: **28 × 28 pixels**
* Number of classes: **10**
* Image type: **Grayscale**

Each image represents a handwritten digit from 0 to 9.

### Dataset Structure

```text
Training Data
├── Images: 60,000
└── Labels: 60,000

Testing Data
├── Images: 10,000
└── Labels: 10,000
```

---

## 🧠 Model Architecture

The neural network consists of the following layers:

```text
Input Image
    ↓
Flatten Layer
    ↓
Dense Layer
    ↓
Dense Layer
    ↓
Output Layer
```

The **Flatten** layer converts the 28 × 28 image into a one-dimensional array.

The **Dense** layers learn patterns and features from the image.

The final layer contains **10 neurons**, corresponding to the ten possible digit classes.

---

## ⚙️ Data Preprocessing

The pixel values of MNIST images range from:

```text
0 to 255
```

These values are normalized to:

```text
0 to 1
```

This is done by dividing the pixel values by 255.

Normalization helps the neural network train more efficiently.

---

## 💻 Installation

Make sure Python is installed on your computer.

Install the required libraries using:

```bash
pip install tensorflow numpy matplotlib
```

---

## ▶️ How to Run

### 1. Clone or download the project

Download the project files to your computer.

### 2. Open the project directory

```bash
cd MNIST-Handwritten-Digit-Classification
```

### 3. Install dependencies

```bash
pip install tensorflow numpy matplotlib
```

### 4. Run the Python program

```bash
python mnist.py
```

The program will load the MNIST dataset, train the neural network, evaluate its performance, and display predictions.

---

## 📁 Project Structure

```text
MNIST-Handwritten-Digit-Classification/
│
├── mnist.py
├── README.md
└── requirements.txt
```

### `mnist.py`

Contains the complete Python implementation for:

* Dataset loading
* Data preprocessing
* Model creation
* Model training
* Model evaluation
* Prediction
* Visualization

### `README.md`

Contains project documentation and instructions.

### `requirements.txt`

Contains the Python libraries required to run the project.

Example:

```text
tensorflow
numpy
matplotlib
```

---

## 📈 Model Training

During training, the neural network learns to identify patterns in handwritten digits.

The model uses:

* **Loss Function:** Sparse Categorical Crossentropy
* **Optimizer:** Adam
* **Evaluation Metric:** Accuracy

Example:

```python
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
```

---

## 🔍 Prediction

After training, the model can predict the digit represented by an unseen image.

Example:

```python
prediction = model.predict(x_test)

predicted_digit = np.argmax(prediction[0])

print("Predicted Digit:", predicted_digit)
```

The predicted digit is determined by selecting the class with the highest probability.

---

## 📊 Visualization

Matplotlib can be used to display MNIST images and their predicted labels.

Example:

```python
plt.imshow(x_test[0], cmap='gray')
plt.title(f"Predicted Digit: {predicted_digit}")
plt.axis('off')
plt.show()
```

This allows us to visually compare the actual handwritten digit with the model's prediction.

---

## ✅ Results

The trained neural network is capable of recognizing handwritten digits with high accuracy on the MNIST test dataset.

The final accuracy depends on:

* Model architecture
* Number of training epochs
* Batch size
* Optimizer
* Preprocessing
* Hardware used for training

The training output displays the achieved training and testing accuracy.

---

## 🚀 Future Improvements

The project can be improved by:

* Using a **Convolutional Neural Network (CNN)**.
* Adding more hidden layers.
* Using **Dropout** to reduce overfitting.
* Implementing data augmentation.
* Creating a web interface using **Streamlit**.
* Allowing users to draw digits using a mouse or touchscreen.
* Deploying the trained model as a web application.
* Comparing different neural network architectures.

---

## 📚 Learning Outcomes

Through this project, the following concepts are demonstrated:

* Machine Learning
* Deep Learning
* Image Classification
* Neural Networks
* TensorFlow
* Keras
* Data Preprocessing
* Model Training
* Model Evaluation
* Prediction and Visualization

---

## 👨‍💻 Author

**Harsh**

B.Tech Information Technology
Specialization: Artificial Intelligence & Machine Learning

---

## 📄 License

This project is created for **educational and academic purposes**.
