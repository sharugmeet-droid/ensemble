# Fashion-MNIST CNN Ensemble vs Single CNN

## Dataset
Fashion-MNIST loaded via keras.datasets.fashion_mnist.load_data().
Used first 50 samples for training and first 50 for testing.

## Preprocessing
- Normalized pixel values to [0,1]
- Reshaped to (28,28,1)
- Train/Validation split using train_test_split

## Models
CNN Architecture:
- Conv2D(32, 3x3, ReLU)
- MaxPooling2D(2x2)
- Flatten
- Dense(10, Softmax)

## Ensemble
- Trained 5 CNN models using bootstrap sampling (bagging)
- Each model trained for 3 epochs
- Ensemble prediction done by averaging probabilities

## Results
Reported validation and test accuracy for:
- Ensemble model
- Single CNN model
