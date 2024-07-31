# Deep Learning for Bankruptcy Prediction

## Introduction
This project focuses on using deep learning techniques to improve company bankruptcy prediction. The primary objective is to develop an effective neural network model that accurately predicts bankruptcy, emphasizing the Recall metric. The dataset used for this project includes financial data from the Taiwan Economic Journal, covering the years 1999 to 2009.

## Project Overview
### Objective
The goal is to identify the best neural network model for predicting bankruptcy, particularly optimizing for Recall. This metric is crucial as it minimizes false negatives, which are instances where bankrupt companies are incorrectly classified as non-bankrupt.

### Data Characteristics
- **Source**: Taiwan Economic Journal (1999-2009)
- **Size**: 6819 rows and 96 features
- **Challenge**: High imbalance with only 3.2% positive bankruptcy cases

### Methodology
1. **Data Exploration**
   - Ensured data quality with no missing or duplicated values.
   - Addressed the class imbalance using the SMOTE technique to balance the training dataset.
   - Analyzed feature correlations to avoid overfitting.

2. **Feature Selection**
   - Reduced the feature set from 96 to 20 using correlation analysis and domain knowledge.
   - Applied mutual information analysis to identify the most informative features.

3. **Initial Neural Network Model**
   - Developed a Multilayer Perceptron (MLP) with varying numbers of hidden layers.
   - Tested different configurations, ultimately finding the best recall results with models using 4 and 6 hidden layers.
   - Implemented LeakyReLU activation to handle data noise and outliers effectively.

4. **Model Optimization Techniques**
   - Utilized early stopping and dropout regularization to enhance model performance.
   - Early stopping helped prevent overfitting by halting training when validation performance plateaued.
   - Dropout regularization improved model generalization by randomly deactivating neurons during training.

5. **Hyperparameter Tuning**
   - Applied grid and random search techniques to optimize hyperparameters.
   - Identified the best node configurations, further improving model performance.

### Results
The final model, with optimized hyperparameters, achieved high accuracy, recall, and precision. Specifically, the model demonstrated an F1-score of 0.95, with a precision of 0.96 and recall of 0.93 on the test dataset. These results indicate the model's effectiveness in correctly identifying companies at risk of bankruptcy.

### Discussion
The project demonstrates the potential of deep learning techniques in financial risk assessment. By carefully selecting features, balancing the dataset, and optimizing model parameters, the developed neural network effectively predicts bankruptcy, minimizing false negatives.

### Conclusion and Future Work
This project highlights the importance of deep learning in enhancing bankruptcy prediction models. The findings show that increasing the number of hidden layers and nodes, along with hyperparameter tuning, significantly improves model performance. Future research can explore alternative neural network architectures, incorporate additional data sources, and investigate advanced deep learning techniques to further enhance predictive accuracy.

