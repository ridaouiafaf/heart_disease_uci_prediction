# Heart Disease Prediction (ML)
Hi! This is a mini-project where I explored classification techniques to diagnose whether a person is likely to have heart disease based on various health indicators.
The 2nd project to help me gain hands-on experience with the **ML pipeline in healthcare** and overcome my fear of **statistical visualizations** step by step. The additional step here that's different than the diabetes project is that I tried other classification algorithms. 😊


## Project Goals

- Preprocessing data (missing values, outliers, and errors).
- Build and evaluate a Logistic Regression classifier and compare its performance with other classification algorithms like: Decision Tree, Random Forest, SVM, and KNN.
- Learn to visualize model outputs like **ROC AUC**, and **confusion matrices**.
- Comparing algorithms' accuracy, trying to understand why some perform well and others don't.


## Dataset Overview

- 303 rows, 14 columns
- Features include:
  -  age: Age in years
  -  sex: Sex (1 = male, 0 = female)
  -  cp: Chest pain type (4 values)
  -  trestbps: Resting blood pressure (mm Hg)
  -  chol: Serum cholesterol (mg/dl)
  -  fbs: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
  -  restecg: Resting electrocardiographic results (values 0, 1, 2)
  -  thalach: Maximum heart rate achieved
  -  exang: Exercise-induced angina (1 = yes, 0 = no)
  -  oldpeak: ST depression induced by exercise relative to rest
  -  slope: Slope of the peak exercise ST segment
  -  ca: Number of major vessels (0–3) colored by fluoroscopy
  -  thal: Thalassemia (3 = normal, 6 = fixed defect, 7 = reversible defect)
- Target variable: target (1 = Heart Disease, 0 = No Heart Disease)

## ML Pipeline Overview

### 1. Data Cleaning

- Checked for invalid values (e.g., 0 for cholesterol or blood pressure)
- Verified that features like oldpeak can realistically have 0 values (no ST depression at rest)
- Confirmed no major missing/null values in the dataset

### 2. Visual Exploration

- Used boxplots to detect and understand outliers (e.g., cholesterol > 500 mg/dl)
- Explored feature distributions across the target classes (heart disease vs. no heart disease)
- Verified dataset balance: target variable is reasonably balanced (165 vs 138)
- Used a Bar chart to compare algorithms' performance on the same dataset splitting.
- Plotted ROC curve and confusion matrix.

### 3. Feature Scaling

- Applied **StandardScaler** to normalize input features

### 4. Baseline Modeling

- Started with Logistic Regression
- Evaluated with confusion matrix, classification report, ROC AUC
- Baseline ROC AUC: ~0.86

### 5. Model Comparison

- Implemented and compared multiple classifiers: Logistic Regression (LR), Decision Tree (DT), Support Vector Machine (SVM), K-Nearest Neighbors (KNN), and Random Forest (RF).
- Visualized performance using a bar chart of ROC AUC scores

### 6. Results

- SVM achieved the best performance with ROC AUC ~0.84
- Decision Tree performed the weakest (ROC AUC ~0.69), likely due to overfitting and lack of regularization
- Logistic Regression, Random Forest, and KNN all showed competitive results (~0.80)

## What I Learned

- How to code ML pipelines independently without relying too much on AI chatbots help.
- The importance of choosing the right visualization to detect data issues (outliers, imbalances, distributions)
- How to compare multiple classification algorithms for the same problem.
- Why some models (like Decision Trees) can underperform without tuning.
- That visualization and evaluation are as important as model training itself.
- Building confidence to experiment and learn by trial-and-error rather than always seeking ready-made answers.

## License

- Dataset: Heart Disease UCI dataset, sourced from the UCI Machine Learning Repository
. Licensed under CC BY 4.0.
- Code: Released under the MIT License.
