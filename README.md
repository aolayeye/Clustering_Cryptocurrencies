# Cryptocurrencies
## Overview
In this project, we use unsupervised learning to discover patterns and groups in a cryptocurrency dataset that will then help determine what class of cryptocurrencies are tradable. In the initial phase phase we process the dataset for input into the machie learning algorithm, then we would group the data using clustering and K-Means algorithm. Finally, we would make our model more efficient by using the Principal Component Analysis.

## Control Flow
1. Data Processing
    - Read in dataset
    - Keep cryptocurrencies that are traded
    - Keep cryptocurrencies that have a working algorithm
    - Remove rows that have at least one null value
    - Keep rows where cryptocurrencies are mined
2. Create a new DataFrame that holds only the cryptocurrencies names
3. Drop the 'CoinName' column since it's not going to be used on the clustering algorithm.
4. Use get_dummies() to create variables for text features
5. Standardize the data with StandardScaler()
