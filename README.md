___________CREDIT CARD FRAUD DETECTION ____________________
Credit card fraud detection is a imbalanced classification problem where fraudulent transactions are extremely rare compared to legitimate ones.
This project builds and evaluates machine learning models to detect fraud reliably while considering real-world business constraints such as false positives, false negatives, and deployment challenges.

Total transactions: 284,807

Fraudulent transactions: 492 (~0.17%)

Features: 28 anonymized PCA-transformed features + Time + Amount

Target: Class (0 = Legitimate, 1 = Fraud)
_____________________________________________________________

Model 1: Logistic Regression 

Why Logistic Regression?

Simple and interpretable

Produces probability outputs

Commonly used in financial risk modeling

Observation:

High accuracy

Very poor fraud recall (fails to detect fraud effectively)

_____________________________________________________________________

Model 2: Logistic Regression with Class Weighting

Technique Used: class_weight='balanced'

Effect:

Improves fraud recall significantly

Slight increase in false positives

Suitable for production where missing fraud is costly.
___________________________________________________________________
Model 3: Logistic Regression with SMOTE

Technique Used: Synthetic Minority Oversampling Technique

Effect:

Strong improvement in fraud recall

Increased false positives
______________________________________________________________________
Model 4: Random Forest (Tree-Based Model)

Why Random Forest?

Captures nonlinear patterns

Handles feature interactions well

Robust to noise

Imbalance Handling: class_weight='balanced'

Achieved the best overall balance between recall and precision.
_____________________________________________________________________

Due to class imbalance, the following metrics were used:

Recall (Fraud Class) – Most important

Precision (Fraud Class)

ROC-AUC

Confusion Matrix

Accuracy was deliberately not treated as the primary metric.
__________________________________________
Tools & Libraries Used

Python

Pandas, NumPy

Scikit-learn

Imbalanced-learn

Matplotlib, Seaborn
