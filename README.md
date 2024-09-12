# Microsoft-Classifying-Cybersecurity-Incidents
## Domain Introduction

The project operates within the cybersecurity domain, focusing on enhancing the efficiency of Security Operation Centers (SOCs). The goal is to leverage machine learning to predict the triage grade of cybersecurity incidents, improving response times and security posture.

### Problem Statement

The task is to build a classification model that categorizes incidents as true positive (TP), benign positive (BP), or false positive (FP)

### Data Cleaning and Preprocessing

Columns with more than 50% null values were dropped, followed by the removal of rows with any remaining null values. This ensured a clean dataset for model building and reduced noise in the data.

### Exploratory Data Analysis (EDA)

- **Univariate Analysis**: Performed on the target column `incidentgrade` to understand its distribution.
- **Pattern Finding**: Identified trends and insights from the target column.

[pattern:](https://www.notion.so/pattern-1fc43f2f335d4bfd82f4e7e4ecad464f?pvs=21)

- **Categorical Features Analysis**: Investigated the distribution of key categorical variables and their relation to the target.
- **Trend Analysis**: Analyzed the trend of `incidentgrade` over time to capture any time-based patterns.

### Feature Engineering

- **Class Balancing**:Class imbalance was handled by undersampling the majority classes to match the size of the minority class using resampling. This approach ensured an equal representation of all `incidentgrade` categories, preventing bias in the model.
- **Feature Importance and Selection**: Feature importance was computed using a Random Forest model, and the top 15 features were selected to focus on key predictors for `incidentgrade`. This reduced dimensionality and improved model performance

### Model Building

- **Base Model**: Logistic Regression was chosen as the base model for its simplicity and interpretability.
- **Advanced Models**: Random Forest,XGBClassifier and Gradient Boosting algorithms were selected for their robustness in handling complex relationships within the data. GridSearchCV was used for hyperparameter tuning to enhance model performance.

### Model Evaluation Metrics

- **Macro-F1 Score**: Selected as the primary metric to balance precision and recall across all classes, particularly given the imbalanced nature of the dataset.
- **Precision and Recall**: Used alongside the macro-F1 score to assess the model's effectiveness in correctly identifying true and false positives.

### Final Model

XGBClassifier  was chosen as the final model due to its superior ability to capture non-linear relationships and its overall better performance in predicting incident grades.

### Conclusion

The feature importance analysis showed that variables like incident category and temporal features (e.g., timestamps) were key contributors to accurate predictions.

### Business Suggestion/Solution

Implementing this model in the SOC's guided response system will significantly improve incident classification, leading to faster and more effective cybersecurity responses.
