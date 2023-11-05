# Clusting_customers
  apply customer segmentation on this historical data. utilizing unsupervised Learning
if you need to apply customer segmentation on this historical data. Customer segmentation is the practice of partitioning a customer base into groups of individuals that have similar characteristics. It is a significant strategy as a business can target these specific groups of customers and effectively allocate marketing resources. For example, one group might contain customers who are high-profit and low-risk, that is, more likely to purchase products, or subscribe for a service. A business task is to retain those customers. Another group might include customers from non-profit organizations and so on.
download the dataset from IBM Object Storage.  IBM is offering a unique opportunity for businesses, with 10 Tb of IBM Cloud Object Storage
path of dataset='https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%204/data/Cust_Segmentation.csv

# Import necessary libraries
from sklearn.cluster import KMeans
from sklearn.cluster import AgglomerativeClustering
from sklearn.cluster import DBSCAN

# Load your data into the variable 'X'

# 1. K-Means Clustering
# Explanation:
# K-Means is a partitional clustering method that divides data into non-overlapping clusters.
# It requires specifying the number of clusters (k) in advance.
# K-Means works well for large datasets but can be sensitive to the initial placement of centroids.

# Create a K-Means model with the desired number of clusters (k)
kmeans = KMeans(n_clusters=k)

# Fit the K-Means model to your data (X)
kmeans.fit(X)

# Get cluster labels for each data point
labels_kmeans = kmeans.labels_

# 2. Hierarchical Clustering (Agglomerative)
# Explanation:
# Hierarchical clustering creates a hierarchy of clusters by iteratively merging clusters based on proximity.
# It doesn't require specifying the number of clusters in advance.
# Hierarchical clustering can handle clusters of various shapes and sizes.

# Create an instance of Agglomerative Clustering with the desired number of clusters
hierarchical = AgglomerativeClustering(n_clusters=k)

# Fit the hierarchical clustering model to your data (X)
hierarchical.fit(X)

# Get cluster labels for each data point
labels_hierarchical = hierarchical.labels_

# 3. DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
# Explanation:
# DBSCAN identifies clusters as dense regions separated by sparser areas.
# It does not require specifying the number of clusters in advance.
# DBSCAN can find clusters of arbitrary shape and is robust against outliers.

# Create a DBSCAN model with desired parameters (eps and min_samples)
dbscan = DBSCAN(eps=eps, min_samples=min_samples)

# Fit the DBSCAN model to your data (X)
dbscan.fit(X)

# Get cluster labels for each data point (including noise points)
labels_dbscan = dbscan.labels_

