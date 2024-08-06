# CryptoClustering



Used knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Prepared Data 
* Loaded the crypto_market_data.csv
* Obtained Summary Statistics

![bokeh_plot](https://github.com/svafaeva93/CryptoClustering/assets/124627601/cf7e97a2-c570-4993-ab13-92f88d87437c)

* Used the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
* Created a DataFrame with the scaled data and set the 'coin_id' index from the original DataFrame as the index for the new DataFrame.

<img width="1096" alt="Screenshot 2023-07-06 at 1 37 24 PM" src="https://github.com/svafaeva93/CryptoClustering/assets/124627601/9f43c9b0-d858-4db2-8371-b85b4db88da0">

## Best Value for k Using the Original Scaled DataFrame
* Used elbow method to find the best value for k
  
![elbow_plot_1](https://github.com/svafaeva93/CryptoClustering/assets/124627601/d90399fd-c02d-4056-a896-34a378252ab1)

**Question:** What is the best value for `k`?

**Answer:** The best value for 'k' is 4 based on the Elbow Curve, as there is a strong inflection point. 

## Clustered Cryptocurrencies with K-means Using the Original Scaled Data

![scatter_plot_1](https://github.com/svafaeva93/CryptoClustering/assets/124627601/bc2129ed-b12b-4ae0-a7bf-1b95eaf8b647)

## Optimize Clusters with Principal Component Analysis

<img width="349" alt="Screenshot 2023-07-06 at 1 43 26 PM" src="https://github.com/svafaeva93/CryptoClustering/assets/124627601/05de48a2-5e20-4797-8e53-196964091d3b">

## The Best Value for k Using the PCA Data

![elbow_plot_2](https://github.com/svafaeva93/CryptoClustering/assets/124627601/a823266d-f244-42c3-8fda-c8a15354357b)

**Question:** What is the best value for `k` with PCA data?

**Answer:** The best value for 'k' seems to be 4 again. 

## Clustered Cryptocurrencies with K-means Using the PCA Data

![scatter_2](https://github.com/svafaeva93/CryptoClustering/assets/124627601/18e218ef-7ec3-4627-9b4f-5eaa61091956)

## Visualize and Compare the Results

* Composite plot to contrast elbow curves
  
![elbow_plot_1](https://github.com/svafaeva93/CryptoClustering/assets/124627601/45782e17-02ca-439d-8981-b2d6ac89c25f)

![elbow_plot_2](https://github.com/svafaeva93/CryptoClustering/assets/124627601/f62a736a-343a-4e83-80db-bbc64a485fc6)

* Composite plot to contrast scatter plots


![scatter_plot_1](https://github.com/svafaeva93/CryptoClustering/assets/124627601/b1b3fa61-61b6-49c1-9c56-478b99c75d38)

![scatter_2](https://github.com/svafaeva93/CryptoClustering/assets/124627601/4d798dc9-f677-439c-9d7c-029d2f54ea81)

  * **Question:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

  * **Answer:** Based on the elbow curves, using less features yielded similar results as the original model, the best k-value for both was 4. The scatter plot data using PCA differed from the original plot. Although having many feautures presented may sound optimal, sometimes there is a tendency to overfit the data. Using fewer features in the plot on the right seems to be a better way of presenting the clusters in a more distiguished manner. For example, cluster 0 and 1 seen in the original plot can barely be distiguished as different clusters as they are located in similar coordinates. However, in the second plot on the right using PCA spread those two clusters apart.  Similarly, cluster 1 and 2 are well distinguished in the plot on the right side. 












 
