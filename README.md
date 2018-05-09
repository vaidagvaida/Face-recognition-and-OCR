# Face-recognition-and-OCR

## 1. About the project
In this project I have created a function that identifies faces of our classmates, using feature extraction methods and assigns them with the label (which, in most cases, was the number classmates were holding). This was achieved using 3 types of classifiers (Support Vector Machine (SVM), Feed Forward Neural Network (NN) and AlexNet) and 2 types of feature extraction techniques (HOG and SURF). The types of feature extraction techniques were used in combination with SVM and NN (e.g. NN+HOG, NN+SURF), AlexNet did not need a separate feature Extraction to be performed. I have also created a function that identifies digits from pictures (.jpg format) and videos (.mov format). For this I have created an SVM classifier with HOG features. Both functions were created using Matlab R2018a.

## 2. How to run functions

### 2.1. RecogniseFace
This function takes in 3 arguments: 1. Image path; 2. Feature type; 3. Classifier name (figure 2). It returns a N x 3 matrix that contains predicted label, x coordinate and y coordinate for every face, detected in the picture. It returns a label of 0 if faces, found in the picture, did not match any faces, used to train the classifiers.

### 2.2. detectNum
This function takes file path as an argument and returns a matrix N x 1 that contains each number, seen in the picture (individual numbers are recognised, which means if a person is holding 108, the function should return 1,0,8). This function works for images (.jpg) and videos (.mov). This function uses trained SVM classifier with HOG features. 
