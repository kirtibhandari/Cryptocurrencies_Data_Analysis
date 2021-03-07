# **Cryptocurrencies Analysis**

## **Overview**
This project is built to help clients to recommend Cryptocurrencies which could prove profitable to the client.
Because of the popularity of Cryptocurrencies, it has become costlier  for the new investors. Bu the market is full of many companies which offer different crypto currencies at affordable price. 

We have a dataset of cryptocurrencies which we can analyze in any way we want. By using this dataset, we want to discover trends to convince the client to invest in the recommended new currencies.

In this analysis, because we only have input data and no target results. this implies we do not know what results we are expecting. hat is why, here we have used **Unsupervised Machine Learning**. This helps to discover patters or groups in data. To accomplish this, we use available dataset as input data only, process data for an unsupervised model, use clustering and most popular unsupervised **K-means algorithm**. The model is then refined using **Principal Component Analysis** (PCA), to limit the features used for analysis and speed up the model.

In order to do the analysis, there are four important stages which were performed:

1. Preprocessing the Data for PCA (Principal Component Analysis)
2. Reducing Data Dimensions using PCA
3. Clustering Cryptocurrencies using K-means algorithm
4. Visualizing Cryptocurrencies Results
## **Results**

- ### **Data Preprocessing**

    **Initial dataset**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/initial_dataset.png)

    **Dataset after preprocessing**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/preprocessed_dataset.png)

    **Data from scaled columns**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/data_standardization.png)


     Available data was preprocessed to make it usable for the PCA. By usability of data, it is meant that the data is free of columns which do not play an important role to find out an answer to our question of grouping useful Cryptocurrencies. 

    To complete this preprocessing, Cryptocurrencies rows which had at least 1 null value, which were not currently trading, which did not have a working algorithm and which did not have any mined coins were removed. Also, removal of one column, which was not required to create those groups or clusters as it did not provide any important information at this point, was done. This column was stored in a separate DataFrame as its the name of coins being traded, which will be useful at later stage after obtaining the results. 

    Also, there were two columns who were important but in text format and make them usable, they were converted to numeric values so that they can be used for PCA.Also, we had to scale these converted numeric columns.

 - ### **Dimension reduction using PCA**

    Three principal components were created to reduce the dimensions using PCA that works on the preprocessed data obtained in stage 1.

    **Dataframe with 3 principal components**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/pca_components.png)

- ### **Clustering Cryptocurrencies using K-means algorithm**

    An elbow curve was created to find out an appropriate value which is to be provided as the number of clusters that needs to be created to appropriately make predictions for clusters from the data.

    **Elbow Curve**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/elbow_curve.png)

    Then we combine the relevant columns from predicted clusters and features from our available dataset.

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/predicted_clusters.png)


- ### **Visualizing CryptoCurrencies**

    **3D- Scatter with PCA data and the clusters**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/3_D_Scatter_plot.png)

    **Table Tradable Cryptocurrencies**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/tradable_currencies.png)

    **Scatter plot Coins Supply Vs Coins mined - tradable Cryptocurrencies**

    ![](https://github.com/kirtibhandari/Cryptocurrencies/blob/main/Resources/final_plot.png)


## **Summary**
From the above scatter plot, we can clearly depict that there are Clusters of coins,, which are divided in 4 different classes to choose from, for Total coins Supplied and Total Coins mined. 

We are able to find which coins performed better than others and we have cluster of various currencies which can be recommended to the client to convince them to invest into these recommended ones to stand at a profitable position than some of the expensive ones in the market.
