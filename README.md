# Breast Cancer Diagnosis 

## Introduction
In this README, we will provide an overview of our breast cancer diagnosis classification project. The primary objective was to develop a robust machine learning model to classify breast tumors as either benign (B) or malignant (M) based on various features extracted from diagnostic images.

## Data
The dataset used for this project can be accessed at the following path:
`C:/Users/Niner/Desktop/Builds/breast-cancer-diagnosis-icu-wisconsin-/data.csv`

The dataset contains 569 samples and was preprocessed as follows:

- Removal of unnecessary columns ('id' and 'Unnamed: 32').
- Feature selection based on mutual information.
- Standardization of selected features using StandardScaler.

### Data Overview
- Number of Features: 30 (After preprocessing)
- Number of Instances: 569
- Class Distribution: Benign (357) and Malignant (212)

## Feature Selection
Feature selection was performed to improve model performance and reduce dimensionality. Mutual Information was used to evaluate the importance of each feature with respect to the target variable (B or M).

The top informative features selected based on mutual information include:

- radius_mean
- concave points_worst
- perimeter_mean
- concavity_mean
- area_mean
- concave points_mean
- texture_mean
- radius_worst
- area_se
- smoothness_se

## Model Building
We used the Gradient Boosting Classifier with the following hyperparameters:

- Number of Estimators: 500
- Learning Rate: 0.1

The Gradient Boosting Classifier is an ensemble learning method known for its strong predictive power and resistance to overfitting. The model was trained on the preprocessed data.

## Model Evaluation
The model was evaluated using various performance metrics:

- **Accuracy:** The model achieved an accuracy of approximately 95.91% on the test dataset.

- **Classification Report:**
  ```
  precision    recall  f1-score   support

           0       0.97      0.97      0.97       108
           1       0.95      0.95      0.95        63

    accuracy                           0.96       171
   macro avg       0.96      0.96      0.96       171
weighted avg       0.96      0.96      0.96       171
  ```

- **Mean Squared Error (MSE):** The MSE was approximately 0.04, indicating the model's good predictive accuracy.

- **Root Mean Squared Error (RMSE):** The RMSE was approximately 0.20, showing the model's good generalization.

- **Cross-Validation:** The model was subjected to 5-fold cross-validation, resulting in an average cross-validation score of approximately 96.12%. The low standard deviation of approximately 0.0098 suggests that the model generalizes well.

## Conclusion
The model demonstrates strong performance in breast cancer diagnosis classification. It achieves an accuracy of 95.91% on the test data, has a low mean squared error and root mean squared error, and generalizes well with a low standard deviation in cross-validation.

The model is robust and suitable for breast cancer diagnosis. It may be considered for deployment to assist medical professionals in identifying potential malignancies in breast tumors. Further refinement may be considered to improve its robustness and adaptability for clinical use.

## Additional Notes
The code provided in this README contains snippets that may require additional adjustments to generate the mutual information plot and confusion matrix plot. Make sure to save those plots as 'mutual_info.png' and 'confusion_matrix.png' to include them in your report or README.