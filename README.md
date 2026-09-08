# Handwritten Digit Recognition using CNN

A Convolutional Neural Network (CNN) project for recognizing handwritten digits from the **MNIST dataset** using TensorFlow/Keras.

The model is trained on 60,000 handwritten digit images and evaluated on 10,000 test images. After training, the model is saved to a file and can be used to predict the digit represented in a new image.

## 🚀 Features

* Uses the MNIST handwritten digit dataset
* Image preprocessing and pixel normalization
* Convolutional Neural Network (CNN) architecture
* Categorical cross-entropy loss
* SGD optimizer with momentum
* Trains for 10 epochs
* Saves the trained model as `final_model.h5`
* Supports prediction on custom handwritten digit images

## 🧠 Model Architecture

The CNN consists of:

* `Conv2D` layer with 32 filters
* `MaxPooling2D`
* `Conv2D` layer with 64 filters
* `Conv2D` layer with 64 filters
* `MaxPooling2D`
* `Flatten`
* `Dense` layer with 100 neurons
* `Dense` output layer with 10 neurons and Softmax activation

The input image size is **28 × 28 × 1**, corresponding to grayscale MNIST images.

## 📊 Dataset

This project uses the **MNIST dataset**, which contains handwritten digits from 0 to 9.

* Training images: 60,000
* Test images: 10,000
* Image size: 28 × 28 pixels
* Number of classes: 10

Each pixel is normalized from the range `0–255` to `0–1` before being passed to the neural network.

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* MNIST Dataset

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

Install the required dependencies:

```bash
pip install tensorflow numpy
```

## ▶️ Training the Model

Run the training script:

```bash
python train.py
```

The trained model will be saved as:

```text
final_model.h5
```

## 🔍 Making Predictions

Place a handwritten digit image named:

```text
sample_image.png
```

in the project directory.

Then run the prediction script:

```bash
python predict.py
```

The program will load the trained model, preprocess the image, and print the predicted digit.

Example:

```text
7
```

## 📁 Project Structure

```text
.
├── train.py
├── predict.py
├── sample_image.png
├── final_model.h5
└── README.md
```

## 🔄 Workflow

```text
MNIST Dataset
      ↓
Image Preprocessing
      ↓
Pixel Normalization
      ↓
CNN Training
      ↓
Trained Model
      ↓
Save as final_model.h5
      ↓
Load Custom Image
      ↓
Image Preprocessing
      ↓
CNN Prediction
      ↓
Predicted Digit (0–9)
```

## 🎯 Purpose

This project demonstrates the basic workflow of building an image classification system using a Convolutional Neural Network. It can serve as an introduction to deep learning, computer vision, and handwritten digit recognition with TensorFlow/Keras.

## 📌 Future Improvements

* Add model evaluation on the MNIST test set
* Display accuracy and loss graphs
* Add a confusion matrix
* Support multiple input image formats
* Improve prediction preprocessing for handwritten images
* Build a simple web interface for digit recognition
* Upgrade the saved model format to `.keras`

## 📄 License

This project is available for educational and personal use.
