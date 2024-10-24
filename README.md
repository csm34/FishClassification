# Fish Classification Project

A deep learning project that identifies different types of fish from their images using Artificial Neural Networks (ANN).

## Table of Contents
- [About]
- [Dataset]
- [Setup]
- [Model Details]
- [Results]

## About
This project helps identify different types of fish by looking at their pictures. It uses artificial intelligence to learn and recognize fish patterns.

## Dataset
- Source: Kaggle Fish Dataset: https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset
- Image type: PNG files
- Image size: 128x128 pixels
- Color: RGB (Red, Green, Blue)

## Setup

### Required Libraries
```python
numpy
pandas
tensorflow
scikit-learn
matplotlib
seaborn
Pillow
```


## Model Details

### Network Structure
The model processes images through several layers:

1. **Input**
   - Takes in fish images (128x128 pixels)

2. **Hidden Layers**
   - First layer: 512 nodes
   - Second layer: 256 nodes
   - Third layer: 128 nodes
   - Each layer has:
     - ReLU activation
     - Batch Normalization
     - Dropout (30% to prevent overfitting)

3. **Output**
   - Final layer: One node per fish type
   - Uses Softmax to predict fish type

### Training Settings
- Training-Test split: 80%-20%
- Batch size: 32 images at once
- Maximum training rounds: 20
- Learning rate: 0.001
- Optimizer: Adam

### Model Improvements
We tested three different setups:

1. Setup 1:
   - 3 layers
   - 512 nodes
   - 30% dropout
   - Learning rate: 0.001

2. Setup 2:
   - 4 layers
   - 1024 nodes
   - 40% dropout
   - Learning rate: 0.0001

3. Setup 3:
   - 2 layers
   - 256 nodes
   - 20% dropout
   - Learning rate: 0.001

### Safety Features
- Early stopping to prevent overtraining
- Learning rate reduction when needed
- Regular accuracy checks
- Dropout layers to improve learning

## Results
The model provides:
- Accuracy score
- Error rate
- Confusion matrix (shows correct vs incorrect predictions)
- Detailed classification report

## Model Monitoring
- Tracks training progress
- Shows accuracy improvements
- Identifies any learning problems
- Saves the best version of the model

## Future Improvements
1. Add more training data
2. Try different network structures
3. Test other learning methods
4. Add cross-validation
5. Try combining multiple models

## Notes
- Model progress is constantly monitored
- Training stops automatically if no improvement
- Best model version is saved
- Regular checks prevent overtraining

Kaggle: https://www.kaggle.com/code/cisemh/ann-8/
