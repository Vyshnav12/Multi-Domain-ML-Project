# Multi-Domain ML Project: Haggis Population Forecasting, Human Activity Recognition, and Medical Image Classification

## Overview

This repository contains three main projects:

1. Haggis Population Forecasting
2. Human Activity Recognition and Clustering
3. Classification of Medical Images (BloodMNIST)

## 1. Haggis Population Forecasting

### Objective
Develop a model to forecast the Haggis population on a specific mountain over a 5-year period, using both precise ground recordings and satellite remote sensing estimates.

### Key Components
- Implementation of a Gaussian basis function
- Development of ridge regression models using gradient descent
- Exploration of different cost functions (sum of squared errors vs. sum of absolute errors)
- Combination of Gaussian and sinusoidal bases to capture annual oscillations
- Optimization of model parameters for accurate forecasting

### Implementation Steps
1. Data preparation and standardization
2. Implementation of Gaussian basis function
3. Gradient descent for ridge regression
4. Implementation of absolute error cost function
5. Development of combined Gaussian and sinusoidal basis function
6. Parameter selection and model evaluation
7. Visualization of results

### Conclusion
The model effectively captures the cyclical pattern of the Haggis population, closely matching the true trend for most of the observed period. It successfully reproduces annual oscillations, demonstrating the effectiveness of the combined Gaussian and sinusoidal basis functions. However, the forecast for the last 12 months shows some divergence, overestimating peaks and underestimating troughs. The model appears robust against outliers in the training data but shows limitations in long-term prediction accuracy.

## 2. Human Activity Recognition and Clustering

### Objective
Analyze the UCI Human Activity Recognition Using Smartphones dataset to uncover patterns and groupings through clustering and dimensionality reduction techniques.

### Dataset
- 561 features representing different aspects of sensor dynamics
- 7352 samples in the training set
- 6 different activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)

### Implementation Steps
1. Data Loading and Exploration
2. Clustering Analysis using K-means
3. Clustering Quality Evaluation using cluster purity
4. Dimensionality Reduction using PCA
5. Visualization of clusters in reduced feature space

### Key Findings
- K-means clustering with 6 clusters was applied
- Average cluster purity: 0.5893
- One well-defined cluster (purity 0.9618) identified
- Other clusters showed mixed activities (purities 0.4680-0.6156)
- PCA was used for dimensionality reduction and visualization

## 3. Classification of Medical Images (BloodMNIST)

### Objective
Implement and compare various classifier models for medical image classification using the BloodMNIST dataset.

### Dataset
- 28x28 RGB images from the BloodMNIST dataset
- Pre-split into training, validation, and test sets

### Implementation Steps
1. Load and preprocess the BloodMNIST dataset
2. Implement Logistic Regression and Multi-Layer Perceptron (MLP) classifiers
3. Train models and optimize hyperparameters
4. Compare performance of different architectures
5. Visualize results and discuss findings

### Conclusion
Both Logistic Regression and MLP models performed well on the BloodMNIST dataset, achieving accuracies above 80%. The MLP (82.13%) slightly outperformed Logistic Regression (80.67%), indicating some benefit from capturing non-linear relationships in the data. The MLP's learning curves showed rapid initial improvement and stable performance, with good generalization. The small performance gap between the models implies that the dataset has strong linear separability, but there are some patterns that benefit from the MLP's non-linear capabilities.

## Requirements

- Python 3.x
- NumPy
- Matplotlib
- Scikit-learn
- PyTorch

## Results

Detailed results and visualizations can be found within each respective notebook.

## Acknowledgements

The UCI Human Activity Recognition Using Smartphones dataset used in this project was obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones).

## License

This project is licensed under the MIT [License](LICENSE).

The UCI HAR dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license.
