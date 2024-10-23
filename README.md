# Elucidating governing factors of PFAS removal by polyamide membranes using machine learning and molecular simulations

This file is the guidance for running XGboost and multimodal transformer models for predicting PFAS rejections by nanofiltration and reverse osmosis membranes. All the codes were run and tested on Google Colab. Jupyter noteboook or other Python integrated development environments (IDE)/code editor can also be used to run the codes.

## Overview

The transformer and XGBoost models aim to predict the PFAS removal rates by NF and RO membranes. The models are trained on PFAS removal rate dataset obtained from the literature. The data from the literature were used for training while the experimental results obtained from our own experiments were used for testing. During the training, 5-fold cross validation was used by stratifying the data based on their sources. In this way, the inclusion of data points from the same paper is avoided, preventing data leakage. We assigned 'ref_ID' 1 to our experimental data. The training data and testing data can be split by including/exclusing the data with 'ref_ID' = 1. 

## Version

```
Python version: 3.10.12
SHAP version: 0.44.0
RDKit version: 2023.09.3
Tensorflow version: 2.14.0
hyperopt version: 0.2.7
```

## Ownwers
Nohyeong Jeong, njeong6@gatech.edu

## Considerations

## Use Cases
* The models can be used to predict the performance of nanofiltration (NF) and reverse osmosis (RO) based on the membrane properties, PFAS properties, as well as operational conditions.

## Limitations
* Due to the nature of NF and RO membranes, PFAS removal rates obtained from the literature were generally high. Inclusion of low PFAS removal may need to consider other types of membranes, such as ultrafiltration membranes.
