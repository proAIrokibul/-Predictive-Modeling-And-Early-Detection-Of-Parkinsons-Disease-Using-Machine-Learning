# Predictive Modeling And Early Detection Of Parkinsons Disease Using Machine Learning

## Overview
This project aims to classify individuals as healthy or diagnosed with Parkinson's disease based on vocal feature data. The dataset comprises various acoustic measurements that capture voice characteristics, which are crucial for detecting subtle changes related to Parkinson's disease.

## Dataset
The dataset contains **1195 samples** and various vocal features, including:

- **MDVP:Fo(Hz)**: Fundamental Frequency
- **MDVP:Fhi(Hz)**: Highest Frequency
- **MDVP:Flo(Hz)**: Lowest Frequency
- **MDVP:Jitter(%)**: Jitter (local variation in fundamental frequency)
- **MDVP:Jitter(Abs)**: Absolute Jitter
- **MDVP:RAP**: Relative Average Perturbation
- **MDVP:PPQ**: Pitch Perturbation Quotient
- **MDVP:Shimmer**: Shimmer (amplitude variation)
- **HNR**: Harmonics-to-Noise Ratio
- **RPDE**: Recurrence Period Density Entropy
- **status**: Diagnosis (0: Healthy, 1: Parkinson's)

## Methodology
We implemented three machine learning models to classify the data:
1. **Logistic Regression**
2. **Random Forest Classifier**
3. **Support Vector Machine (SVM)**

### Preprocessing
Data preprocessing steps included:
- Handling missing values and ensuring data integrity.
- Encoding the target variable (`status`).
- Splitting the dataset into training and testing sets.

### Model Evaluation
Each model's performance was evaluated using accuracy, precision, recall, and F1-score metrics, which provide insights into the models' predictive capabilities.

## Results

### Logistic Regression
- **Accuracy:** 89.74%
- **Classification Report:**
    ```
                   precision    recall  f1-score   support

             0.0       1.00      0.43      0.60         7
             1.0       0.89      1.00      0.94        32

        accuracy                           0.90        39
       macro avg       0.94      0.71      0.77        39
    weighted avg       0.91      0.90      0.88        39
    ```

### Random Forest Classifier
- **Accuracy:** 94.87%
- **Classification Report:**
    ```
                   precision    recall  f1-score   support

             0.0       1.00      0.71      0.83         7
             1.0       0.94      1.00      0.97        32

        accuracy                           0.95        39
       macro avg       0.97      0.86      0.90        39
    weighted avg       0.95      0.95      0.95        39
    ```

### Support Vector Machine (SVM)
- **Accuracy:** 87.18%
- **Classification Report:**
    ```
                   precision    recall  f1-score   support

             0.0       0.67      0.57      0.62         7
             1.0       0.91      0.94      0.92        32

        accuracy                           0.87        39
       macro avg       0.79      0.75      0.77        39
    weighted avg       0.87      0.87      0.87        39
    ```

## Analysis
- **Logistic Regression** performed well with an overall accuracy of **89.74%**, but it struggled with classifying healthy individuals (only 43% recall for class 0).
- **Random Forest Classifier** exhibited the best performance with an accuracy of **94.87%**, demonstrating a strong ability to classify both classes effectively, particularly for the Parkinson's class (100% recall).
- **Support Vector Machine (SVM)** had the lowest accuracy at **87.18%**, and while it performed reasonably well for the Parkinson's class, it had difficulties with the healthy class (57% recall).

The results indicate that while all models can discriminate between classes, the Random Forest Classifier is the most effective for this dataset. This finding suggests that more complex models may better capture the intricacies in vocal features associated with Parkinson's disease.

## Future Work
Future improvements to this project could include:
- Hyperparameter tuning to optimize model performance further.
- Exploring additional machine learning models and ensemble techniques.
- Using more extensive and diverse datasets for better generalization.

## Conclusion
This project demonstrates the potential of using vocal feature analysis in the early detection of Parkinson's disease. The findings underscore the importance of selecting appropriate machine learning algorithms to improve diagnostic accuracy in healthcare applications.
