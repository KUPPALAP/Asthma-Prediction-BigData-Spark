# Asthma-Prediction-BigData-Spark

Project Overview

This project leverages Apache Spark to process and analyze a large-scale dataset from Kaggle on asthma disease. The main objectives were to identify the critical factors contributing to asthma diagnosis and develop predictive insights using statistical and machine learning methods. By using Spark, we aimed to efficiently manage and preprocess big data, enabling complex analysis to better understand the influences of lifestyle, environmental, and clinical factors on asthma.


Dataset

The dataset for this project, sourced from Kaggle, contains detailed health information for 2,392 patients, including factors such as age, BMI, diet quality, lung function, and various asthma symptoms.

Technology Stack

Apache Spark: Core framework for big data processing and analytics.

Python & Scikit-learn: For data preprocessing and implementing machine learning models.

Virtual Cluster (VMs): Securely configured VM environment with Michigan Tech’s network, ensuring stable Spark performance across nodes.

Big-IP Edge VPN Client: Used for secure access to the virtual cluster.


Virtual Machine and Network Configuration

We utilized a virtual cluster with Michigan Tech’s VMS setup. Accessing this environment was made secure through the F5 Big-IP Edge VPN client, and configuration adjustments were made to support Spark processing across multiple VMs.

Spark Setup

Spark was installed and configured across the VM nodes (hadoop1 and hadoop2) to support distributed processing. Spark master and worker nodes were defined for efficient task management.

Data Preprocessing Steps

1.Missing Value Handling: Missing values in key variables such as Age, BMI, and lung function metrics were filled to ensure dataset completeness.

2.Categorical Encoding: Converted categorical features (e.g., Gender, PetAllergy) into numerical formats suitable for model input.

3.Scaling & Normalization: Continuous features were scaled using MinMaxScaler to unify ranges across variables.

4.Binning: Continuous variables like Age and BMI were binned to simplify interpretation.

5.Dataset Splitting: Dataset was split into training and testing sets (70:30) to support independent classification and regression tasks.
Statistical Analysis

6.Correlation Analysis: A correlation matrix was created to examine linear relationships among continuous variables, revealing minimal associations.

7.Chi-Square Tests: Explored categorical associations with asthma diagnosis to evaluate statistical significance.

Machine Learning Models

1.Logistic Regression: Achieved 94.8% accuracy for predicting asthma diagnosis.

2.Linear Regression: Modeled lung function based on health factors with an R² score of 1.0.

3.K-Means Clustering: Clustered patient profiles based on continuous variables, identifying distinct health profiles for potential tailored interventions.

Results

Despite some challenges with VM configuration, the project provided valuable insights into asthma risk factors, illustrating the power of Spark in handling large datasets for health analytics. The analysis identified critical patterns in asthma diagnosis and patient grouping, which could inform future predictive healthcare models.


Conclusion

The project successfully demonstrated the applicability of big data tools like Spark in healthcare data analysis, uncovering patterns that can assist in asthma management. Future work could involve exploring non-linear models and integrating additional datasets to enhance predictive accuracy.
