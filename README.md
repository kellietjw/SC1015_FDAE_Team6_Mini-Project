FDAE Team 6 Mini-Project: Popular Spotify Songs

We started off by importing the essential libraries: numpy, pandas, seaborn, etc.


1: Import Data
Imported using pd.read_csv()


2: Data Cleaning
1. Removed non-numeric 'streams' values
2. Removed duplicates and sorted data in ascending order of 'streams'
3. Removed irrelevant columns
4. Check for null values and delete if necessary
   (not necessary in this case)
5. Listed out the description of relevant features


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
