![Project Banner](project-banner.png)
# 🛒 Customer Segmentation with RFM & K-Means Clustering

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-green)

This project is an **Unsupervised Learning** project that aims to segment customers based on their purchasing habits using the **Online Retail II** dataset from a UK-based retail company.

The project combines and compares the rule-based **RFM Analysis** method with machine learning-based **K-Means** and **Hierarchical Clustering** techniques.

## 📋 Table of Contents
- [Business Problem](#-business-problem)
- [Dataset Story](#-dataset-story)
- [Methods and Techniques](#-methods-and-techniques)
- [Project Stages](#-project-stages)
- [Installation and Usage](#-installation-and-usage)
- [Results](#-results)

---

## 🎯 Business Problem
The company wants to divide its customers into groups (segments) based on their characteristics to develop specific marketing strategies for each group. For example, different campaigns will be designed for high-revenue customers versus those who haven't shopped in a long time.

## 📊 Dataset Story
The dataset includes online sales transactions between **01/12/2009 - 09/12/2011**.

* **InvoiceNo:** Invoice number (starts with 'C' if cancelled).
* **StockCode:** Product code.
* **Description:** Product name.
* **Quantity:** Product quantity.
* **InvoiceDate:** Invoice date.
* **UnitPrice:** Unit price (Sterling).
* **CustomerID:** Unique customer number.
* **Country:** Country name.

---

## 🛠 Methods and Techniques

The following Data Analytics and Machine Learning techniques were applied in this project:

1.  **Data Preprocessing:** Cleaning missing data and removing cancelled transactions (returns).
2.  **Outlier Detection:** Suppressing outliers using statistical threshold values (IQR method).
3.  **RFM Analysis:**
    * **Recency:** How recently the customer made a purchase.
    * **Frequency:** How often the customer makes a purchase.
    * **Monetary:** How much money the customer spends.
4.  **Feature Scaling:** Applying **Log Transformation** and **StandardScaler** to make the data suitable for the K-Means algorithm.
5.  **K-Means Clustering:** Determining the optimal number of clusters using the **Elbow Method** and building the model.
6.  **Hierarchical Clustering:** Visualizing clusters with a Dendrogram.

---

## 🚀 Project Stages

When the code is executed, the following steps occur sequentially:

1.  **Data Loading:** Reading data from the Excel file.
2.  **Cleaning:** Applying `Quantity > 0` and `Price > 0` filters. Removing invalid StockCodes.
3.  **RFM Scoring:** Calculating Recency, Frequency, and Monetary values for each customer.
4.  **Visualization:** Plotting distribution graphs (Histograms).
5.  **ML Preparation:**
    * Applying `Log Transformation` to fix skewness.
    * Applying `StandardScaler` for distance-based algorithms.
6.  **Modeling:**
    * Plotting the Elbow graph using the `Yellowbrick` library to find the optimal `k` (cluster count).
    * Assigning customers to segments.
7.  **Reporting:** Printing average spending and frequency values of segments to the console.

---

## 💻 Installation and Usage

To run this project on your local machine:

1.  Clone this repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/PROJECT_NAME.git](https://github.com/YOUR_USERNAME/PROJECT_NAME.git)
    ```

2.  Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scipy yellowbrick openpyxl
    ```

3.  Add the `online_retail_II.xlsx` file to the project directory and run the script:
    ```bash
    python Customer_segmentation_with_k_means.py
    ```

---

## 📈 Results

As a result of the analysis, customers were grouped based on the optimal cluster number determined by the **Elbow Method**.

Example Output Analysis:
* **Segment 1:** "Loyal Customers" who shop frequently and spend high amounts.
* **Segment 2:** "At Risk" customers who haven't visited in a long time.
* **Segment 3:** New customers with high potential.

*(Note: The exact number of segments is automatically determined by the Elbow analysis during runtime.)*

---

## 📧 Contact

**Developer: [Büşra Telli]

