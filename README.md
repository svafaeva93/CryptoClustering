# CryptoClustering
[
](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.arabnews.com%2Fnode%2F2074441%2Fbusiness-economy&psig=AOvVaw0bv4QwmCclxqZHwds1n8So&ust=1723001886412000&source=images&cd=vfe&opi=89978449&ved=0CA8QjRxqFwoTCNCurra434cDFQAAAAAdAAAAABAE)![image](https://github.com/user-attachments/assets/7d04bfd8-ba38-4a1b-8bc4-6933c8eaafec)

This project involved creating a machine learning model that grouped cryptocurrencies to assemble investment portfolios that are based on the profitability of the cryptocurrencies. 

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

## Conclusion 

- Market Structure Insight: The presence of four distinct clusters suggests that the 41 cryptocurrencies can be grouped into four different segments based on their similar characteristics. Each cluster represents a group of cryptocurrencies that behave similarly or share common features.

- Diverse Investment Opportunities: By identifying four clusters, you highlight that the cryptocurrency market is not homogenous. Different clusters may represent different levels of risk, growth potential, market behavior, or utility (e.g., stablecoins, altcoins, high-volatility assets).

- Strategy Development: The four clusters can be used to develop different investment strategies. For instance, a conservative investor might focus on cryptocurrencies in a cluster characterized by lower volatility, while a risk-tolerant investor might prefer those in a high-volatility cluster.

- Risk Management: Understanding the characteristics of each cluster allows for better risk management. For instance, if one cluster is highly sensitive to market conditions, a portfolio manager might choose to hedge against potential losses by balancing the portfolio with assets from more stable clusters.

- Market Prediction: If historical data is used for clustering, the identified clusters might help in predicting future trends or behaviors of the cryptocurrencies within each cluster.

In summary, segmenting the 41 cryptocurrencies into 4 clusters using K-means and visualizing them in a scatter plot provided a structured way to understand the diversity within the cryptocurrency market. This finding is significant as it aids in portfolio diversification, risk management, strategy formulation, and market analysis, ultimately leading to more informed investment decisions.












 
