# Market Segmentation
In business, marketing drives growth by building brands, engaging customers, and boosting sales. Yet, knowing what customers want is a big challenge. By understanding them, we create focused marketing that suits their needs. Using customer data, data science helps split customers into groups. The goal is to help the bank's marketing team launch a new product. We're sorting customers into at least three groups to make their advertising more effective for each group's needs.
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

The dataset used in this project is the `Marketing_data.csv` file available in the `Dataset` folder. There are 8950 records in the dataset. It contains various features related to credit card usage, such as balance, purchase frequency, credit limit, payments, etc. This dataset was preprocessed and scaled before applying segmentation techniques.


| Feature                        | Description                                                             |
|--------------------------------|-------------------------------------------------------------------------|
| CUSTID                         | Identification of Credit Card holder                                      |
| BALANCE                        | Balance amount left in customer's account to make purchases                |
| BALANCE_FREQUENCY              | How frequently the Balance is updated, score between 0 and 1              |
| PURCHASES                      | Amount of purchases made from account                                     |
| ONEOFF_PURCHASES               | Maximum purchase amount done in one-go                                    |
| INSTALLMENTS_PURCHASES         | Amount of purchase done in installment                                   |
| CASH_ADVANCE                   | Cash in advance given by the user                                         |
| PURCHASES_FREQUENCY            | How frequently the Purchases are being made, score between 0 and 1        |
| ONEOFF_PURCHASES_FREQUENCY     | How frequently Purchases are happening in one-go, score between 0 and 1   |
| PURCHASES_INSTALLMENTS_FREQUENCY | How frequently purchases in installments are being done, score between 0 and 1 |
| CASH_ADVANCE_FREQUENCY         | How frequently the cash in advance being paid                              |
| CASH_ADVANCE_TRX               | Number of Transactions made with "Cash in Advance"                         |
| PURCHASES_TRX                  | Number of purchase transactions made                                      |
| CREDIT_LIMIT                   | Limit of Credit Card for user                                              |
| PAYMENTS                       | Amount of Payment done by user                                            |
| MINIMUM_PAYMENTS               | Minimum amount of payments made by user                                   |
| PRC_FULL_PAYMENT               | Percent of full payment paid by user                                      |
| TENURE                         | Tenure of credit card service for user                                     |

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

### K-Means Clustering

K-Means clustering was employed on both PCA-reduced and autoencoder-generated datasets. 
#### Key steps were:

- Determining the optimal number of clusters: Using the elbow method to find the right number of clusters.
- Applying KMeans: Clustering the data into distinct groups based on the identified number of clusters.
- Visualizing clusters: Plotting clusters based on the reduced dimensions from PCA and autoencoders.

## Usage

To run this project:

1. Ensure Python environment with required libraries is set up.
2. Clone the repository.
3. Access the `Dataset` folder with `Marketing_data.csv` file.
4. Use the Jupyter Notebook `Market Segmentation_.ipynb' to execute the code step-by-step.

## Results

### PCA Results

- Identified clusters: A total of 8 clusters were identified using PCA.
- Cluster distribution: Cluster distribution ranged from 30 records to 2723 records.

### Autoencoder Results

- Reduced dimensions: The autoencoder reduced the dataset to 10 dimensions.
- Cluster distribution: Clustering based on autoencoder-generated dimensions resulted in 4 clusters with varying sizes.

## Conclusion

The project successfully segmented credit card customers into distinct groups based on their behavior using PCA, autoencoders, and KMeans clustering. The identified clusters can be used for targeted marketing strategies, personalized customer experiences, or risk assessment.
