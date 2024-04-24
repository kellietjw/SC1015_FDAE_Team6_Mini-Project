FDAE Team 6 Mini-Project: Popular Spotify Songs

We started off by importing the essential libraries: numpy, pandas, seaborn, etc.

-----------------------------------------------------------------------------------------

1: Import Data
Imported using pd.read_csv()

-----------------------------------------------------------------------------------------

2: Data Cleaning
1. Removed non-numeric 'streams' values
2. Removed duplicates and sorted data in ascending order of 'streams'
3. Removed irrelevant columns
4. Check for null values and delete if necessary
   (not necessary in this case, no null values)
5. Listed out the description of relevant features

-----------------------------------------------------------------------------------------

3: EDA

1. Uni-Variate Analysis on Musical Features
   Purpose: To check for relationships between the features and 'streams'
   Box Plots and Histograms for Numerical Features
   Cat Plot for Categorial Features

2. Uni-Variate Analysis on Non-Musical Features
   Purpose: To check for relationships between the features and 'streams'
   Box Plots and Histograms for Numerical Features (All numerical)

3. Correlation Matrix / Heat Map
   Purpose: To check for relationships between the features and 'streams', and ALSO among the features

4. Top 20s

-----------------------------------------------------------------------------------------

4: ML: K-Means Clustering

New imports used:  
from sklearn.cluster import KMeans
from sklearn.metrics import silhouette_score
from sklearn.decomposition import PCA

1. Select all numeric data
2. Fit KMeans model to data, store in array sse[] that contains sum of squared distances
3. Elbow Method, plot sum of squared distance from array sse[]
   Optimal number of clusters is the point in the plot where the rate of decrease in sse slows down abruptly
4. Fit the model to the data using fit() from KMeans
5. Generate cluster assignments using predict() from KMeans
6. Calculate silhouette_score to check for quality of clusters, whether they are well matched.
   A higher silhouette score indicates a good clustering configuration,
   a lower silhouette score indicates a poor clustering configuration.
7. Reduce the data to 2 dimensions using PCA, then plot the points on a scatter plot
   Includes other forms of visualisation to display the data cluster by cluster
   (scatter plot with specific cluster highlighted, bar plot)