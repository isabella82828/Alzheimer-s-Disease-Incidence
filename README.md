# Alzheimer's Disease Incidence Model

## Project Overview 

This project consists of two complementary models aimed at enhancing Alzheimer’s Disease (AD) diagnostics:

- __📊 Cost-Effective Predictor Selection Model:___ Identifies a minimal set of diagnostic predictors that optimize both accuracy and cost-effectiveness, reducing the need for costly testing procedures.
- __🔍 Alzheimer’s Detection Model:__ Uses these predictors in a bidirectional LSTM-based model to detect Alzheimer's Disease and assess the likelihood of AD progression.

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

## Conclusions
### Cost-Effective Predictor Selection Model:
- __Model Performance:__ The multinomial logistic regression model achieved a training set accuracy of 0.855, validation set accuracy of 0.830, and test set accuracy of 0.754. This represents the final model's ability to classify patients into different stages of Alzheimer's Disease based on the selected predictors.
- __Cost vs. Accuracy Trade-off:__ The analysis revealed that while some predictor bundles (e.g., ECogPT and MMSE) did not significantly impact accuracy, others showed varied contributions. Genetic testing stood out as a cost-effective early-stage predictor, improving model accuracy by 0.025 with a relatively low cost.
- __Predictor Importance:__ PET scans, despite their high cost, did not contribute significantly to predictive accuracy. On the other hand, ADAS provided a notable accuracy improvement (> 0.03) but was associated with higher costs due to late-stage detection.
  
### Alzheimer’s Detection Model:
-__Detection Accuracy__:The Bidirectional LSTM model captured forward and backward temporal dependencies in patient biomarker data, yielding an overall diagnostic accuracy of 93% for detecting Alzheimer's Disease progression.
- __Robustness:__ The model's use of a diverse set of biomarkers, including neuroimaging and CSF data, contributed to its comprehensive evaluation capabilities, ensuring a balanced approach to disease prediction.
- __Model Strengths:__ The model's architecture leveraged temporal data, allowing it to identify subtle changes over time that are critical for early detection and monitoring of Alzheimer's Disease. The bidirectional structure enhanced the model's capacity to learn from past and future data points in the sequence.

## Future Improvements 
- __Expanded Feature Set:__ Include additional predictors such as lifestyle and environmental factors, cognitive test scores, and advanced imaging metrics to improve predictive power and better reflect the nature of Alzheimer's Disease.
- __Longitudinal Data Integration:__ Incorporate more comprehensive longitudinal analyses, such as repeated measures of biomarkers over extended periods, to improve disease progression prediction.


