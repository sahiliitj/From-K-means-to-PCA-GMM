📊 MNIST Clustering from Scratch – K-Means, PCA & GMM
📁 Project Overview
This project, developed as part of an assignment for the CSL7620 Machine Learning course at IIT Jodhpur, demonstrates unsupervised learning techniques applied to the MNIST dataset. The objective is to explore data clustering using two major workflows:

K-Means Clustering implemented from scratch using cosine similarity

Principal Component Analysis (PCA) from scratch followed by Gaussian Mixture Model (GMM) clustering

The MNIST dataset of handwritten digits is used throughout the project to evaluate clustering quality and analyze the efficacy of different approaches.

📚 Dataset
MNIST Dataset

Contains 70,000 grayscale images of handwritten digits (0–9)

Image dimensions: 28x28 pixels

Training set: 60,000 images

Test set: 10,000 images

🔍 Task 1: K-Means Clustering from Scratch
📌 Subtasks
Exploratory Data Analysis (EDA)

Visualized sample images

Analyzed label distributions

Examined pixel intensity distribution and correlation heatmap

K-Means Implementation

Implemented from scratch using cosine similarity instead of traditional Euclidean distance

Cosine similarity formula used:

sim
(
𝜃
)
=
𝑣
1
⋅
𝑣
2
∥
𝑣
1
∥
∥
𝑣
2
∥
sim(θ)= 
∥v 
1
​
 ∥∥v 
2
​
 ∥
v 
1
​
 ⋅v 
2
​
 
​
 
Cluster Visualization

Results shown for k = 4, k = 7, and k = 10 clusters

Images in each cluster visualized and analyzed

Cluster Analysis

Observed that:

Hard assignments can lead to overlapping class clusters

K-Means is sensitive to outliers and initialization

Best clustering observed at k = 10

Optimal Cluster Count

Elbow method used to determine optimal value of k

Found k = 10 to be the most appropriate

📎 K-Means Google Colab Notebook

📈 Task 2: PCA from Scratch + GMM Clustering
📌 Subtasks
PCA Implementation (from scratch)

PCA applied to reduce dimensionality using:

32 components

64 components

128 components

Libraries were used only for SVD (Singular Value Decomposition)

GMM Clustering

Clustering performed using Gaussian Mixture Models

Implemented using sklearn.mixture.GaussianMixture

Cluster Visualization

Analyzed results for combinations of:

Components = 32, 64, 128

Clusters = 4, 7, 10

Cluster Characteristics & Comparison with K-Means

GMM provides soft assignments, leading to:

Better handling of noise/outliers

Better separation of overlapping clusters

Clusters of non-spherical shapes (flexible boundaries)

Observed that GMM significantly outperforms K-Means for this dataset

Optimal Component Count

Found 128 PCA components preserve sufficient information

Bonus discussion on PCA limitations:

Sensitive to scaling and outliers

Ineffective for non-linear patterns

Computationally expensive for large datasets

📎 PCA & GMM Google Colab Notebook

🧠 Key Learnings
Importance of choosing the right similarity metric (cosine similarity worked well)

PCA helps reduce dimensionality before applying complex clustering models

GMM's probabilistic nature handles ambiguity better than hard-clustering methods like K-Means

Visual analysis is critical to evaluate clustering performance effectively

🔗 Resources Used
📖 K-Means Clustering – Wikipedia

📖 Gaussian Mixture Model – GeeksforGeeks

📖 Mixture Models – Wikipedia

📖 SVD in NumPy

👨‍🎓 Author
Name: Sahil Sharma
Roll No: M21MA210
Program: M.Sc - M.Tech (Data and Computational Sciences)
Institution: Indian Institute of Technology, Jodhpur
Course: CSL7620 - Machine Learning
Submission Date: October 14, 2023
