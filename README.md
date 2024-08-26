# Gender-prediction-from-functional-connectivity

## Project Overview

This project aims to predict the gender of subjects using functional connectivity patterns derived from resting-state fMRI data. The project uses the **ABIDE dataset**, which contains collected resting-state functional magnetic resonance imaging (rs-fMRI) data. Only control subjects were included in this analysis. The project use the **AAL (Automated Anatomical Labeling)** atlas to define 116 regions of interest (ROIs) in the brain.

The goal was to build a **Support Vector Machine (SVM)** model, to test whether rfMRI functional connectivity (FC) can be used to predict gender and identify FC features that are most predictive of gender. A total of **468 subjects** were included in the analysis.

## Dataset

- **Dataset**: ABIDE (Autism Brain Imaging Data Exchange) dataset
- **Number of subjects**: 468
- **Type of data**: Resting-state fMRI
- **Atlas**: AAL (Automated Anatomical Labeling) atlas with 116 regions of interest (ROIs)

## Methods

### Preprocessing and Data Splitting
- **Data Splitting**: The data was split into training and testing sets.
- **Class Imbalance Handling**: The dataset was imbalanced with respect to gender, and **undersampling** was applied to the training data to address this imbalance.

### Model

- **Algorithm**: Support Vector Machine (SVM)
- **Features**: Functional connectivity between pairs of ROIs

### Results

- **Accuracy**: The SVM model achieved **68% accuracy** on the test data.

The model showed a significant discrepancy between precision and recall for predicting female subjects. The model was able to **identify female subjects** (higher recall: 0.67) but struggled to **predict them correctly** (lower precision: 0.33). Conversely, predictions for male subjects showed both high precision and recall (0.90 - 0.68). Permutation tests confirmed that gender prediction was reliable ( p<.05)

### Feature Importance

To interpret the model, **SVM coefficients** were used to identify the most important functional connections that contributed to the gender prediction. The analysis revealed the following key findings:

- **fronto‐parietal and sensorimotor networks** were among the most important regions, which aligns with findings in the literature regarding gender differences in brain structure and function (zhang 2018).

## Conclusion

This project demonstrates that functional connectivity patterns in the brain can be used to predict gender with moderate accuracy. However, the model shows limitations in accurately predicting female subjects, as reflected by the low precision for that class.
