🔍 Binary Classification with Logistic Regression
This project demonstrates how to use logistic regression to predict binary outcomes using a real dataset. It walks through the full ML pipeline—from preprocessing to evaluation and threshold tuning.

📁 Dataset
The dataset contains several features and a binary target variable (0 or 1). The task is to predict the class of each observation using logistic regression.

🧪 Project Steps
Load & preprocess data

Handle missing values and convert categorical variables (if any).

Split dataset

Training and test sets (80/20 split).

Standardize features

Important for optimizing logistic regression performance.

Train logistic regression model

Using scikit-learn's LogisticRegression class.

Evaluate model

Confusion matrix

Precision & recall

ROC-AUC score and ROC curve

Threshold tuning

Demonstrates how changing the classification threshold affects precision and recall.

📈 Evaluation Metrics Explained
Confusion Matrix: Shows TP, TN, FP, FN to understand prediction performance.

Precision: How many predicted positives were actually positive.

Recall: How many actual positives were correctly predicted.

ROC-AUC: Measures ability of model to distinguish between classes across thresholds.

⚙️ Logistic Regression Details
Uses the sigmoid function to convert model output to probabilities.

Outputs are in range (0, 1), suitable for binary classification.

Can be extended to multi-class problems using OvR or multinomial strategies.

🧠 Key Concepts
Logistic regression outputs probabilities, not raw classes.

The decision threshold (default 0.5) can be adjusted based on use case.

Proper handling of imbalanced classes is critical—accuracy is not always enough.
