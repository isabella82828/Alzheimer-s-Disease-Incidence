# Alzheimer's Disease Incidence

## Project Overview 

This project consists of two complementary models aimed at enhancing Alzheimer’s Disease (AD) diagnostics:

- Cost-Effective Predictor Selection Model: Identifies a minimal set of diagnostic predictors that optimize both accuracy and cost-effectiveness, reducing the need for costly testing procedures.
  
- Alzheimer’s Detection Model: Uses these predictors in a bidirectional LSTM-based model to detect Alzheimer's Disease and assess the likelihood of AD progression.


## Models
### Cost-Effective Predictor Selection Model
This model evaluates and ranks various biomarkers based on their diagnostic value and cost-efficiency. It uses statistical and feature selection methods to identify a minimal set of predictors that maintain high diagnostic accuracy while reducing the cost of clinical testing.

Key Predictors Identified:

- Neuroimaging Metrics: Brain volume, hippocampal atrophy, cortical thickness.
- CSF Biomarkers: Amyloid beta, total tau, phosphorylated tau.
- Genetic Markers: APOE ε4 allele presence.
- Inflammatory Markers: YKL-40, C-Reactive Protein (CRP).
- Blood-Based Biomarkers: Neurofilament light chain (NfL).

### Alzheimer’s Detection Model
This model employs a Bidirectional LSTM architecture to analyze longitudinal patient data. It processes sequences over time, capturing temporal dependencies that are crucial for predicting Alzheimer’s progression.

Architecture:
- Bidirectional LSTM Layers: Captures forward and backward temporal patterns in patient biomarker data.
- Output Layer: Sigmoid activation for binary classification (Alzheimer’s vs. Normal).
