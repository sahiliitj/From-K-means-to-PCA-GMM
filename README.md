# 📊 MNIST Clustering from Scratch – K-Means, PCA & GMM

> Machine Learning Assignment – CSL7620  
> **Author:** Sahil Sharma  
> **Roll No.:** M21MA210  
> **Program:** M.Sc - M.Tech (Data and Computational Sciences)  
> **Institute:** Indian Institute of Technology, Jodhpur  
> **Submission Date:** October 14, 2023  

---

## 📝 Project Overview

This project explores unsupervised learning techniques using the MNIST dataset. Two main approaches are implemented:

- **K-Means Clustering** from scratch using cosine similarity
- **PCA (Principal Component Analysis)** from scratch followed by **GMM (Gaussian Mixture Model)** clustering

---

## 📁 Dataset Description

- **Dataset:** [MNIST](http://yann.lecun.com/exdb/mnist/)
- **Images:** 70,000 grayscale images of handwritten digits (0–9)
- **Image Size:** 28x28 pixels
- **Train Set:** 60,000 images
- **Test Set:** 10,000 images

---

## 🔍 Task 1: K-Means Clustering from Scratch

### ✅ Subtasks

1. **Exploratory Data Analysis**
    - Visualized sample images
    - Analyzed digit distribution
    - Observed pixel intensity histogram
    - Correlation heatmap for image features

2. **K-Means Implementation**
    - Implemented from scratch using **cosine similarity**:
      \[
      \text{sim}(\theta) = \frac{v_1 \cdot v_2}{\|v_1\| \|v_2\|}
      \]

3. **Clustering Visualizations**
    - Visual results shown for:
      - `K = 4`
      - `K = 7`
      - `K = 10`

4. **Cluster Characteristics**
    - Hard assignment
    - Sensitivity to initialization and outliers
    - Similar digits grouped together (e.g., 3 & 5)
    - Best results observed at `K = 10`

5. **Finding Optimal `K`**
    - Elbow Method used  
    - Elbow point at `K = 10`

📎 **Notebook:** [Google Colab – K-Means](https://colab.research.google.com/drive/1u0dqXh735Gu5G9CIX-_0zknUG-mP7mMn?usp=sharing)

---

## 📈 Task 2: PCA from Scratch + GMM Clustering

### ✅ Subtasks

1. **PCA Implementation**
    - Implemented PCA from scratch
    - Used `numpy.linalg.svd` for decomposition
    - Tested with:
        - 32 components
        - 64 components
        - 128 components

2. **GMM Clustering**
    - Applied Gaussian Mixture Model using `sklearn.mixture.GaussianMixture`
    - Clustering for:
        - 4 clusters
        - 7 clusters
        - 10 clusters

3. **Cluster Visualizations**
    - Plotted results for each combination of components × clusters

4. **Comparison with K-Means**
    - GMM provides soft assignment (probabilistic)
    - Handles noise & overlapping better than K-Means
    - Non-spherical clusters possible
    - More robust to outliers and complex patterns

5. **Optimal PCA Components**
    - Best quality with **128 components**
    - Clear image recognition and cluster separation

6. **When PCA May Fail (BONUS)**
    - Data with **non-linear relationships**
    - Data not **standardized**
    - **Information loss** in low-variance components
    - **Computationally expensive** for large datasets
    - Sensitive to **outliers**
    - May not be ideal for classification → Consider LDA (Fisher’s)

📎 **Notebook:** [Google Colab – PCA + GMM](https://colab.research.google.com/drive/18XgKzS8CLidb-4eHtrv7lueAZH51mbmb?usp=sharing)

---

## 🧠 Key Insights

- Cosine similarity effectively replaces Euclidean in K-Means
- PCA simplifies high-dimensional data and enhances GMM results
- GMM outperforms K-Means in separating complex clusters
- Visualizations are essential for qualitative evaluation

---

## 🔗 References

- [K-Means Clustering – Wikipedia](https://en.wikipedia.org/wiki/K-means_clustering)  
- [Gaussian Mixture Model – GeeksforGeeks](https://www.geeksforgeeks.org/gaussian-mixture-model/)  
- [Mixture Models – Wikipedia](https://en.wikipedia.org/wiki/Mixture_model)  
- [SVD – NumPy Documentation](https://numpy.org/doc/stable/reference/generated/numpy.linalg.svd.html)  
- [Digital Image Processing Basics](https://www.geeksforgeeks.org/digital-image-processing-basics/)

---

## 🙋‍♂️ Author Info

```text
Name       : Sahil Sharma
Roll No.   : M21MA210
Program    : M.Sc - M.Tech (Data and Computational Sciences)
Institute  : Indian Institute of Technology, Jodhpur
Course     : CSL7620 - Machine Learning
