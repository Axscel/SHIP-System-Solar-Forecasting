# SHIP-System-Solar-Forecasting

This repository contains the MATLAB codes for the various machine learning models used to forecast solar energy generation from a Solar Heat for Industrial Process (SHIP) system, described in the paper...

The paper compares several regression methods (SVR, Decision Tree, Random Forest, XGBoost, ANN, LSTM) and three hybrid LSTM variants tuned with GA, PSO, and SSA. It focuses on 1-hour ahead forecasting of useful and delivered solar thermal energy from a large SHIP installation in Johor Bahru, Malaysia.

# Hyperparameters
All of the models were created in MATLAB. The hyperparameters for each model are outlined below.

## Support Vector Regression (SVR) Model
| Hyperparameter | Setting |
| :------ | :---------: |
| Kernel   | Gaussian (RBF) |
| Epsilon  | 0.1 (Default)   |
| BoxConstraint   | 1 (Default) |
| Standardize   | True |

## Decision Tree Model
| Hyperparameter | Setting |
| :------ | :---------: |
| MinLeafSize   | 5 |
| Split Criterion  | MSE   |

## Random Forest Model
| Hyperparameter | Setting |
| :------ | :---------: |
| NumTrees   | 100 |
| OOB Prediction  | enabled   |

## eXtreme Gradient Boosting (XGBoost) Model
| Hyperparameter | Setting |
| :------ | :---------: |
| MaxNumSplits   | 5 |
| NumLearningCycles  | 100   |

## Artificial Neural Network (ANN) Model
| Hyperparameter | Setting |
| :------ | :---------: |
| Input Dimensions   | 4 |
| Hidden Layer  | 1 (10 Neurons)   |
| Training   | Levenberg–Marquardt |
| Batch Size   | Full Training Set (693) |
| MaxEpochs   | 1000 (with early stopping |

## Long Short-Term Memory (LSTM) Model
| Hyperparameter | Setting |
| :------ | :---------: |
| Input Dimensions   | 4 |
| LSTM Layer  | 1   |
| LSTM Hidden Units  | 151   |
| Look-back Step   | 1 |
| Optimizer  | Adam   |
| Initial Learning Rate  | 0.0038   |
| GradientThreshold  | 1   |
| Learning Rate Schedule   | Drop every 85 epochs |
| Learning Rate Drop Factor   | 0.9613 |
| MaxEpochs   | 205 |
| Mini-batch Size   | 128 |
