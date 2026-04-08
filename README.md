# 📊 Retail Customer Segmentation with Machine Learning (RFM & K-Means)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-F7931E.svg)
![Seaborn](https://img.shields.io/badge/Seaborn-Data_Visualization-44B78B.svg)

## 📝 Project Overview
This project is an *end-to-end* Data Science solution focused on the retail sector. It transforms a raw transactional database into an actionable marketing strategy through automated customer segmentation. 

By utilizing **RFM (Recency, Frequency, and Monetary value)** analysis in combination with the **K-Means** unsupervised learning algorithm, the model identifies hidden patterns in purchasing behavior and clusters customers into strategic business categories (VIP, Loyal, At Risk, Lost).

## 🚀 Key Features (Data Pipeline)

1. **Data Cleaning & Preprocessing:**
   - Handling of missing values (NaNs).
   - Filtering financial anomalies (negative quantities and prices corresponding to returns or system errors).
2. **Feature Engineering:**
   - Construction of the RFM matrix from transactional data.
   - Application of **Logarithmic Transformations (`np.log1p`)** to normalize highly right-skewed distributions (long tails of "whale" customers).
3. **Predictive Modeling (Machine Learning):**
   - Use of the **Elbow Method** to determine the optimal number of mathematical clusters (k).
   - Training the Scikit-Learn **K-Means** algorithm individually for each RFM pillar.
4. **Business Logic & Scoring:**
   - Intelligent cluster sorting to assign coherent ratings (0 = Worst, 3 = Best).
   - Creation of an **Overall RFM Score** (Scale 0 to 9).
   - Assignment of dynamic commercial labels.

## 🎯 Final Customer Segmentation
The model automatically classifies the entire database into 4 segments ready for targeted marketing campaigns:
* 🏆 **VIP / Champions (Score 7-9):** Buy with high frequency, spend large amounts, and visited us recently. *(Action: Rewards and preferential treatment)*.
* 🤝 **Loyal Customers (Score 5-6):** Customers with good historical purchasing behavior. *(Action: Cross-selling and up-selling)*.
* ⚠️ **At Risk / Average (Score 3-4):** Customers who are starting to cool off or buy very sporadically. *(Action: Aggressive reactivation coupons)*.
* 💔 **Lost Customers (Score 0-2):** Inactive customers of very low value. *(Action: Avoid advertising spend)*.

## 🛠️ Installation Requirements
To run this project in your local environment, clone this repository and install the necessary dependencies:

```bash
# Clone the repository
git clone [https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git)

# Install required libraries
pip install pandas numpy scikit-learn matplotlib seaborn
