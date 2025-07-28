💳 Credit Card Fraud Detection System
A machine learning project that detects fraudulent credit card transactions using classification algorithms. The system is built using Python, with a focus on imbalanced datasets, data preprocessing, and model performance evaluation.

📊 Dataset
The project uses the -  import kagglehub

# Download latest version
path = kagglehub.dataset_download("mlg-ulb/creditcardfraud")

print("Path to dataset files:", path)

🔍 Features
🧹 Data cleaning and preprocessing

📉 Handling imbalanced data using:

Undersampling

Oversampling (SMOTE)

🤖 Model training using:

Logistic Regression

Random Forest

XGBoost

📈 Model evaluation using:

Confusion matrix

ROC-AUC curve

Precision, Recall, F1-score

📊 Visualizations for better understanding

✅ Summary of Your Pipeline
🔹 Step 1: Data Loading and Exploration
Loaded dataset using pandas

Checked shape: (284807, 31)

No missing values

Imbalance found in Class (fraud = 1, normal = 0):

Normal: 275,190

Fraud: 473

🔹 Step 2: Preprocessing
Scaled the Amount column using StandardScaler

Dropped the Time column (not useful for prediction)

Removed duplicates: reduced data to (275663, 30)

🔹 Step 3: Visualization
Used seaborn to visualize the class imbalance

🔹 Step 4: Initial Model Evaluation (Before Sampling)
Logistic Regression

Accuracy: ~99.92%

F1 Score: ~0.719

Recall: ~0.604 (important in fraud detection!)

Decision Tree

Accuracy: ~99.90%

F1 Score: ~0.725

Recall: ~0.769 (better than Logistic)

⚠️ These high accuracy values are misleading due to severe class imbalance.

⚖️ Step 5: Undersampling for Balance
Balanced the dataset:

473 fraud + 473 randomly sampled normal transactions

Total = 946 rows, perfectly balanced

🤖 Step 6: Model Evaluation (After Undersampling)
🔸 Logistic Regression
Accuracy: 92.63%

Precision: 94.9%

Recall: 91.2%

F1 Score: 93.0%

🔸 Decision Tree (You truncated here, but likely similar or better F1)

