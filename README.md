# Cirrohsis_survival
This model predicts patient status at N_Days: C (alive), CL (alive due to liver transplant), and D (deceased), using an ensemble of an Optuna-tuned XGBoost classifier and a neural network. Data is preprocessed with imputation, scaling, and one-hot encoding. Final predictions are blended to minimize log loss via cross-validation.
