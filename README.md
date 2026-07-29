# Customer Segmentation using K-Means Clustering and PCA

## Objective
The objective of this project is to divide shopping mall customers into different groups based on their annual income and spending behavior. These customer segments can then be utilized by the mall's management for targeted marketing campaigns.

## Dataset Link
The dataset used for this assignment is the **Mall Customer Segmentation Dataset**. 
Due to redistribution guidelines, the dataset is not hosted in this repository. It can be downloaded directly from Kaggle:
[Kaggle: Customer Segmentation Tutorial in Python](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

## Libraries Used
*   **Pandas**: For data loading, manipulation, and analysis.
*   **Matplotlib / Seaborn**: For generating the Elbow Curve and PCA scatter plot visualizations.
*   **Scikit-Learn**: For data preprocessing (`StandardScaler`, `LabelEncoder`), model building (`KMeans`), and dimensionality reduction (`PCA`).

## Methodology
1.  **Data Understanding & Preprocessing**: Loaded the dataset and inspected it for missing values. Removed unnecessary columns (e.g., `CustomerID`), encoded categorical variables (like Gender), and standardized all numerical features using `StandardScaler`.
2.  **Finding Optimal Clusters**: Utilized the Elbow Method by plotting the Within-Cluster Sum of Squares (WCSS) against a range of K values to determine the optimal number of clusters.
3.  **K-Means Clustering**: Trained a K-Means model using the selected optimal K value and assigned a cluster label to each customer.
4.  **Dimensionality Reduction**: Applied Principal Component Analysis (PCA) to reduce the dataset to 2 principal components, enabling 2D visualization of the high-dimensional data.

## Results
*   **Elbow Curve**: The Elbow curve displayed a gradual decrease in WCSS. Evaluating the rate of variance drop indicated that K=4 or K=5 were reasonable choices for the optimal number of clusters.
*   **Clustering**: The K-Means model successfully separated the customer base into distinct generalized profiles.
*   **PCA Visualization**: Reducing the features to two principal components allowed for a clear 2D scatter plot visualization of the customer segments while retaining maximum variance.

## Conclusion
This analysis segmented mall customers using K-Means clustering across four demographic features. The key findings reveal specific customer profiles, though the elbow method indicated a smooth variance drop, suggesting overlapping traits among the groups. From a business perspective, defining these segments (such as the high-income/high-spending group) allows the mall to launch targeted marketing campaigns, optimizing promotional budgets. A notable limitation of K-Means clustering encountered here is its sensitivity to the number of dimensions and the sometimes subjective requirement to pre-define the number of clusters. To overcome the difficulty of plotting four distinct features, Principal Component Analysis (PCA) was applied. The primary advantage of PCA is dimensionality reduction; it effectively compressed the dataset into two principal components, enabling clear, two-dimensional visualization without losing significant variance.
