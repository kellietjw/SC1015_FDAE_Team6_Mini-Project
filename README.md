FDAE Team 6 Mini-Project: Popular Spotify Songs

Started off by importing the essential libraries: numpy, pandas, seaborn, etc.


-----------------------------------------------------------------------------------------------------------

1: Import Data
Imported using pd.read_csv()

-----------------------------------------------------------------------------------------------------------

2: Data Cleaning
1. Removed non-numeric 'streams' values
2. Removed duplicates and sorted data in ascending order of 'streams'
3. Removed irrelevant columns
4. Check for null values and delete if necessary
   (not necessary in this case, no null values)
5. Listed out the description of relevant features

-----------------------------------------------------------------------------------------------------------

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

4. Top 20s (Reflects the preferences and tastes of Spotify users)  
   Purpose: This selection ensures that the analysis focuses on the most impactful and relevant observations.  
   Allows for a more targeted examination of key features that contribute to the success of these top-performing entries.  

-----------------------------------------------------------------------------------------------------------

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

-----------------------------------------------------------------------------------------------------------

Individual Contributions:  
@sabareeshkannan - EDA, K-Means Clustering  
@shaniaooi - Data Extraction, Data Clean-Up, EDA  
@kellietjw - EDA, K-Means Clustering  

References:  
1. https://developer.spotify.com/documentation/web-api/reference/get-audio-features  
2. https://www.digitalocean.com/community/tutorials/exploratory-data-analysis-python  
3. https://www.datacamp.com/tutorial/k-means-clustering-python  
4. https://drlee.io/the-ultimate-step-by-step-guide-to-data-mining-with-pca-and-kmeans-83a2bcfdba7d  
5. https://towardsdatascience.com/k-means-clustering-and-principal-component-analysis-in-10-minutes-2c5b69c36b6b  
6. https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a
7. SC1015 Course Content  

