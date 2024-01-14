# Clustering with Basic K-Means Algorithm 

## Goal 

Write functions to implement the basic k-means algorithm and apply those to a test dataset. 

## Dataset 

The data used here is a small, 2D dataset curated for the purpose of testing the functions generated. 

[Dataset](https://gist.githubusercontent.com/TieJean/ff4dbd0022ab5e292db73d8b4910f551/raw/624db21e20faa92b79e5289ce4d9002e863b0d68/data_kmeans.csv)

<img width="206" alt="Screenshot 2024-01-14 at 12 17 44 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/34a2c098-0772-41aa-a9f0-ff9c37738d44">
Figure 1. Sample of original dataset. 

## Function to return k random rows 

This function will accept two parameters: a data frame df_data, and an integer k, and returns the initial centroids for our k-means algorithm. The return values will be the indices of k random points from the dataframe. 

Using random_state = 42

<img width="208" alt="Screenshot 2024-01-14 at 12 18 27 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/9c36d526-8860-4f3c-a99d-c99f00dd114d">
Figure 2. Initial centroids randomly chosen. 

## Function to assign every row of data to a centroid 

This function will accept two parameters: a data frame, df_data, that represents our data to be clustered, and the data frame, df_centroids, which is of length k and contains the current centroids for our clusters.  It returns a series of the same length of df_data that contains the index of the closest centroid in df_centroid. 

Using Euclidean distance as the distance measure. 

<img width="104" alt="Screenshot 2024-01-14 at 12 19 30 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/d0d10a1a-4b87-473a-95ef-e252b2eb4217">
Figure 3. Amount of points initially assigned to each centroid. 

## Function that recomputes centroids 

This function takes two parameters: the data frame, df_data containing the data being clustered, and a series of the same length that contains the label of the assigned centroid for every row in df_data, s_centroid_assignment. It will return a data frame containing the centroids (mean) value for each unique centroid. 

<img width="203" alt="Screenshot 2024-01-14 at 12 20 19 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/2f7667b3-fc90-4fec-93f3-81491f033672">
Figure 4. Recomputed centroids based on initial clustering. 

## Function that compares two centroid dataframes 

The stopping condition for our k-means is when our centroids have not moved since the last iteration. 

This function will take 2 centroid dataframes and return a boolean indicating if the centroids at each unique index are equal. 

## Function that implements k-means via the previously written functions

This function takes a dataframe with values to cluster and the number of clusters to form (k). It returns a series of data of the same length as the original dataset that contains the cluster assignments. 

<img width="72" alt="Screenshot 2024-01-14 at 12 21 31 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/2c72448f-a653-4b81-90da-311927393187">
Figure 5. Final amount of points in each cluster. 

## Final results 

<img width="485" alt="Screenshot 2024-01-14 at 12 22 30 PM" src="https://github.com/catherinealeal/BasicKMeans/assets/100166102/77038e05-0ec0-4320-9309-43c3a7e5bf5a">
Figure 6. The original data points plotted using color to distinguish assigned clusters. 

## View full notebook [here](https://github.com/catherinealeal/BasicKMeans/blob/5c743bf51d9ea5cbdae075bb5d2bbd754d34b549/BasicKMeans.ipynb)
