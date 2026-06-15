# ICU Mortality Prediction using Machine Learning

This project focuses on predicting in-hospital mortality for Intensive Care Unit (ICU) patients diagnosed with heart failure using machine learning models. The goal is to explore how predictive analytics can support early risk stratification in critical care settings.

---

## 1. Project Overview

This project investigates whether machine learning models can predict patient survival outcomes in the ICU using structured clinical data such as demographics, laboratory measurements, comorbidities, and vital signs.

The motivation is to support clinical decision-making by identifying high-risk patients early and improving healthcare resource allocation.

---

## 2. Dataset

The dataset is derived from ICU patient records and is based on the MIMIC-III critical care database (Beth Israel Deaconess Medical Center).

- Number of patients: ~1,100  
- Number of features: 50+ clinical variables  
- Task: Binary classification (mortality prediction)

### Feature Categories:
- Demographics (age, gender)
- Laboratory results (e.g., calcium levels)
- Comorbidities (e.g., diabetes)
- ICU vital signs and clinical measurements

---

## 3. Methodology

The project was implemented in Python using Scikit-learn and PyCaret.

### 3.1 Data Preprocessing
- Missing values handled using mean imputation (initially)
- Improved using K-Nearest Neighbors (KNN) imputation (k=5)
- Feature scaling applied where necessary

### 3.2 Train-Test Split
- 70% training set
- 30% testing set

(using `train_test_split` from Scikit-learn)

---

## 4. Models Implemented

Several machine learning models were evaluated:

### 4.1 Multi-Layer Perceptron (MLP)
- Initial neural network baseline
- Performance: ~40% accuracy
- Limited performance due to dataset structure

### 4.2 Decision Tree
- Captures non-linear relationships
- Strong improvement over baseline model

### 4.3 Random Forest
- Ensemble of decision trees
- Improved accuracy by ~5% over single decision tree
- More robust and stable predictions

### 4.4 Naive Bayes
- Fast probabilistic model
- Strong performance on imbalanced data
- High recall for mortality prediction

### 4.5 AutoML (PyCaret)
- Automated model comparison
- Ridge Classifier achieved highest accuracy
- Naive Bayes performed best in recall and F1-score

---

## 5. Evaluation Metrics

Due to class imbalance, multiple evaluation metrics were used:

- Accuracy  
- Precision  
- Recall  
- F1-score  

**Key insight:** Accuracy alone is not sufficient in healthcare prediction tasks.

---

## 6. Key Insights

- Class imbalance significantly impacts model evaluation
- Tree-based models outperform simple neural networks on structured clinical data
- Naive Bayes performs well in detecting minority (mortality) cases
- F1-score and recall are more meaningful than accuracy in clinical prediction tasks

---

## 7. Limitations

- Dataset is based on a single hospital system (MIMIC-III)
- External validation is required for generalization
- Clinical interpretability and ethical validation are necessary before real-world use
- This project is for research and educational purposes only

---

## 8. Conclusion

This project demonstrates the application of machine learning techniques for ICU mortality prediction using structured healthcare data. The results highlight the importance of model interpretability and appropriate evaluation metrics in medical AI applications.

Future work may include:
- Feature engineering improvements
- Deep learning models
- Multi-hospital validation
- Explainable AI techniques (e.g., SHAP)

---

## 9. References

- MIMIC-III Clinical Database (PhysioNet)
- Kaggle: In-Hospital Mortality Prediction Dataset
- PyCaret AutoML Framework
- Research literature on ICU mortality prediction using machine learning
