## Before You Begin

Create a new repository for this project called CryptoClustering. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Push your changes to GitHub.

### Instructions

1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

2. Load the crypto_market_data.csv into a DataFrame.

3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

### Prepare the Data

1. Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

2. Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

3. The first five rows of the scaled DataFrame should appear as follows:

   ![Scaled DataFrame](https://github.com/Weekes-Rod/CryptoClustering/blob/main/scaled_DataFrame.png?raw=true)


### Find the Best Value for k Using the Original Scaled DataFrame

1. Use the elbow method to find the best value for k using the following steps:

   - Create a list with the number of k values from 1 to 11.
   - Create an empty list to store the inertia values.
   - Create a for loop to compute the inertia with each possible value of k.
   - Create a dictionary with the data to plot the elbow curve.
   - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

2. Answer the following question: What is the best value for k?

### Cluster Cryptocurrencies with K-means Using the Original Scaled Data

1. Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

   - Initialize the K-means model with the best value for k.
   - Fit the K-means model using the original scaled DataFrame.
   - Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
   - Create a copy of the original data and add a new column with the predicted clusters.
   - Create a scatter plot using hvPlot as follows:
     - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
     - Color the graph points with the labels found using K-means.
     - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### Optimize Clusters with Principal Component Analysis

1. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

2. Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

   - What is the total explained variance of the three principal components?

3. Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

4. The first five rows of the PCA DataFrame should appear as follows:

   ![PCA DataFrame](https://github.com/Weekes-Rod/CryptoClustering/blob/main/PCA_DataFrame.png?raw=true)

### Find the Best Value for k Using the PCA Data

1. Use the elbow method on the PCA data to find the best value for k using the following steps:

   - Create a list with the number of k-values from 1 to 11.
   - Create an empty list to store the inertia values.
   - Create a for loop to compute the inertia with each possible value of k.
   - Create a dictionary with the data to plot the Elbow curve.
   - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

### Cluster Cryptocurrencies with K-means Using the PCA Data

1. Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

   - Initialize the K-means model with the best value for k.
   - Fit the K-means model using the PCA data.
   - Predict the clusters to group the cryptocurrencies using the PCA data.
   - Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
   - Create a scatter plot using hvPlot as follows:
     - Set the x-axis as "PC1" and the y-axis as "PC2".
     - Color the graph points with the labels found using K-means.
     - Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

### REFERENCE
 You can also check [Composing Plots](link_to_composing_plots) in the hvPlot documentation.

### Requirements

#### Find the Best Value for k by Using the Original Data

- Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.
- Answer the following question: What’s the best value for k?

#### Cluster the Cryptocurrencies with K-Means by Using the Original Data

- Initialize the K-means model with four clusters by using the best value for k.
- Fit the K-means model by using the original data.
- Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values.
- Create a copy of the original data, and then add a new column of the predicted clusters.
- Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.

#### Optimize the Clusters with Principal Component Analysis

- Create a PCA model instance, and set n_components=3.
- Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.
- Get the explained variance to determine how much information can be attributed to each principal component.
- Answer the following question: What’s the total explained variance of the three principal components?
- Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

#### Find the Best Value for k by Using the PCA Data

- Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11.
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.
- Answer the following questions: What is the best value for k when using the PCA data? Does it differ from the best value for k that you found by using the original data?

#### Cluster Cryptocurrencies with K-means by Using the PCA Data

- Initialize the K-means model with four clusters by using the best value for k. 
- Fit the K-means model by using the original data. 
- Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values. 
- Create a copy of the original data, and then add a new column of the predicted clusters. 
- Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Color the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents. 

#### Optimize the Clusters with Principal Component Analysis 

- Create a PCA model instance, and set n_components=3. 
- Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.
- Get the explained variance to determine how much information can be attributed to each principal component. 
- Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame. 

#### Find the Best Value for k by Using the PCA Data 

- Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11. 
- To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k. 
  
