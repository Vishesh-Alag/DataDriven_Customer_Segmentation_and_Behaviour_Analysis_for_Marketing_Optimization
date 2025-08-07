# 🛍️ Data-Driven Customer Segmentation and Behaviour Analysis for Marketing Optimization

A comprehensive data analysis project to uncover insights about customer purchasing behavior using Descriptive Statistics, Probability Distributions, and Customer Segmentation. This project was implemented in Python using Pandas, Seaborn, Matplotlib, and Scikit-learn, and executed in Google Colab.

---

## 🔍 Problem Statement

The aim of this project is to analyze customer-level marketing data and uncover patterns, trends, and segments that can be leveraged to:
- Increase offer acceptance rates
- Improve campaign targeting
- Enhance customer retention and satisfaction

---

## 🎯 Objectives

- Clean and preprocess raw marketing data.
- Understand demographic and behavioral patterns using descriptive statistics.
- Detect outliers and manage skewed distributions.
- Analyze probability distributions of key purchase behaviors.
- Segment customers using KMeans clustering and derive business strategies.

---

## 📁 Dataset

- **📄 Dataset Name:** `superstoremarketingdata.csv`
- **📎 Download:** [Click here to download](https://drive.google.com/file/d/14H7tRcIIyVDKaWLQyYPf2SZvV3k5xQHM/view?usp=sharing)
- **🧾 Source:** Marketing campaign dataset from a past campaign, containing demographics, transactions, and product category spend.

---

## 🛠️ Project Setup

### ✅ Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- scipy

Install all dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```

### ▶️ To Run

1. Open the Colab notebook or your local IDE.
2. Upload the dataset (`superstoremarketingdata.csv`) to the environment.
3. Run the cells step-by-step to execute analysis and visualizations.

---

## 🧹 Step 1: Data Cleaning & Preprocessing

- Handled missing values using median imputation.
- Converted string dates into datetime objects and parsed invalid entries.
- **Feature Engineering:**
  - Calculated Age, Customer Tenure, Is_Parent (binary), Total_Spent.
- Removed unrealistic age values (e.g., age > 100).

---

## 📊 Step 2: Descriptive Statistics

- Calculated mean, median, variance, skewness, and kurtosis.
- **Visualized key features:**
  - Histograms for Age, Income, Spending
  - Pie charts for Education & Marital Status
  - Box plots for outlier detection
- Applied Winsorization instead of IQR/standard deviation to handle outliers (keeps data intact).

---

## 📈 Step 3: Probability Distributions

- Tested Normality for Income, Age, and Total_Spent using Shapiro-Wilk, skewness, and kurtosis.
- **Used:**
  - Empirical Probability (e.g., % of customers spending less than ₹500)
  - Poisson Distribution for purchase counts (Web, Store, Catalog)
  - Binomial Distribution for binary events (Response, Complain, Is_Parent)
- **Derived probabilities like:**
  - P(X ≥ 5 Web Purchases)
  - P(Income > ₹60,000)
  - P(Response ≥ 20 in 100 trials)

---

## 🧠 Step 4: Customer Insights & Relationships

- **Analyzed key relationships:**
  - Income ↔ Total_Spent (strong positive)
  - Age ↔ Spending (weak)
  - Education, Marital Status, Parenthood ↔ Spending
- Generated scatter plots, boxplots, and heatmaps to visualize relationships.
- Extracted strategic marketing insights for each demographic.

---

## 👥 Step 5: Customer Segmentation (KMeans)

- **Used 3-cluster KMeans based on:**
  - Behavioral + Demographic features (Income, Age, Purchases, Spend, Education, etc.)
- Performed PCA for 2D visualization.
- **Labeled segments dynamically:**
  - 🟢 **Budget** – Low Income & Spend
  - 🔵 **Mid-tier** – Moderate Income & Spend
  - 🟠 **Premium** – High Income & Spend
- Saved output as `clustered_customer_segments.csv`

---

## 📊 Step 6: Final Visualizations

- Segmentation: Income vs Total Spending (Scatter)
- Education vs Spending (Boxplot)
- Parenthood vs Spending (Boxplot)
- Clear visual summaries for stakeholders

---

## 📦 Output Files

- `cleanedssmcsv.csv` – After data cleaning
- `winsorized_cleaned_marketing_data.csv` – After outlier treatment
- `clustered_customer_segments.csv` – Final clustered data

---

## ✅ Key Business Recommendations

- Focus premium offers on high-income, high-spending customers.
- Target mid-tier customers for loyalty upgrades.
- Activate low-engagement users with educational campaigns or better deal visibility.
- Separate campaigns for parents vs non-parents.
- Optimize channels (web vs in-store) based on user behavior patterns.

---

## 📌 Project Highlights

- ✅ End-to-end data project workflow from cleaning to clustering.
- 📈 Applied advanced descriptive + inferential statistics.
- 🧠 Used real-world marketing metrics for actionable insights.
- 💡 Built robust visualizations and segmentation strategy.

