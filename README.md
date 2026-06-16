🛒 The Effect of Website User Experience (UX) on Customer Purchase Decisions


CIS3032 – E-Commerce and Digital Marketing

Faculty of Computing, University of Sri Jayewardenepura

Author: W.K.S.D. Walallawita | FC223044




📄 Overview

This project investigates how website User Experience (UX) dimensions influence customer purchase decisions in e-commerce environments. Using behavioural analytics and machine learning on a large-scale real-world dataset of 12,330 e-commerce sessions, the study identifies the UX factors that most strongly predict consumer purchasing intentions and develops a validated predictive model for purchase intent classification.


📁 Repository Structure

├── CIS3032_FC223044.ipynb        # Main Jupyter Notebook (analysis & models)
├── online_shoppers_intention.csv # Dataset (Sakar et al., 2019)
├── README.md                     # Project documentation


📊 Dataset

Online Shoppers Purchasing Intention Dataset

Source: UCI Machine Learning Repository

Original Paper: Sakar, C.O. et al. (2019) – Real-Time Prediction of Online Shoppers' Purchasing Intention Using Machine Learning, Neural Computing and Applications.

PropertyDetailTotal Sessions12,330Features18 (behavioural & contextual)Target VariableRevenue (Boolean – purchase or no purchase)Conversion Rate15.47% (1,908 purchasing sessions)Missing ValuesNone

Key Variables

VariableTypeDescriptionPageValuesContinuousMean page value before transaction (strongest predictor)ExitRatesContinuousMean exit rate of pages visitedBounceRatesContinuousMean bounce rate of pages visitedProductRelatedContinuousCount of product-related page visitsProductRelated_DurationContinuousTime spent on product pages (seconds)VisitorTypeCategoricalReturning / New / Other visitorMonthCategoricalCalendar month of sessionRevenueBooleanTarget – whether session resulted in a purchase


🔬 Methodology

The notebook implements the following analytical pipeline:

Data Loading & Exploration
        ↓
Preprocessing & Feature Engineering
  (LabelEncoding, MinMaxScaler, Binary Conversion)
        ↓
Descriptive Statistics & Visualisation
        ↓
Pearson Correlation Analysis
        ↓
Hypothesis Testing (t-tests, Chi-square)
        ↓
Machine Learning Models
  ├── Logistic Regression
  ├── Decision Tree Classifier
  └── Random Forest Classifier
        ↓
K-Means Customer Segmentation (k=3)
        ↓
Feature Importance & Findings


📈 Key Results

Model Performance

ModelAccuracyAUC-ROCLogistic Regression87%0.8606Decision Tree88%0.9188Random Forest89%0.9211 ✅

Top Predictive Features (Random Forest)

RankFeatureImportance1PageValues38.12%2ProductRelated_Duration8.93%3ExitRates8.80%4ProductRelated7.23%5Administrative_Duration5.87%

Customer Segments (K-Means, k=3)

ClusterLabelSessionsConversion RateCluster 0Engaged Shoppers9,55819.17%Cluster 1Quick-Exit Users8140.37%Cluster 2Passive Browsers1,9583.73%


⚠️ A 51-fold conversion rate difference exists between Cluster 0 and Cluster 1 — entirely attributable to UX behavioural variables.




🛠️ Requirements

Python 3.8+
pandas
numpy
scikit-learn
scipy
matplotlib
seaborn
jupyter

Install all dependencies with:

bashpip install pandas numpy scikit-learn scipy matplotlib seaborn jupyter


▶️ How to Run


Clone the repository


bashgit clone https://github.com/your-username/your-repo-name.git
cd your-repo-name


Install dependencies


bashpip install -r requirements.txt


Launch Jupyter Notebook


bashjupyter notebook CIS3032_FC223044.ipynb


Run all cells — Kernel → Restart & Run All



📌 Main Findings


PageValues is the single strongest predictor of purchase intention (r = 0.4926, p < 0.000001)
ExitRates has the strongest negative influence on conversion (r = −0.2071)
New visitors convert at nearly double the rate of returning visitors (24.91% vs 13.93%)
November is the peak conversion month at 25.35%; February is the lowest at 1.63%
Product page content quality and exit behaviour management are the highest-impact levers for conversion optimisation



📚 References


Sakar, C.O. et al. (2019). Real-Time Prediction of Online Shoppers' Purchasing Intention. Neural Computing and Applications. https://archive.ics.uci.edu/dataset/468
Lindgaard, G. et al. (2006). Attention Web Designers: You Have 50 Milliseconds. Behaviour and Information Technology, 25(2), 115–126.
Baymard Institute. Cart Abandonment Research. https://baymard.com/lists/cart-abandonment-rate
Google. Mobile Page Speed Industry Benchmarks. https://www.thinkwithgoogle.com



⚖️ Ethical Compliance

The dataset used is fully anonymised with no personally identifiable information and is publicly available for academic research via the UCI Machine Learning Repository. No individual informed consent was required.
