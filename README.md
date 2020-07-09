# Digit Recognizer

kaggle Computer Vision Beginner Competition - https://www.kaggle.com/c/digit-recognizer/overview

## Data
MNIST ("Modified National Institute of Standards and Technology") is dataset of computer vision.The data has total 60,000 images, consisting of 10 classes (0-9 digit images).

## Steps to Code.

### 1. Load Data 

1. Download data from here - https://www.kaggle.com/c/digit-recognizer/data . Load the train and test data csv files.

### 2. Data Pre-processing

1. Null & Missing Values - Check for null values and missing pixel values.

2. Data Normalization - We perform grayscale normalization (divide each pixel value by 255) to reduce effect of        Illumination. CNN converges faster on [0,1] data,than [0,255].

3. Reshape Data - CNN takes in 3D matrix. Each pixel column in the training set has a name like pixel x, where x is      an integer between 0 and 783, inclusive. Reshape data to [28, 28, 1]. Since its grayscale, having 1 channel.

4. Label Encoding - One hot encoding of Target variable. Ex- 1 - [0,1,0,0,0,0,0,0,0]

5. Data Split - Train data is split into train (90% Train) and validation (10% Train).

### 3. CNN model

Model - Basic CNN model having 2 sets of (Conv2d -> MaxPool -> Dropout). Then Flat layer - Dense (10 class).
<p align="center">
  <img src="https://github.com/Ranger105/Digit-Recognizer/blob/master/my_CNN_model.png">
</p> 
