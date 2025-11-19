**🔹 Project Overview**

This project demonstrates:

**1.Data Engineering**

Designed a Snowflake data warehouse using the Medallion Architecture

1. RAW (Bronze) – Direct ingestion of CSV files

2. CLEAN (Silver) – Data cleaning, standardization, feature preparation

3. GOLD (Gold) – Customer 360 model, RFM features, churn dataset

**2. ETL / ELT Pipeline**

1. Loaded data from CSV into Snowflake

2. Cleaned nulls, fixed dtypes, standardized labels

3. Created engineered features (age, total spent, total purchases, children count, recency metrics)

**3. Customer 360° Model**

The GOLD layer contains a unified table with:

1. Demographics

2. Spending behavior

3. Purchase frequency

4. Recency & response metrics

5. RFM segmentation fields

6. Final churn label

**4. Machine Learning (Python + XGBoost)**

1. Exported GOLD dataset locally

2. Performed:

3. Data cleaning

4. Feature encoding

5. Train–test split

6. Trained XGBoost Binary Classifier for churn prediction

7. Pushed predictions back to Snowflake (GOLD.CUSTOMER_PREDICTIONS)

**5. Visualization (Tableau)**

Created an interactive Tableau dashboard showing:

1. Total revenue

2. Customer demographic breakdown

3. Spending behavior

4. Campaign response analysis

5. Churn risk segmentation

6. RFM segments

**🏗️ Architecture**


           ┌─────────────────────────────────────────┐
           
           │                
                           **RAW Layer               │
                           
           │        (Ingested CSV Files)**           │
           
           └─────────────────────────────────────────┘
                               │
                               ▼
           ┌──────────────────────────────────────────┐
           │                
                           **CLEAN Layer              │
                           
           │    (Standardization + Feature Cleaning)**│
           
           └──────────────────────────────────────────┘
                               │
                               ▼
           ┌─────────────────────────────────────────┐
           │                 
                       **GOLD Layer  
                                                     │
           │  Customer360 + RFM + Churn Dataset**    │
           
           └─────────────────────────────────────────┘
                               │
                               ▼
           ┌───────────────────────────────────────────┐
           │         
                      **Machine Learning (Python)      │
           
           │     XGBoost Model + Predictions Upload**  │
           
           └───────────────────────────────────────────┘
                               │
                               ▼
           ┌─────────────────────────────────────────┐
           
           │                **Tableau Dashboard**    │
           
           └─────────────────────────────────────────┘


**📁 Repository Structure**


📁 customer360-project

│
├── 📄 README.md

├── 📁 sql/

│   ├── schema_setup.sql

│   ├── raw_clean_gold_queries.sql

│   ├── feature_engineering.sql

│   ├── churn_upload.sql

│
├── 📁 data/

│   ├── raw_customers.csv

│   ├── customer360_gold.csv

│   ├── churn_predictions.csv

│
├── 📁 notebooks/

│   ├── churn_model_xgboost.ipynb

│
├── 📁 dashboards/

│   ├── tableau_screenshots.png

│
└── 📁 diagrams/

    ├── architecture.png
    
    ├── medallion_flow.png

**🔹 Dashboard screenshots**

![**Behavioral Dashboard**](https://raw.githubusercontent.com/SahanaMathad/customer360-snowflake-churn-insights/main/Behavioral%20Analysis%20Dashboard%20(2).png)


![**Age Demographics & Churn Insights**](https://raw.githubusercontent.com/SahanaMathad/customer360-snowflake-churn-insights/main/Age%20Demographics%20%26%20Churn%20Insights.png)


![**Customer Insights Overview**](https://raw.githubusercontent.com/SahanaMathad/customer360-snowflake-churn-insights/main/Customer%20Insights%20Overview.png)



**🛠️ Tools & Technologies**
🔹 Data Engineering

Snowflake (Free Tier)

SQL

Medallion Architecture

🔹 Machine Learning

Python

Pandas

Scikit-learn

XGBoost

🔹 Visualization

Tableau

Matplotlib/Seaborn (optional)

**🔹 Key Features**

1. Fully automated multi-layer warehouse (RAW → CLEAN → GOLD)

2. Customer 360 creation with engineered features

3. End-to-end churn prediction pipeline

4. Upload predictions back to Snowflake

5. BI dashboard for business insights

6. Beginner-friendly Snowflake setup (free tier)

**📊 Dashboard Insights**

The Tableau dashboard provides:

Customer segmentation

Spend patterns

Campaign response behavior

RFM clusters

Churn probability distribution

High-risk customer list

**📌 How to Run the Project**

Load data into Snowflake RAW layer

Run CLEAN layer transformations

Run GOLD layer feature engineering

Download GOLD dataset

Open Python notebook → train ML model

Upload predictions to Snowflake

Connect Tableau → create visual dashboard

**🧠 Learnings**

Hands-on experience with Snowflake

Medallion data architecture

SQL transformations and feature engineering

Churn prediction using XGBoost

End-to-end data pipeline design

Business analytics with Tableau

**🤝 Contributing**

Contributions and suggestions are welcome!
Open a PR or reach out if you'd like to collaborate.

**📬 Contact**

**Sahana Mathad
📧 sahanamathad1892@gmail.com**

🔗 LinkedIn:https://www.linkedin.com/in/sahana-mathad/

🔗 GitHub: https://github.com/SahanaMathad/
