# Kickstarter Project Analysis: Predicting Success and Identifying Clusters

**Category**: Classification, Clustering, Business Insights  
**Tools Used**: Python, Random Forest, Logistic Regression, K-Prototypes  

## Overview
This project focuses on analyzing Kickstarter projects to predict their success and identify meaningful clusters. By leveraging advanced machine learning models and exploratory analysis, the goal is to provide actionable insights for creators to maximize their chances of success and help platforms like Kickstarter enhance user experiences.

## Objectives
1. **Classification Model**:
   - Predict whether a Kickstarter project will be "successful" or "failed."
   - Provide insights into features influencing project outcomes.
2. **Clustering Model**:
   - Group projects based on shared characteristics for tailored recommendations.
   - Identify distinct creator needs to enhance Kickstarter’s platform strategy.

---

## Task 1: Classification Model
### **Data Preprocessing**
- **Target Variable**: Focused only on 'successful' and 'failed' states; other states were dropped.
- **Missing Data**:
  - Replaced missing values in `main category` based on frequency within categories.
- **Feature Engineering**:
  - Created a new variable, `Continent`, to simplify `country` (115 categories → 6 categories).
  - Selected variables based on exploratory analysis and visual insights.

### **Exploratory Data Analysis (EDA)**
- Numerical variables like `blurb_len` and `deadline_month` showed clear differences between successful and failed projects.
- Categorical variables like `Continent`, `currency`, and `main category` revealed significant trends.
- Selected Variables:
  - **Numerical**: `blurb_len`, `deadline_month`, `deadline_yr`, etc.
  - **Categorical**: `Continent`, `main_category`, `currency`, `show_feature_image`.

### **Modeling**
- **Models Compared**: Random Forest vs. Logistic Regression.
- **Best Model**: Logistic Regression with 75% accuracy, 80% precision, and 75% recall.
- **Key Insights**:
  - Projects with feature images and videos have higher success rates.
  - Categories like Children's Books and Comics are positively associated with success, while Food and Technology face challenges.

### **Business Implications**
- Visual appeal (e.g., feature images and videos) significantly increases project success.
- Strategic timing and category selection can improve outcomes for creators.
- Multimedia engagement is a critical factor for backers.

---

## Task 2: Clustering Model
### **Cluster Modeling**
- Excluded the `state` variable to avoid bias toward success or failure.
- Implemented **K-Prototype Clustering** to handle mixed categorical and numerical data.

### **Model Specifications**
- Used the **Elbow Method** and **Silhouette Score** to identify 3 optimal clusters.
- Initialization with `Huang` ensures effective handling of mixed data types.

### **Cluster Insights**
1. **Cluster 0**: 
   - Moderately descriptive Film & Video projects (launched in 2019).
   - Well-planned with consistent deadlines and significant use of promotional materials.
   - Primarily targeted at North American audiences.
2. **Cluster 1**: 
   - Recent Art projects focused on Accessories (launched in 2020).
   - Standard patterns but with less emphasis on multimedia content.
3. **Cluster 2**: 
   - Niche projects with shorter deadlines and targeted audiences.
   - Minimal reliance on promotional tools like videos.

### **Business Usefulness**
- **Cluster 0**: Provide premium tools for professional creators.
- **Cluster 1**: Offer simplified resources for smaller creators.
- **Cluster 2**: Focus on targeted support for niche projects.

---

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/kickstarter-analysis.git
