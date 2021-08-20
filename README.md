# Cryptocurrencies
## Overview
In this project, we use unsupervised learning to discover patterns and groups in a cryptocurrency dataset that will then help determine what class of cryptocurrencies are tradable. In the initial phase phase we process the dataset for input into the machie learning algorithm, then we would group the data using clustering and K-Means algorithm. Finally, we would make our model more efficient by using the Principal Component Analysis.

## Control Flow
1. Basic Data Processing
    - Read in dataset
    - Keep cryptocurrencies that are traded
    - Keep cryptocurrencies that have a working algorithm
    - Remove rows that have at least one null value
    - Keep rows where cryptocurrencies are mined
2. Data Processing for PCA
    - Create a new DataFrame that holds only the cryptocurrencies names
    - Drop the 'CoinName' column since it's not going to be used on the clustering algorithm.
    - Use get_dummies() to create variables for text features
    - Standardize the data with StandardScaler()
 3. Reducing Data Dimensions Using PCA
    - Use PCA to reduce dimension to three principal components
    - Create a DataFrame with the three principal components.
4. Clustering Crytocurrencies Using K-Means
    - Create an elbow curve to find the best value for K and calculate the inertia for the range of K values
    - Create the elbow curve
    - Run K-Means with K=4
    - Create a new DataFrame including predicted clusters and cryptocurrencies features
5. Visualizing Cryptocurrencies Results
    - Creating a 3D-Scatter with the PCA data and the clusters
    - Create a table with tradable cryptocurrencies.
    - Scale the data to create the scatter plot with tradable cryptocurrencies
    - Create a new DataFrame that has the scaled data with the clustered_df DataFrame index
    - Create a hvplot.scatter plot using x="TotalCoinsMined" and y="TotalCoinSupply".


## Results
