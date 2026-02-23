# Medical Assistant – Clinical Decision Support Modeling System  

## Executive Summary  
Modern healthcare environments face increasing patient volume, documentation burden, and diagnostic complexity. This project delivers a machine learning–driven clinical decision-support pipeline designed to assist medical professionals in risk stratification, triage prioritization, and outcome prediction using structured patient data.

The system is built with production-grade considerations in mind, including data integrity validation, class imbalance handling, calibrated probability outputs, and interpretability to ensure responsible integration into healthcare workflows.

This is a **decision-support system**, not a diagnostic authority.

---

## Business Objective  
Develop a clinically aligned classification system that:

- Accurately estimates risk probability across patient cases  
- Produces **reliable probability estimates**, not just class predictions  
- Supports triage prioritization and intervention planning  
- Maintains interpretability suitable for healthcare review  

This project prioritizes **clinical reliability and safety over pure performance metrics**.

---

## Data Overview  
- Structured patient-level health records  
- Mixed numeric and categorical features including:
  - Vital signs  
  - Laboratory values  
  - Demographic information  
  - Clinical indicators  
- Potential class imbalance between low-risk and high-risk outcomes  
- Sensitivity to missing data and real-world variability  

---

## Technical Approach  

### 1. Data Integrity & Preprocessing  
- Canonical schema validation  
- Robust missing value handling  
- Feature scaling and encoding  
- Outlier detection and normalization  
- Defensive preprocessing to prevent leakage  

### 2. Class Imbalance Strategy  
- SMOTE or weighted training strategies  
- Stratified cross-validation  
- Evaluation metrics chosen to reflect minority-class sensitivity  

### 3. Model Development  
Models evaluated include:
- Logistic Regression (interpretability baseline)  
- Gradient Boosting frameworks  
- Tree-based ensemble models  

All models were trained using **stratified cross-validation** to preserve outcome distributions.

### 4. Probability Calibration  
Because healthcare decisions require calibrated confidence:

- Platt scaling and Isotonic regression applied  
- Calibration curves evaluated alongside ROC and PR metrics  
- Outputs optimized for threshold-based triage policies  

---

## Evaluation Framework  
Performance assessed using:

- ROC-AUC for ranking quality  
- Precision–Recall curves for high-risk sensitivity  
- Calibrated probability reliability  
- Confusion matrices at clinically meaningful thresholds  

This ensures the model supports **responsible decision support**, not blind automation.

---

## Key Findings  
- Certain physiological indicators significantly influence predicted risk  
- Probability calibration materially improves downstream decision confidence  
- Interpretable models enhance clinician trust and auditability  
- High recall at calibrated thresholds improves early intervention strategy  

---

## Limitations  
- Historical clinical bias may influence model outputs  
- Temporal drift in patient populations may affect generalization  
- This system is **advisory only**, not a replacement for licensed medical judgment  

---

## Next Steps  
- Temporal validation across admission periods  
- Fairness audits across demographic segments  
- Integration with EMR-compatible pipelines  
- Policy-aware RAG system for guideline contextualization  
- Deployment as a triage-support microservice  

---

## View Modeling
[![View Model](https://img.shields.io/badge/View-Live%20Model-0A66C2?logo=githubpages&logoColor=white)](https://aineuroforge.github.io/Medical-Assistant-RAG-Pipeline/)

---

## Project Context
This project was completed as part of the **Advanced Machine Learning curriculum** in the  
**UT Austin / Great Learning Post Graduate Program in AI & ML** and has been refactored and extended into a **portfolio-grade Retrieval-Augmented Generation (RAG) clinical decision-support system**.

[View Medical Assistant Project in ePortfolio](https://www.mygreatlearning.com/eportfolio/christopher-gonzalez-mejias)
