
This project is a deep learning model built to classify handwritten digits from the well-known MNIST dataset. It uses a Sequential Neural Network implemented in **TensorFlow** and the **Keras** API.

The model is trained on 60,000 images and validated on 10,000 unseen images, achieving an accuracy of approximately **97%**.

## 📋 Dataset

This project uses the **MNIST dataset**, a large database of handwritten digits that is a standard benchmark for machine learning and computer vision.

* **Training Set:** 60,000 images
* **Testing Set:** 10,000 images
* **Image Format:** 28x28 pixel grayscale images

The data is pre-processed by **normalizing** the pixel values (scaling them from 0-255 to 0-1) to improve model training.

## 🤖 Model Architecture

The model is a simple Sequential Neural Network with the following layers:

1.  **Flatten Layer:** Converts the 2D (28x28) image array into a 1D (784 pixels) vector.
2.  **Dense Layer (Hidden):** 128 neurons with a `relu` (Rectified Linear Unit) activation function.
3.  **Dense Layer (Hidden):** 128 neurons with a `relu` activation function.
4.  **Dense Layer (Output):** 10 neurons (one for each digit, 0-9) with a `softmax` activation function. `softmax` converts the model's raw output (logits) into a probability distribution, showing the model's confidence for each class.

The model is compiled using the **Adam optimizer** and the **`sparse_categorical_crossentropy`** loss function, which is ideal for multi-class classification problems where the labels are integers (like 0, 1, 2...).

## 📊 Performance

After training for 3 epochs, the model achieved the following performance on the 10,000-image test set:

* **Test Accuracy:** ~97%
* **Test Loss:** ~0.096

A pre-trained version of this model is saved in the `handwritten.keras` file.

## 🛠️ Technologies Used

* **Python 3**
* **TensorFlow / Keras:** For building and training the neural network.
* **NumPy:** For numerical operations (though TensorFlow handles most).
* **Matplotlib:** For visualizing data (used in exploratory phases).
* **Jupyter Notebook:** For interactive development and documentation.
