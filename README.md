# Cirrohsis_survival
This model predicts patient status at N_Days: C (alive), CL (alive due to liver transplant), and D (deceased), using an ensemble of an Optuna-tuned XGBoost classifier and a neural network. Data is preprocessed with imputation, scaling, and one-hot encoding. Final predictions are blended to minimize log loss via cross-validation.
This project aims to predict the survival status of patients at a specific time (N_Days). The model predicts three possible statuses:  
C: Patient is alive at N_Days.  
CL: Patient is alive at N_Days due to a liver transplant.  
D: Patient is deceased at N_Days.  
The prediction is based on clinical data, and the solution combines XGBoost and a Neural Network model to classify the status, leveraging ensemble learning for enhanced performance.  

# Model Overview

Approach:  
XGBoost Classifier: An optimized decision-tree-based model tuned using Optuna for hyperparameter optimization.  
Neural Network: A deep learning model with multiple dense layers and dropout regularization to prevent overfitting.  
Ensemble Learning: The final prediction is a weighted average of the predictions from the XGBoost and Neural Network models, optimized for minimal log loss.  
Key Features:  
Data Preprocessing: Handling of missing values, scaling of numerical features, and one-hot encoding for categorical variables.  
Cross-validation: Stratified k-fold cross-validation for model evaluation, ensuring robust performance across different data splits.  
Model Tuning: Hyperparameters for XGBoost are optimized using Optuna, and the final ensemble weights are determined via cross-validation.  

# Results

The model predicts the probability of each status (C, CL, D) for the test dataset.   
Model Performance Summary:  
XGBoost - Average log loss: 0.3606 ± 0.0111  
Neural Network - Average log loss: 0.4093 ± 0.0117  

Ensemble Results:  
Optimal weights: XGBoost = 0.90, NN = 0.10  
Ensemble validation log loss: 0.3604  


# Tech Stack  

Python for the implementation.  
XGBoost for the classification model.  
TensorFlow (Keras) for the neural network model.  
Optuna for hyperparameter tuning.  
scikit-learn for preprocessing, splitting, and evaluation.  
# Author  
Malavika  
