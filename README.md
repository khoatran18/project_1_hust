# Chronic Kidney Disease Prediction System

## Overview  

Chronic Kidney Disease (CKD) is a progressive condition that often develops without clear early symptoms, making timely diagnosis challenging. Clinical diagnosis relies on multiple laboratory indicators and complex interpretation, which can delay detection and treatment.  

This project presents a machine learning–driven prediction system designed to assist early CKD identification by leveraging clinical test data. The system focuses on building a robust end-to-end predictive pipeline that transforms raw medical data into reliable diagnostic insights while maintaining statistical validity and model interpretability.

---

## Problem Statement  

Medical datasets typically exhibit several challenges:

- Heterogeneous feature types (numerical lab results and categorical clinical indicators)  
- Missing and noisy measurements  
- Class imbalance between CKD and non-CKD patients  
- Complex non-linear relationships between biomarkers  

These issues can significantly degrade model performance if not handled systematically. The goal of this project is to design a data processing and modeling framework that preserves clinical information while improving predictive accuracy and generalization.

---

## System Approach  

The system is built as a structured ML pipeline consisting of data standardization, preprocessing, feature analysis, and model training stages.

### Data Standardization  

The original dataset is converted from ARFF format into a machine-learning–ready structure. This step ensures compatibility with modern data processing libraries and establishes a consistent schema for downstream processing.

---

### Data Preprocessing Strategy  

To maintain statistical integrity and reduce bias, the pipeline applies tailored preprocessing techniques:

- **Missing Value Handling**  
  - Numerical features are imputed using K-Nearest Neighbors to preserve multivariate relationships  
  - Categorical features are filled using the most frequent category  

- **Feature Scaling**  
  Numerical attributes are standardized to normalize measurement ranges and stabilize model optimization  

- **Feature Selection**  
  Statistical significance testing (p-value thresholding) is used to retain clinically relevant predictors and remove noise  

- **Class Imbalance Mitigation**  
  SMOTE is applied to generate synthetic minority samples, improving the model’s ability to detect CKD cases  

---

## Modeling Strategy  

Multiple machine learning models are evaluated to capture different data characteristics:

- Linear models for global decision boundaries  
- Distance-based models for local similarity patterns  
- Tree-based and ensemble models for non-linear relationships  

This comparative approach ensures a balanced assessment of predictive performance and robustness.

---

## Key Mechanisms  

- End-to-end data transformation pipeline ensuring reproducibility  
- Statistically grounded preprocessing to maintain clinical relevance  
- Balanced learning strategy to reduce false negatives  
- Model evaluation using accuracy, precision, recall, and F1-score  
- Interpretability considerations for clinical applicability  

---

## Outcome  

The system demonstrates that combining rigorous preprocessing with diverse modeling techniques can significantly improve CKD prediction reliability.  
Results highlight strong performance in recall and F1-score, indicating effective detection capability while maintaining balanced classification behavior.

The project provides a practical framework for applying machine learning to medical decision support scenarios, emphasizing data quality, interpretability, and generalization.
