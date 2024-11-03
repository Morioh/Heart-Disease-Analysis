# Heart Disease Clustering and Analysis

This project focuses on clustering and analyzing the **Heart Disease Dataset** from the UCI Machine Learning Repository. The dataset contains 303 instances with 14 attributes, including age, sex, chest pain type, blood pressure, serum cholesterol, and a target variable indicating the presence or absence of heart disease.

The analysis involves clustering patients based on their medical history, identifying potential risk factors for heart disease, and evaluating the performance of various clustering algorithms.

## Table of Contents

- [Heart Disease Clustering and Analysis](#heart-disease-clustering-and-analysis)
  - [Table of Contents](#table-of-contents)
  - [Project Overview](#project-overview)
  - [Dataset](#dataset)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Data Preprocessing](#data-preprocessing)
  - [Clustering Algorithms Applied](#clustering-algorithms-applied)
    - [K-means Clustering](#k-means-clustering)
    - [Hierarchical Clustering](#hierarchical-clustering)
    - [DBSCAN](#dbscan)
  - [Dimensionality Reduction](#dimensionality-reduction)
  - [Model Evaluation](#model-evaluation)
  - [Installation and Usage](#installation-and-usage)

## Project Overview

The objective of this project is to cluster patients based on their medical history to gain insights into groups that may be at higher risk for heart disease. We employed several clustering algorithms, including **K-means**, **Hierarchical Clustering**, and **DBSCAN** to create patient clusters. Additionally, **Gaussian Mixture Models (GMMs)** were applied to identify risk factors associated with heart disease.

To evaluate the clustering algorithms, metrics such as the **Davies-Bouldin Index** and **Silhouette Score** were used. **Principal Component Analysis (PCA)** and **t-SNE** were employed to visualize the clusters and examine the relationships between variables.

## Dataset

The heart disease dataset used in this project contains the following 14 attributes:

- **Age**: Patient's age in years
- **Sex**: Gender (1 = male, 0 = female)
- **cp**: Chest pain type (categorical)
- **trestbps**: Resting blood pressure (mm Hg)
- **chol**: Serum cholesterol (mg/dl)
- **fbs**: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- **restecg**: Resting electrocardiographic results (categorical)
- **thalach**: Maximum heart rate achieved
- **exang**: Exercise-induced angina (1 = yes, 0 = no)
- **oldpeak**: ST depression induced by exercise relative to rest
- **slope**: Slope of the peak exercise ST segment (categorical)
- **ca**: Number of major vessels colored by fluoroscopy
- **thal**: Thalassemia (categorical)
- **target**: Presence or absence of heart disease (1 = disease, 0 = no disease)

## Exploratory Data Analysis (EDA)

Before clustering, exploratory data analysis was conducted to understand the feature distributions and relationships. The EDA includes:

- Descriptive statistics
- Correlation matrix to identify relationships between variables
- Visualization of key features using histograms and box plots

## Data Preprocessing

To prepare the dataset for clustering, the following preprocessing steps were applied:

- Handled missing values by imputing or removing them
- Scaled numerical features using **StandardScaler** to normalize the data
- Encoded categorical variables using **one-hot encoding**

## Clustering Algorithms Applied

### K-means Clustering
- Optimized the number of clusters (k) using the **Elbow Method** and **Silhouette Score**.
- Applied K-means clustering with **k=5** and **k-means++ initialization**.

### Hierarchical Clustering
- Applied **agglomerative hierarchical clustering** and evaluated the clusters formed.

### DBSCAN
- Applied **Density-Based Spatial Clustering** to group patients based on density.

## Dimensionality Reduction

To reduce dimensionality and visualize clusters, we used **PCA** and **t-SNE**:

- **PCA** helped explain the variance of different components and how the features contributed to clustering.
- **t-SNE** provided a non-linear embedding of the clusters, giving additional insights into how the clusters were formed.

## Model Evaluation

To evaluate clustering performance, the following metrics were used:

- **Davies-Bouldin Index**: A lower value indicates better clustering.
  - K-means: 1.94
  - Hierarchical Clustering: 2.02
  - GMM: 2.01

- **Silhouette Score**: Measures the similarity of each point to its own cluster compared to others.
  - K-means: 0.20
  - Hierarchical Clustering: 0.19
  - GMM: 0.13

Based on these results, **K-means** performed slightly better than the other algorithms, with a higher Silhouette Score (0.20) and a slightly lower Davies-Bouldin Index (1.94). 

---


While **K-means** performed marginally better, the low Silhouette Scores and high Davies-Bouldin Indexes across all algorithms suggest that the data could have gotten a clearer, well-defined clustering structure in the preprocessing phase.

## Installation and Usage

1. Clone the repository.
2. Install dependencies listed in `requirements.txt`.
3. Run the analysis scripts to reproduce clustering and visualization results.

```bash
git clone <repository-url>
cd heart-disease-clustering
pip install -r requirements.txt
