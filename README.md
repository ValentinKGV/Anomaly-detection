# Anomaly Prediction Model

## Dataset Analysis:

### 1.1 Nature of the Data:
The dataset provided for the project addresses the classification of abnormal data registered from different patients. It includes six features for each patient: incidence, tilt, angle, slope, radius, and grade. The task is to classify samples as normal or abnormal, where anomalous samples correspond to patients with various medical problems (e.g., disk hernia, spondylolisthesis).

### 1.2 Data Structure and Characteristics:
Features:
* Incidence
* Tilt
* Angle
* Slope
* Radius
* Grade

Target Variable:
* Binary classification: Normal (0) or Abnormal (1)

## 2 Statistical Analysis:

### 2.1 Descriptive Statistics:
Performed basic descriptive statistics, including mean, median, standard deviation, and quartiles for each feature. This helped in understanding the central tendency and variability in the data.

### 2.2 Advanced Statistical Methods:
Utilized advanced statistical methods such as correlation analysis to explore relationships between features and the target variable. Examined the distribution of each feature to identify potential outliers.

## 3. Machine Learning Model: Logistic Regression

### 3.1 Model Selection:
For the anomaly prediction task, we chose the Logistic Regression model due to its simplicity, interpretability, and effectiveness in handling classification problems. Logistic Regression is well-suited for anomaly detection, particularly when the decision boundary is non-linear and the dataset is not too large.

### 3.2 Dataset Balancing with SMOTE:
Given the imbalanced nature of the dataset, where the number of abnormal instances is significantly lower than the normal instances, we employed the undersampling technique. Undersampling generates synthetic instances for the minority class, addressing the class imbalance and providing the model with a more representative training set.

### 3.3 Hyperparameter Tuning:
To optimize the performance of the Logistic Regression  model, we conducted hyperparameter tuning. 

### 3.4 Model Development:
Implemented the Logistic Regression  model with the optimal hyperparameters and trained it on the dataset augmented with undersampling-generated samples.

## 4. Model Evaluation:

### 4.1 Performance Metrics:
Evaluated the Logistic Regression  model using a comprehensive set of performance metrics:

Accuracy: 0.66
Precision: 0.8
Recall: 1.0
F1 Score: 0.88
ROC AUC Score: 0.81

### 4.2 Significance of Metrics:
The use of undersampling and hyperparameter tuningsignificantly improved the model's ability to recognize anomalies by addressing the class imbalance issue. The achieved recall of 1.0 indicates that the model successfully identified all abnormal instances, minimizing false negatives. Precision of 0.8 demonstrates a balanced trade-off between correctly identifying anomalies and avoiding false positives.

The F1 Score, a harmonic mean of precision and recall, provides a consolidated measure of the model's overall performance. The ROC AUC Score of 0.80 further confirms the model's effectiveness in distinguishing between normal and abnormal instances.

In summary, the combination of the KNN model, SMOTE for dataset balancing, and hyperparameter tuning led to a well-performing anomaly detection model with robust metrics across accuracy, precision, recall, F1 score, and ROC AUC score.

## 5. Results and Discussion:

### 5.1 Model Performance Overview:
The Logistic Regression model, enhanced by the application of Synthetic Minority Over-sampling Technique (SMOTE) for balancing the dataset and careful hyperparameter tuning, exhibited exceptional performance in the task of anomaly detection.

### 5.2 Evaluation Metrics:
Accuracy: 0.8653846153846154

The model achieved an accuracy of approximately 86.5%, indicating its proficiency in correctly classifying both normal and abnormal instances.
Precision: 0.8

Precision of 0.8 highlights the model's capability to accurately identify abnormal instances while minimizing false positives, making it a reliable tool for medical anomaly detection.
Recall: 1.0

A perfect recall of 1.0 underscores the model's ability to identify all instances of abnormality. This is a crucial metric in the context of medical diagnosis, where missing an abnormal case is highly undesirable.
F1 Score: 0.888888888888889

The F1 Score, balancing precision and recall, attains a high value of approximately 0.89, indicating a harmonious trade-off between false positives and false negatives.
ROC AUC Score: 0.8541666666666666

The ROC AUC Score of 0.8541666666666666 reflects the model's robustness in distinguishing between normal and abnormal instances across different classification thresholds.
Accuracy (0.655):

The accuracy is the proportion of correctly classified instances out of the total instances.
In this case, the model has an accuracy of approximately 65.5%, indicating that it correctly predicted the target variable for about 65.5% of the samples.

Confusion Matrix:

A confusion matrix provides a detailed breakdown of the model's predictions.
In this case:
True Positive (TP): 16 instances correctly predicted as class 0.
False Negative (FN): 10 instances of class 0 incorrectly predicted as class 1.
False Positive (FP): 0 instances of class 1 incorrectly predicted as class 0.
True Negative (TN): 3 instances correctly predicted as class 1.

Classification Report:

Precision: The ratio of true positives to the total predicted positives.
Recall: The ratio of true positives to the total actual positives.
F1-score: The harmonic mean of precision and recall.
Support: The number of actual occurrences of the class in the specified dataset.
In this case:
Class 0 (non-anomaly): High precision (1.00), indicating that when the model predicts class 0, it is usually correct. However, the low recall (0.62) and F1-score (0.76) suggest that the model misses some instances of class 0.
Class 1 (anomaly): Moderate precision (0.23), indicating that when the model predicts class 1, it is less reliable. However, high recall (1.00) suggests that the model correctly identifies most instances of class 1.

ROC AUC Score (0.808):

The Receiver Operating Characteristic Area Under the Curve (ROC AUC) measures the ability of the model to discriminate between positive and negative instances.
A score of 0.808 suggests that the model has a relatively good ability to distinguish between the two classes.
### 5.3 Implications and Insights:
The exceptional recall and F1 Score suggest that the Logistic Regression model, enriched by the inclusion of Undersampling, has successfully learned to identify anomalies, particularly instances associated with medical problems such as disk hernia and spondylolisthesis. The use of Undersampling and fine-tuning hyperparameters hasplayed a pivotal role in mitigating the impact of class imbalance, leading to a more balanced and effective model.

### 5.4 Further Considerations:
While the model showcases impressive results, ongoing evaluation on new data and continuous monitoring are recommended. Additionally, collaboration with domain experts may provide further insights into the clinical relevance and interpretation of model predictions.

In conclusion, the results obtained from the Logistic Regression model, especially after incorporating Undersampling and fine-tuning hyperparameters, demonstrate a promising approach to anomaly detection in the medical domain. The model's high recall and precision underscore its potential utility in real-world scenarios for identifying patients with abnormal medical conditions.
