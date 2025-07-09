# Cat vs. Dog Image Classification Using SVM

## Problem Statement

Implement a **Support Vector Machine (SVM)** to classify images of cats and dogs using the Kaggle "Dogs vs. Cats" dataset. The objective is to build a model that can accurately distinguish between cat and dog images based on their pixel features.

## Approach

1. **Data Loading and Exploration:**  
   Download and extract the dataset from Kaggle or Microsoft Research. Inspect image samples and labels for quality and balance[3][4][5].

2. **Data Preprocessing:**  
   - Resize all images to a fixed size (e.g., 64x64 pixels) for uniformity.  
   - Convert images to grayscale for simplicity.  
   - Flatten images into 1D arrays for SVM input.  
   - Assign labels: 0 for cat, 1 for dog.  
   - Normalize pixel values to the range [1].

3. **Feature Selection:**  
   Use raw pixel values as features or experiment with simple feature extraction methods (e.g., Histogram of Oriented Gradients).

4. **Model Training:**  
   Split data into training and test sets. Train an SVM classifier on the training data.

5. **Evaluation:**  
   Evaluate the model using accuracy, precision, recall, and confusion matrix on the test set.

6. **Visualization:**  
   Display sample predictions and the confusion matrix for qualitative assessment.


## Results

- **Accuracy:** Printed in the output.
- **Classification Report:** Shows precision, recall, and F1-score for both classes.
- **Confusion Matrix:** Visualizes the number of correct and incorrect predictions for each class.

## Conclusion

An SVM classifier can effectively distinguish between cat and dog images when provided with well-preprocessed data. While SVMs are not optimal for very large, high-dimensional image datasets compared to deep learning, they offer a simple and interpretable baseline for binary image classification tasks.

## Next Steps

- Extract more advanced features (e.g., HOG, SIFT) for improved performance.
- Experiment with different SVM kernels (e.g., RBF).
- Scale up to more images and consider dimensionality reduction (e.g., PCA).
- Try deep learning models (CNNs) for higher accuracy on complex images.

## How to Run

1. Download the Kaggle dataset from [Kaggle Dogs vs. Cats Competition][3] or [Microsoft Research][4].
2. Extract the images and place them in `train/cat` and `train/dog` directories.
3. Install dependencies:
    ```bash
    pip install numpy opencv-python scikit-learn matplotlib
    ```
4. Run the script:
    ```bash
    python svm_cat_dog_classifier.py
    ```

## Dataset Sources

- [Kaggle Dogs vs. Cats Competition][3]
- [Microsoft Cats and Dogs Dataset][4]
- [Kaggle Cat and Dog Dataset][2]

**References:**  
- Kaggle Dogs vs. Cats: [3][5]
- Microsoft Cats and Dogs Dataset: [4]
- Additional Kaggle datasets: [2][6][8][9]
