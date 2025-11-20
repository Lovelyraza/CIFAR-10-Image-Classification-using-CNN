CIFAR-10 Image Classification using CNN

This project implements a Convolutional Neural Network (CNN) to classify images from the CIFAR-10 dataset. CIFAR-10 contains 60,000 color images (32x32x3) divided into 10 classes. The model is built using TensorFlow/Keras and trained with data augmentation, batch normalization, and dropout to improve accuracy and generalization.

Dataset Information

CIFAR-10 contains the following 10 classes:

Airplane

Automobile

Bird

Cat

Deer

Dog

Frog

Horse

Ship

Truck

Each image is 32x32 resolution with 3 color channels (RGB).

Model Features

Multiple Conv2D layers with ReLU activation

Batch Normalization for stable and faster training

MaxPooling layers for dimensionality reduction

Dropout layers to reduce overfitting

Adam optimizer with categorical crossentropy loss

Data augmentation applied to improve accuracy

Final Dense layer with softmax activation for 10 classes

Model Architecture Summary

Conv2D → BatchNorm → Conv2D → BatchNorm → MaxPooling → Dropout

Conv2D → BatchNorm → Conv2D → BatchNorm → MaxPooling → Dropout

Flatten → Dense (512) → Dropout → Dense (10)

Training Configuration

Optimizer: Adam

Loss: Categorical Crossentropy

Metrics: Accuracy

Batch Size: 64

Epochs: 20

Validation Split: 20%

Steps Performed in Code

Load CIFAR-10 dataset

Normalize images (0–255 → 0–1)

One-hot encode labels

Apply data augmentation

Build CNN model

Train model

Evaluate on test data

Expected Accuracy

After 20 epochs, the model normally achieves between 70% and 85% accuracy depending on hardware and training time.

Requirements

Install dependencies using:

pip install tensorflow numpy matplotlib

How to Run

Clone the repository:

git clone https://github.com/your-username/cifar10-cnn.git
cd cifar10-cnn


Run the script:

python cifar10_cnn.py

Future Improvements

Add learning rate scheduling

Use transfer learning (ResNet, VGG)

Apply hyperparameter tuning
