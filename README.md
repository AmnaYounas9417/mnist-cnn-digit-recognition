MNIST Handwritten Digit Recognition with CNN

A Convolutional Neural Network (CNN) that recognizes handwritten digits (0-9) from the MNIST dataset, built with TensorFlow/Keras.

Dataset
MNIST: 60,000 training and 10,000 test images
Each image is 28 x 28 pixels, grayscale
Stored as CSV: 1 label column + 784 pixel columns (1x1 ... 28x28)
The notebook downloads the data through Keras and creates the CSV files automatically
Model architecture
Layer	Details
Conv2D	32 filters, 3x3, ReLU
MaxPooling2D	2x2
Conv2D	64 filters, 3x3, ReLU
MaxPooling2D	2x2
Flatten	
Dense	128 units, ReLU
Dropout	0.5
Dense	10 units, Softmax
Optimizer: Adam
Loss: Categorical cross-entropy
Early stopping on validation loss
Results
Metric	Value
Test accuracy	99.1%

Project workflow
Load the data and save it as CSV
Explore the data (shape, missing values, class balance)
Preprocess (normalize, reshape to 28x28x1, one-hot encode labels)
Build and train the CNN
Evaluate (accuracy, classification report, confusion matrix)
Visualize correct and incorrect predictions
How to run

Google Colab: upload mnist_cnn_digit_classifier.ipynb and click Runtime -> Run all.

Locally:

bash
git clone https://github.com/<your-username>/mnist-cnn-digit-recognition.git
cd mnist-cnn-digit-recognition
pip install -r requirements.txt
jupyter notebook mnist_cnn_digit_classifier.ipynb
Tech stack

Python, TensorFlow/Keras, NumPy, pandas, Matplotlib, scikit-learn
