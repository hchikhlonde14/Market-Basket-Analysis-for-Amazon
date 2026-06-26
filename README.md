# Market Basket Analysis with Python - Amazon Customer Behavior

## Overview
This project presents a comprehensive analysis of Amazon customer behavior using a customer survey dataset. The analysis covers data cleaning, exploratory data analysis (EDA), customer segmentation, and behavioral pattern identification to derive actionable business insights for e-commerce optimization and targeted marketing strategies.

## Problem Statement
- **What products or categories are frequently purchased together**, indicating cross-selling opportunities?
- **How do customer purchasing patterns vary across demographics or regions?**
- **Can we segment customers based on buying behavior** to target personalized promotions?
- **Which products drive repeat purchases or high customer loyalty?**
- **What factors contribute to cart abandonment** and how can they be mitigated?

## Dataset
- **Source:** Amazon Customer Behavior Survey
- **Number of Records:** 800 customer transactions
- **Number of Features:** 24 attributes
- **Data Period:** June 2023
- **Key Metrics:** Purchase frequency, product categories, customer satisfaction, review patterns, cart behavior

## Tools & Technologies
- **Language:** Python 3.11.15
- **Data Processing:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn (K-Means Clustering)
- **Statistical Analysis:** SciPy
- **Visualization:** Matplotlib, Seaborn
- **Notebook Environment:** Jupyter Notebook

## Project Workflow

### 1. **Data Collection**
- Sourced Amazon customer survey dataset with 800 records
- 24 features covering demographics, purchasing patterns, review behavior, and satisfaction metrics

### 2. **Data Cleaning & Preparation**
- **Handled Null Values:** 157 missing values in `Product_Search_Method` column
- **Fixed Duplicate Columns:** Renamed duplicate `Personalized_Recommendation_Frequency` columns to `Recommendation_Response` and `Recommendation_Score`
- **Standardized Column Names:** Removed extra spaces and formatted consistently
- **Data Quality:** Achieved 100% non-null data after cleaning (800 complete records)

### 3. **Exploratory Data Analysis (EDA)**
- **Demographic Analysis:** Gender distribution (Male: 209, Female: 197, Others: 202, Prefer not to say: 192)
- **Purchase Frequency Distribution:** Uniform distribution across 5 categories
  - Once a month: 168 customers
  - Once a week: 159 customers
  - Multiple times a week: 159 customers
  - Few times a month: 158 customers
  - Less than once a month: 156 customers
- **Product Category Preferences:**
  - Clothing and Fashion (Most Popular)
  - Home and Kitchen
  - Beauty and Personal Care
  - Groceries and Gourmet Food
- **Cart Abandonment Analysis:** High shipping costs identified as primary factor
- **Review Dependency:** Customers heavily dependent on reviews show lower satisfaction (3.02) vs. moderate users (3.20)

### 4. **Feature Engineering**
- **Age Grouping:** Binned ages into 5 groups (Child, Teen, Young Adult, Adult, Senior)
- **Purchase Frequency Ranking:** Numerical encoding of purchase patterns
- **Customer Behavior Encoding:** Categorical variables transformed for clustering
- **Satisfaction Metrics:** Combined multiple satisfaction indicators

### 5. **Model Building - Customer Segmentation**
- **Algorithm:** K-Means Clustering
- **Number of Clusters:** 3 customer segments identified
- **Segments:**
  - **Occasional Buyers:** 530 customers (Primary segment - 66.25%)
  - **Frequent Buyers:** 135 customers (16.875%)
  - **At-Risk Customers:** 135 customers (16.875%)

### 6. **Evaluation & Insights**

#### Key Findings:
- **Total Customers:** 800
- **Average Satisfaction Score:** 3.01/5
- **Senior Citizens (50+):** Show highest engagement and purchasing activity
- **Working Class (Young Adults & Adults):** Significant contributors to purchases
- **Top Product Category:** Clothing and Fashion dominates across all age groups
- **Cart Abandonment Rate:** Primarily driven by high shipping costs
- **Shopping Frequency:** Low among majority; mostly occasional shoppers
- **Recommendation Effectiveness:** No significant correlation with satisfaction; high review expectations lead to disappointment

## Results & Insights

### Customer Segmentation Results:
| Segment | Count | % of Total | Characteristics |
|---------|-------|-----------|---|
| Occasional Buyers | 530 | 66.25% | Low purchase frequency, price-sensitive, high cart abandonment |
| Frequent Buyers | 135 | 16.875% | Repeat customers, high engagement, brand loyal |
| At-Risk Customers | 135 | 16.875% | Declining engagement, high dissatisfaction, churn risk |

### Business Insights:
1. **Demographic Insights:**
   - Senior citizens (50+) are most engaged with uniform distribution across age groups
   - All age groups contribute equally to overall business

2. **Product Insights:**
   - Clothing & Fashion is the clear market leader
   - Cross-selling opportunities with Beauty/Personal Care and Home/Kitchen

3. **Behavioral Insights:**
   - 66.25% are occasional buyers - high potential for conversion
   - Cart abandonment due to shipping costs (primary factor)
   - Review reliability paradox: Heavy review dependency correlates with lower satisfaction

4. **Satisfaction Insights:**
   - Overall satisfaction is moderate (3.01/5)
   - Customers with low review dependency show higher satisfaction
   - Rating accuracy and shopping satisfaction show moderate positive correlation

## Strategic Recommendations

### 1. **Reduce Cart Abandonment**
- Implement competitive shipping costs or free shipping thresholds
- Offer shipping cost incentives for first-time buyers
- Display shipping costs early in checkout process

### 2. **Focus on Clothing & Fashion**
- Maintain strong inventory in Clothing & Fashion category
- Create targeted campaigns for seniors and working-class demographics
- Bundle Clothing with complementary categories (Beauty, Home)

### 3. **Convert Occasional Buyers to Frequent Buyers**
- Implement loyalty programs with purchase frequency rewards
- Personalized discounts for occasional buyers
- Email campaigns highlighting new arrivals in preferred categories

### 4. **Manage Review Expectations**
- Curate reviews to reflect realistic product quality
- Add verified purchase badges
- Include detailed product descriptions to reduce expectation mismatch
- Encourage honest reviews from diverse customer segments

### 5. **Retention for At-Risk Customers**
- Implement win-back campaigns
- Offer personalized promotions
- Improve customer service responsiveness
- Survey to understand churn reasons

## Visualizations Generated

### Dashboard Components:
- **Customer Segment Distribution** (Bar Chart)
- **Most Purchased Product Categories** (Horizontal Bar Chart)
- **Shopping Satisfaction Distribution** (Bar Chart)
- **Age Groups Distribution** (Bar Chart)
- **Recommendation Helpfulness vs. Satisfaction** (Heatmap)
- **Customer Segments Across Age Groups** (Grouped Bar Chart)
- **Correlation Matrix** (Heatmap) - Shows relationships between key metrics
- **Purchase Frequency Analysis** (Bar Chart)

## Project Structure
```
├── .git/                          # Version control
├── .gitignore                     # Git ignore file
├── data/                          # Raw and processed datasets
│   └── Amazon.csv                # Source dataset (800 records, 24 features)
├── notebooks/                     # Jupyter notebooks
│   └── MarketAnalysis.ipynb      # Main analysis notebook
├── .jpynb_checkpoints/           # Notebook checkpoints
├── Report/                        # Generated reports and visualizations
│   └── Visualizations/           # Dashboard and chart exports
├── requirements.txt              # Python dependencies
├── README.md                      # Project documentation (this file)
└── .gitignore                    # Files to ignore in version control
```

## Files Description

| File | Description |
|------|---|
| `Amazon.csv` | Source dataset with 800 customer records and 24 features |
| `MarketAnalysis.ipynb` | Complete Jupyter notebook with all analysis and code |
| `README.md` | Project documentation and insights |
| `requirements.txt` | Python library dependencies |

## Key Metrics & KPIs

| Metric | Value | Insight |
|--------|-------|---------|
| Total Customers | 800 | Dataset size |
| Average Satisfaction | 3.01/5 | Moderate satisfaction, room for improvement |
| Frequent Buyers | 135 (16.9%) | Core customer base |
| Occasional Buyers | 530 (66.3%) | Largest untapped growth segment |
| At-Risk Customers | 135 (16.9%) | Retention priority |
| Top Category | Clothing & Fashion | 400+ purchases |
| Cart Abandonment Driver | Shipping Costs | 1st priority to address |
| Avg Review Dependency Impact | 0.18 points | Moderate negative correlation with satisfaction |

## How to Run

### Prerequisites
```bash
Python 3.7+
Jupyter Notebook
```

### Installation
```bash
# Clone the repository
git clone <repository-url>
cd market-basket-analysis

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook

# Open MarketAnalysis.ipynb
```

### Required Libraries
```python
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
scipy>=1.7.0
```

## Author
**Himanshu B. Chikhlonde**
- Data Science Enthusiast
- Specialized in Customer Analytics & Market Basket Analysis

## Certification
- **Data Management and Analysis with MS Excel** - Internshala Trainings (June 2026)
  - Advanced Excel Functions & Formulas
  - Data Analysis & Summarization
  - Pivot Tables, Pivot Charts, Power Pivot
  - Excel Automation Techniques

## References & Resources
- Dataset: Amazon Customer Behavior Survey
- Analysis Tools: Python Data Science Stack
- Clustering Algorithm: K-Means (Scikit-learn)
- Visualization Framework: Matplotlib & Seaborn

## Future Enhancements
- [ ] Implement RFM (Recency, Frequency, Monetary) analysis
- [ ] Add predictive models for customer churn
- [ ] Develop recommendation engine using collaborative filtering
- [ ] Create interactive dashboards (Tableau/Power BI)
- [ ] Perform A/B testing for shipping cost impact
- [ ] Implement time-series analysis for seasonal trends
- [ ] Develop customer lifetime value (CLV) models

## Contact & Collaboration
For questions, suggestions, or collaboration opportunities, feel free to reach out!

---

**Last Updated:** June 2026
**Project Status:** Complete
**License:** MIT (or your preferred license)