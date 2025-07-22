## 📊 **Customer Segmentation Project: Detailed Analysis**

**Overview**:

This project applies data science and machine learning techniques to segment customers based on their demographics and purchasing behavior. The overall goal is to identify distinct customer groups so that businesses can tailor marketing strategies, improve targeting, and increase customer satisfaction and revenue.

## 🗂️ **Data Overview**

The original dataset includes a broad set of features, such as:

### 🧑‍🤝‍🧑 **Demographics**
- **Age**, **Year of Birth**, **Education**, **Marital Status**, **Income**, **Number of Children/Teens at home**

### 🧠 **Behavioral**
- **Recency** (days since last purchase)  
- **Spending amounts** on different product categories: **wines**, **fruits**, **meats**, **fish**, **sweets**, **gold**  
- **Number of purchases** via different channels: **web**, **store**, **catalog**  
- **Number of visits**, and **responses** to various marketing campaigns

### 🧮 **Derived Variables**
- Calculated fields such as **Total Spending** and **Age** (from `Year_Birth`)

## 🧩 **Example Features Used for Segmentation**

- **Age**
- **Income**
- **Total_Spending**
- **NumWebPurchases**
- **NumStorePurchases**
- **NumWebVisitsMonth**
- **Recency**

## 🛠️ **Techniques and Workflow**

### 1️⃣ **Data Preparation**

- **Loading and cleaning**: The dataset was imported using `pandas`. Null values and data types were handled accordingly.
- **Feature engineering**: New features like `Total_Spending` (sum of various product category spendings) and `Age` (calculated from `Year_Birth`) were computed to better capture customer profiles.
- **Selection of relevant features**: For clustering, only key behavioral and demographic variables were used.
- **Scaling**: Features were scaled (using scalers like `StandardScaler` or `MinMaxScaler`) to ensure fair contribution to distance calculations during clustering.

---

### 2️⃣ **Exploratory Data Analysis (EDA)**

- **Statistical Summary**: The dataset was examined to understand distributions, mean, median, min, and max values of the features.
- **Correlation and distribution analysis**: Visualizations (histograms, boxplots, scatterplots) were used to detect trends, outliers, and relationships between variables.

---

### 3️⃣ **Clustering for Customer Segmentation**

- **KMeans Clustering**: The primary unsupervised algorithm applied was `KMeans`, a widely adopted method for grouping similar customers.
- **Customer Grouping**: Customers were grouped by similarities in selected features.
- **Cluster Optimization**: The **Elbow Method** or similar approaches were used to determine the optimal number of clusters.
- **Model Training**: The model was trained on the preprocessed and scaled dataset.
- **Cluster Assignment**: Each customer was labeled with the predicted segment.

---

### 4️⃣ **Interpretation of Segments**

- **Profile Analysis**: Post-clustering, the means of each feature within each cluster were calculated to identify unique characteristics.
- **Summary Table**: Averages of key features such as `Age`, `Income`, `Total_Spending`, `NumWebPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`, and `Recency` were tabulated for each cluster.

---

## 📊 **Results**

### 🔍 **Main Clusters and Their Profiles**

The clustering produced six primary customer segments with the following averaged characteristics:

| Cluster | Age   | Income  | Total_Spending | NumWebPurchases | NumStorePurchases | NumWebVisitsMonth | Recency |
|--------:|:-----:|:-------:|:--------------:|:----------------:|:------------------:|:------------------:|:-------:|
|   0     | 52.14 | 35,701  | 130            | 2.30             | 3.43               | 6.42               | 20.28   |
|   1     | 59.66 | 59,903  | 895            | 7.88             | 7.96               | 6.38               | 47.20   |
|   2     | 67.86 | 42,605  | 182            | 2.63             | 4.07               | 5.45               | 66.88   |
|   3     | 46.07 | 75,178  | 1,312          | 4.74             | 8.84               | 2.78               | 50.34   |
|   4     | 68.83 | 77,555  | 1,199          | 4.52             | 8.12               | 2.48               | 48.46   |
|   5     | 47.47 | 31,319  | 105            | 2.26             | 3.14               | 7.14               |         |

---
## 🧠 **Interpreting the Clusters**

- 🔵 **Clusters 3 and 4**: High-income, high-spending, and frequent purchasers with strong engagement across both web and store channels. These are the **most valuable customers**.
- 🟠 **Cluster 1**: Also shows high total spending and purchase activity, but typically includes **older clients**.
- 🟢 **Clusters 0, 2, and 5**: Represent **lower spenders** and/or **lower-income groups**. Some show **higher recency**, indicating less recent engagement with the business.

---

## 💡 **Business Insights**

- 🎯 **Targeted Marketing**: Segments with **high recency** and **low spending** can be targeted with special offers or win-back campaigns.
- 👑 **High-Value Customers**: Clusters **3 and 4** should be prioritized for **loyalty programs** or **VIP customer treatment**.
- ✉️ **Personalized Engagement**: Behavioral and demographic segmentation enables **highly tailored communications** to suit each group’s needs and preferences.

---

## 🧪 **Techniques Used**

- 🧹 **Data Cleaning and Feature Engineering**
- 📏 **Feature Scaling**
- 🤖 **Unsupervised Machine Learning** using **KMeans Clustering**
- 📊 **Statistical Profiling and Visualization**
- 🔍 **Cluster Analysis and Interpretation**

---

## ✅ **Conclusion**

This project demonstrates a complete pipeline for customer segmentation — from raw data preprocessing to advanced unsupervised learning and insightful result interpretation.

By identifying distinct customer types, businesses can adopt more **personalized, strategic, and data-driven approaches**.  
Such segmentation enhances:

- 📈 **Customer lifetime value**
- 📬 **Marketing campaign effectiveness**
- 🚀 **Sustainable business growth**

---

