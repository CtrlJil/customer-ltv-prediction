## Customer Lifetime Value (CLTV) Prediction using RFM Analysis



![Growth_graph](https://i.postimg.cc/Hx3pdd1Q/bar-graph-business-growth-pastel-color-3d-render-free.png)





## Table of Contents

- [Project Overview](#project-overview)

- [Problem Statement](#problem-statement)

- [Data Sources](#data-sources)

- [Methodology](#methodology)

&nbsp; - \[RFM Analysis](#rfm-analysis)

&nbsp; - \[LTV Prediction Model](#ltv-prediction-model)

- \[Key Findings \& Insights](#key-findings--insights)

- \[Project Structure](#project-structure)

- \[Getting Started](#getting-started)

&nbsp; - [Prerequisites](#prerequisites)

&nbsp; - [Installation](#installation)

&nbsp; - [How to Run the Notebook](#how-to-run-the-notebook)

- [Future Work](#future-work)

- [Contact](#contact)



---



## Project Overview



This project focuses on predicting \*\*Customer Lifetime Value (CLTV)\*\*, a critical metric for businesses to understand the long-term profitability of their customer base. By leveraging \*\*RFM (Recency, Frequency, Monetary) analysis\*\* and machine learning techniques implemented in \*\*Python\*\*, we aim to forecast the future revenue contribution of individual customers. This enables data-driven decision-making for targeted marketing campaigns, personalized customer engagement, optimal resource allocation, and enhanced customer retention strategies. The insights derived can help businesses identify their most valuable customers, anticipate churn, and optimize customer acquisition costs.



## Problem Statement



In many businesses, a significant portion of revenue comes from a relatively small segment of highly valuable customers. However, identifying these high-value customers early and understanding their potential future contribution can be challenging. Without a robust CLTV prediction model, marketing efforts can be untargeted, leading to inefficient spend on customers with low potential lifetime value, and missed opportunities to nurture high-potential customers. This project addresses the need for a systematic approach to:

1.  Segment customers based on their historical behavior.

2.  Quantify the predicted future value of each customer.

3.  Provide actionable insights to improve customer relationship management and overall business profitability.



## Data Sources

The analysis for this project was conducted using a transactional dataset.



* \*\*Dataset:\*\* `(Online Retail Dataset from UCI Machine Learning Repository)`

* \*\*Source:\*\* `(https://archive.ics.uci.edu/ml/datasets/Online+Retail)`

* \*\*Data Description:\*\* This dataset contains transactional data for a UK-based online retail store. Key features include:

&nbsp;   * `InvoiceNo`: Invoice number.

&nbsp;   * `StockCode`: Product (item) code.

&nbsp;   \* `Description`: Product description.

&nbsp;   \* `Quantity`: The quantity of each item per invoice.

&nbsp;   \* `InvoiceDate`: Invoice date and time.

&nbsp;   \* `UnitPrice`: Unit price.

&nbsp;   \* `CustomerID`: Customer number (a unique identifier for each customer).

&nbsp;   \* `Country`: Country of residence for the customer.



\## Methodology



The project follows a structured approach combining data preprocessing, RFM segmentation, and predictive modeling:



\### RFM Analysis



\*\*Recency, Frequency, and Monetary (RFM)\*\* analysis is a marketing technique used to quantitatively rank and group customers based on their buying habits.

\* \*\*Recency (R):\*\* How recently did the customer make a purchase? (Calculated as days since last purchase).

\* \*\*Frequency (F):\*\* How often do they purchase? (Calculated as total number of purchases).

\* \*\*Monetary (M):\*\* How much money do they spend? (Calculated as total money spent).



Customers are segmented into various groups (e.g., "Champions," "Loyal Customers," "At Risk," "Lost") by assigning scores to each RFM dimension, allowing for targeted strategies.



\### LTV Prediction Model



Following RFM segmentation, various models can be applied for CLTV prediction. In this project, we explored and implemented:

\* \*\*(Probability Models like BG/NBD and Gamma-Gamma, or Regression Models).\*\*

&nbsp;   \* \*\*Probabilistic Approach (BG/NBD Model):\*\* Used to predict the number of future transactions a customer will make within a given time frame.

&nbsp;   \* \*\*Monetary Value Prediction (K-means):\*\* Used to predict the average monetary value of a customer's transactions, conditional on them making a purchase.

&nbsp;   \* \*\*Integration:\*\* The outputs from these models are then combined to calculate the predicted CLTV.

\* \*\*Key Steps:\*\*

&nbsp;   \* Data cleaning and feature engineering to derive RFM metrics.

&nbsp;   \* Application of the chosen LTV model(s).

&nbsp;   \* Model training, validation, and evaluation.

&nbsp;   \* Prediction of CLTV for each customer.



\## Key Findings \& Insights


\* \*\*Customer Segmentation:\*\* We successfully identified 3 distinct customer segments based on RFM scores, allowing for differentiated marketing approaches. For example:

&nbsp;   \* \*\*Champions (High R, High F, High M):\*\* Our most valuable customers, highly engaged and profitable. Strategies focus on retention and loyalty programs.

&nbsp;   \* \*\*New Customers (High R, Low F, Low M):\*\* Recent acquisitions with potential. Focus on onboarding and initial engagement.

&nbsp;   \* \*\*At Risk (Low R, High F, High M but dropping):\*\* Valuable customers showing signs of reduced activity. Re-engagement campaigns are crucial.

\* \*\*LTV Distribution:\*\* The predicted CLTV exhibits a skewed distribution, highlighting a small segment of customers contributing disproportionately to future revenue.

\* \*\*Predictive Power:\*\* The model demonstrates `(strong)` predictive power, with `(an average error of 0.010%)'.

\* \*\*Actionable Recommendations:\*\*

&nbsp;   \* Tailor marketing messages to different RFM segments (e.g., exclusive offers for Champions, win-back campaigns for At Risk customers).

&nbsp;   \* Optimize customer acquisition by focusing on channels that yield customers with higher predicted LTV.

&nbsp;   \* Invest in retention strategies for high-LTV customers, as acquiring new customers is often more expensive.


\## Project Structure



customer-ltv-prediction/

├── your\_notebook\_name.ipynb   # Main Jupyter Notebook with analysis and model

├── data/                       # Directory for raw and processed data

│   └── (customer\_LTV\_prediction.csv)

├── visuals/                    # Directory for any generated plots or banner images

│   └── (project\_banner.png)

├── .gitignore                  # Specifies intentionally untracked files to ignore

├── README.md                   # This file

└── requirements.txt            # List of Python dependencies

