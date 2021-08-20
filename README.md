# Cryptocurrencies
## Overview
In this project, we use unsupervised learning to discover patterns and groups in a cryptocurrency dataset that will then help determine what class of cryptocurrencies are tradable. In the initial phase phase we process the dataset for input into the machie learning algorithm, then we would group the data using clustering and K-Means algorithm. Finally, we would make our model more efficient by using the Principal Component Analysis.

### Control Flow
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
##### One-Hot Encoding
![One_Hot_Encoding](https://user-images.githubusercontent.com/67847583/130296075-ca2d0343-d4b6-44b0-8a8b-70ae13ff271f.png)

##### Principal Component Analysis DataFrame
![PCA_DataFrame](https://user-images.githubusercontent.com/67847583/130296136-ebc34e65-8ae0-43cf-ae63-62bfeeb89010.png)

##### Elbow Curve
![Elbow_Curve](https://user-images.githubusercontent.com/67847583/130296208-4132f4c7-d283-4a83-bd13-27f0d827a09c.png)

##### 3D-Scatter with the PCA data and the clusters
![3D_Scatter](https://user-images.githubusercontent.com/67847583/130296376-bb30fa4f-00d5-4ac8-ae6c-35bdb20b7f8f.png)

##### Hvplot Table with tradable cryptocurrencies
![Hvplot_Table](https://user-images.githubusercontent.com/67847583/130296438-8ca299f6-269b-4698-a9ba-22005da61143.png)

##### Hvplot Scatter plot using x="TotalCoinsMined" and y="TotalCoinSupply".
![Hvplot_Scatter](https://user-images.githubusercontent.com/67847583/130296532-24f567ea-ad03-43b0-8ed1-aaa31150d64e.png)


### Summary
After initial data processing, converting text features to dummy variables, and standardizing the crypto dataset with StandardScaler(), we are able to reduce the dimensions of the data to three componenets using PCA.
Our elbow curve determined that our optimal number of clusters is K=4. Using K=4, we create four clusters. We notice that one of the clusters has only one cryptocurruency. We may further evaluate this data point to determine if it may be dropped.
Finally we create a hvplot table showing our final cryptocurrencies and their classes, and a 2D-scatter plot showing TotalCoinedMined and TotalCoinsSupplied. Similar to the 3D-Scatter plot, our 2D-Scatter plot show that we have one outlier cryptocurrency
