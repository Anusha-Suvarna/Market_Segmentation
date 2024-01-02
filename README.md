# Market Segmentation

## Table of Contents

- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Methodology](#methodology)
  - [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
  - [Autoencoders](#autoencoders)
  - [KMeans Clustering](#kmeans-clustering)
- [Usage](#usage)
- [Results](#results)
  - [PCA Results](#pca-results)
  - [Autoencoder Results](#autoencoder-results)
- [Conclusion](#conclusion)

## Introduction

This project aims to segment credit card customers using various techniques like Principal Component Analysis (PCA), Autoencoders, and KMeans clustering. By exploring customer data and applying these methods, it identifies distinct customer groups based on their behavior.

## Dataset Overview

The dataset used in this project is the "Marketing_data.csv" file available in the 'dataset' folder. It contains various features related to credit card usage, such as balance, purchase frequency, credit limit, payments, etc. This dataset was preprocessed and scaled before applying segmentation techniques.

| Feature                      | Description                                  |
|------------------------------|----------------------------------------------|
| Balance                      | Current balance on the credit card           |
| Balance Frequency            | Frequency of updating the balance             |
| Purchases                    | Total amount of purchases made                |
| ...                          | ...                                          |

## Methodology

### Principal Component Analysis (PCA)

The project started with PCA, reducing the dataset's dimensions to two principal components for visualization. The steps involved:

- Data preprocessing: Scaling the features to bring them to a similar scale.
- Applying PCA: Reducing the dimensions to two principal components.
- Visualizing clusters: Plotting the clusters formed after PCA.

### Autoencoders

Autoencoders were used for dimensionality reduction. The process included:

- Setting up the autoencoder model: Configuring layers for encoding and decoding.
- Training the model: Using the autoencoder to learn and compress data.
- Generating encoded values: Extracting reduced dimensions from the trained autoencoder.

### KMeans Clustering

KMeans clustering was employed on both PCA-reduced and autoencoder-generated datasets. Key steps were:

- Determining the optimal number of clusters: Using the elbow method to find the right number of clusters.
- Applying KMeans: Clustering the data into distinct groups based on the identified number of clusters.
- Visualizing clusters: Plotting clusters based on the reduced dimensions from PCA and autoencoders.

## Usage

To run this project:

1. Ensure Python environment with required libraries is set up.
2. Clone the repository.
3. Access the 'dataset' folder and place the 'Marketing_data.csv' file.
4. Use the Jupyter Notebook 'Project_Credit_Card_Segmentation.ipynb' to execute the code step-by-step.

## Results

### PCA Results

- Identified clusters: A total of 8 clusters were identified using PCA.
- Cluster distribution: Cluster distribution ranged from 30 records to 2723 records.

### Autoencoder Results

- Reduced dimensions: The autoencoder reduced the dataset to 10 dimensions.
- Cluster distribution: Clustering based on autoencoder-generated dimensions resulted in 4 clusters with varying sizes.

## Conclusion

The project successfully segmented credit card customers into distinct groups based on their behavior using PCA, autoencoders, and KMeans clustering. The identified clusters can be used for targeted marketing strategies, personalized customer experiences, or risk assessment.
