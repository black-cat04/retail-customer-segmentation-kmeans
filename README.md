# Retail Customer Segmentation using K-Means

## Overview
This repository presents an end-to-end retail customer segmentation project using unsupervised machine learning. The analysis applies K-Means clustering to customer behaviour data to uncover actionable segments that can support targeted marketing, retention planning, and customer lifecycle strategy.

## Business Problem
Retail organisations often struggle to personalise engagement for a diverse customer base. This project addresses that challenge by grouping customers into interpretable behavioural segments using RFM metrics (Recency, Frequency, Monetary), enabling more effective promotional targeting and customer retention initiatives.

## Dataset
The project uses the Retail Customer and Transaction Dataset from Kaggle:

https://www.kaggle.com/datasets/raghavendragandhi/retail-customer-and-transaction-dataset

## Technologies Used
- Python
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn
- kagglehub

## Methodology
1. Downloaded the retail dataset from Kaggle.
2. Explored customer, transaction, review, and support ticket tables.
3. Engineered an RFM-based feature set for customer behaviour analysis.
4. Applied preprocessing steps including outlier capping, power transformation, and scaling.
5. Evaluated clustering quality using the Elbow Method and Silhouette Score.
6. Interpreted the resulting clusters into business-ready customer personas.

## Key Results
- Developed a complete segmentation workflow for retail customer analysis.
- Identified four meaningful customer clusters using K-Means.
- Achieved a final silhouette score of 0.2922 for the selected clustering solution.
- Derived interpretable personas suitable for business decision-making and targeted marketing.

## Repository Structure
- notebook/2025em1200017_ApexProject_Week9.ipynb — main analysis notebook
- report/2025EM1200017_ApexProject_Report.docx — project report
- report/Retail_Customer_Analytics_Report.pdf — optional report PDF if available
- data_dictionary/2025EM1200017_DataDictionary.xlsx — data dictionary
- docs/Problem statement.png — assignment problem statement
- docs/Week Five Feedback.txt — feedback notes
- docs/final assignment details.pdf — assignment details PDF
- images/ — directory for future visual assets
- README.md — project overview and documentation
- .gitignore — repository ignore rules
- LICENSE — MIT license
- requirements.txt — Python dependencies for reproducing the analysis

## Future Improvements
- Add review and support ticket data as post-hoc descriptors for richer profiling.
- Compare K-Means with alternative clustering approaches such as DBSCAN or Gaussian Mixture Models.
- Build an interactive dashboard for stakeholder exploration.
- Productionise the workflow for real-time customer scoring.

## Author
Yashvee Ranjan
