# Ransomware Detection Using Machine Learning

## Project Overview
This project implements a binary classification system to detect ransomware and benign executables using machine learning. The model analyzes static binary features extracted from Windows PE (Portable Executable) files to classify them as either ransomware or benign software.

## Dataset
Source: Kaggle - Ransomware Detection Dataset
Target Variable: Benign (0 = Ransomware, 1 = Benign)
Features: PE file characteristics (MajorImageVersion, MajorOSVersion, NumberOfSections, ResourceSize, DllCharacteristics, etc.)
Split: 80% Training, 20% Testing (stratified to maintain class balance)

## Project Objectives
-  Explore and analyze binary features from PE files
-  Preprocess and scale numerical features
-  Train multiple machine learning classifiers
-  Compare model performance and identify the best detector
-  Generate comprehensive evaluation metrics and visualizations

## Technology Stack
-  Language: Python 3.x
-  Libraries:
    Data Processing: NumPy, Pandas
    Visualization: Matplotlib, Seaborn
    ML Models: Scikit-learn, XGBoost
-  Metrics: Classification Report, Confusion Matrix

## Project Workflow
1. Exploratory Data Analysis (EDA)
  Dataset shape, columns, and data types
  Missing value detection
  Statistical summaries and distributions
  Feature correlation analysis
  Target variable distribution (countplot)
  Numerical feature distributions (histograms, boxplots)

2. Data Preprocessing
  Drop non-predictive features: FileName, md5Hash
  Separate features (X) and target (y)
  Train-test split: 80/20 with stratification
  Feature scaling using StandardScaler

3. Model Training
  Four classifiers trained in parallel:
  Random Forest: Ensemble method with decision trees
  XGBoost: Gradient boosting with optimized parameters
  Support Vector Machine (SVM): Kernel-based classification
  Artificial Neural Network (ANN/MLP): Deep
