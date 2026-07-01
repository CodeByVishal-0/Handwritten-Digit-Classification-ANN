# 🧠 Handwritten Digit Recognition using Deep Neural Network (MNIST)

A Deep Learning project that classifies handwritten digits (0–9) using TensorFlow/Keras on the MNIST dataset. The model is built using a fully connected Artificial Neural Network (ANN) and achieves **97.88% test accuracy**.

---

## 📌 Project Overview

Handwritten digit recognition is one of the most fundamental computer vision tasks. This project demonstrates how a Deep Neural Network (DNN) can accurately classify grayscale images of handwritten digits from the MNIST dataset.

The model is trained using TensorFlow/Keras and consists of multiple Dense layers with ReLU activation and a Softmax output layer for multi-class classification.

---

## 📂 Dataset

The project uses the **MNIST Handwritten Digits Dataset**, which is included with TensorFlow/Keras.

### Dataset Details

- **Total Images:** 70,000
- **Training Images:** 60,000
- **Testing Images:** 10,000
- **Image Size:** 28 × 28 pixels
- **Color Format:** Grayscale
- **Classes:** 10 (Digits 0–9)

Dataset can be loaded using:

```python
from tensorflow.keras.datasets import mnist

(X_train, y_train), (X_test, y_test) = mnist.load_data()
```

---

# 🛠 Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib

---

# 🏗 Model Architecture

The neural network consists of the following layers:

| Layer | Output Shape | Parameters |
|--------|-------------|-----------:|
| Flatten | (None, 784) | 0 |
| Dense (ReLU) | (None, 128) | 100,480 |
| Dense (ReLU) | (None, 32) | 4,128 |
| Dense (Softmax) | (None, 10) | 330 |

### Total Parameters

```
104,938
```

- Trainable Parameters: **104,938**
- Non-Trainable Parameters: **0**

---

# ⚙ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Epochs | 25 |
| Batch Size | 32 |
| Activation | ReLU, Softmax |

---

# 📈 Training Results

The model was trained for **25 epochs**.

### Training Progress

| Epoch | Training Loss | Validation Loss |
|-------:|--------------:|----------------:|
| 1 | 0.2865 | 0.1581 |
| 2 | 0.1240 | 0.1206 |
| 3 | 0.0835 | 0.1047 |
| 4 | 0.0634 | 0.0958 |
| 5 | 0.0480 | 0.1044 |
| 10 | 0.0191 | 0.1057 |
| 15 | ~0.01 | ~0.13 |
| 20 | ~0.008 | ~0.15 |
| 25 | 0.0090 | 0.1608 |

---

# 🎯 Model Performance

## Test Accuracy

```
97.88%
```

### Observations

- Training loss continuously decreases.
- Validation loss initially decreases but later starts increasing.
- The increasing validation loss indicates **slight overfitting** after several epochs.
- Despite this, the model generalizes well and achieves nearly **98% accuracy**.

---

# 📊 Sample Prediction

The trained model predicts handwritten digits from grayscale images.

Example:

```
Input Image  →  Predicted Digit

28×28 Image  →       7
28×28 Image  →       3
28×28 Image  →       0
```

---

# 📁 Project Structure

```
MNIST-Digit-Recognition/
│
├── mnist_classification.ipynb
├── README.md
```

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/yourusername/MNIST-Digit-Recognition.git
```

Move into the project directory

```bash
cd MNIST-Digit-Recognition
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

---

# 📦 Requirements

```
tensorflow
numpy
matplotlib
jupyter
```

or install using

```bash
pip install tensorflow numpy matplotlib jupyter
```

---

# 💡 Future Improvements

- Add Dropout layers to reduce overfitting.
- Implement Batch Normalization.
- Build a Convolutional Neural Network (CNN) for higher accuracy.
- Add data augmentation techniques.
- Deploy the trained model using Flask or FastAPI.
- Create a Streamlit web application for digit prediction.
- Convert the model to TensorFlow Lite for mobile deployment.

---

# 📚 Learning Outcomes

Through this project, I learned:

- Image preprocessing
- Neural Network fundamentals
- TensorFlow/Keras workflow
- Model training and evaluation
- Multi-class classification
- Overfitting analysis
- Hyperparameter tuning

---

# 📸 Results

- ✅ Training completed successfully
- ✅ Test Accuracy: **97.88%**
- ✅ Deep Neural Network implemented using TensorFlow/Keras
- ✅ Multi-class digit classification achieved

---

# 🤝 Contributing

Contributions are welcome!

Feel free to fork this repository, improve the model, and submit a pull request.

---

# 📄 License

This project is open-source and available under the **MIT License**.

---

## ⭐ If you found this project helpful, consider giving it a star on GitHub!