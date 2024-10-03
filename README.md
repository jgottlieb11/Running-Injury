# Running Injury Prediction

This project aims to predict running-related injuries by applying various machine learning algorithms and addressing the challenge of imbalanced datasets. The models tested include Support Vector Machine (SVM), K-Nearest Neighbors (KNN), Random Forest, and XGBoost. Several techniques were implemented to handle the imbalance in the dataset, including SMOTE (Synthetic Minority Over-sampling Technique) and Random Under Sampling.

## Overview

The dataset contains various training metrics related to runners, such as total kilometers run, number of strength training sessions, and recovery metrics. The target variable is whether an injury occurred. Due to the imbalance in the dataset, where non-injury cases dominate, it was necessary to apply oversampling and undersampling techniques to ensure the models learned to identify both injured and non-injured cases effectively.

## Models and Techniques

1. **SVM (Support Vector Machine)**:
   - A classification algorithm that finds the optimal separating hyperplane between classes. SVM was tested with both SMOTE and under-sampling techniques to improve its performance on the imbalanced dataset.
   
2. **KNN (K-Nearest Neighbors)**:
   - A non-parametric classifier that predicts based on the k-nearest neighboring data points. Preprocessing and feature scaling were essential for effective KNN performance.

3. **Random Forest**:
   - An ensemble learning method based on decision trees. Random Forest aggregates multiple decision trees built via bootstrapping and generates predictions by averaging or majority vote.

4. **XGBoost**:
   - An advanced boosting algorithm that builds decision trees in sequence. XGBoost focuses on minimizing error using Gradient Descent and was tuned with different hyperparameters to enhance its prediction capability.

## Handling Imbalanced Data

Two approaches were used to handle the imbalance in the dataset:

1. **SMOTE** (Synthetic Minority Over-sampling Technique):
   - SMOTE was used to increase the number of injury cases by generating synthetic examples based on the existing minority class. This technique helped improve model generalization on the injury class.
   
2. **Random Under Sampling**:
   - This technique was used to balance the classes by randomly reducing the number of non-injury cases. While it helps with balance, it also reduces the size of the dataset, which can impact model performance.

## Results

- The models were trained using both oversampling (SMOTE) and undersampling techniques, and the results were compared in terms of accuracy and confusion matrices.
- **Random Forest** and **XGBoost** performed best with SMOTE, showing an accuracy of over 98%, while **SVM** and **KNN** showed improvements with under-sampling.
- The best results were achieved by the **XGBoost** model, which effectively managed the class imbalance and provided the most accurate predictions when using under-sampling.

## Conclusion

This project highlights the importance of handling imbalanced data in machine learning. The use of SMOTE and under-sampling significantly improved the models' ability to predict injuries. The Random Forest and XGBoost models performed particularly well, making them suitable candidates for injury prediction tasks.

Despite the improvements, further work could focus on collecting more injury data or refining feature selection to enhance the model's predictive performance.
