# credit_risk_loan_default_analysis
Credit risk analysis and loan default prediction using Power BI

Analyzed 5,000 sampled loan records to identify key drivers of credit default, segment borrowers by risk profile, and recommend strategies to improve credit assessment.

Tools

Power BI (Power Query for data cleaning, DAX for measures and calculated columns, interactive multi-page dashboard)

Data Source

Loan Default Dataset — Kaggle (148,670 original records, randomly sampled to 5,000 for analysis)

Process


->Data Cleaning (Power Query): Fixed data types, standardized inconsistent categorical values (Region capitalization, loan purpose codes), imputed missing income/DTI/LTV values, engineered features (DTI_Bucket, Credit_Score_Band, Default_Flag)

->Exploratory Analysis: Built default rate breakdowns by credit score, DTI, region, loan purpose, and age using DAX measures and Power BI visuals

->Risk Segmentation: Built a weighted scorecard (credit score + DTI + LTV) to classify borrowers into Low/Medium/High Risk, validated against actual default outcomes

->Dashboard: Interactive 3-page Power BI report with KPI cards, slicers, drill-through to loan-level detail, and cross-filtering


Key Findings


->Missing DTI values were themselves a strong risk signal — loans with unrecorded DTI defaulted at ~67.6%, nearly 3x higher than any populated DTI bucket

->Credit score showed minimal standalone predictive power in this dataset — default rates stayed within a narrow 24-25% band across all score bands

->The risk scorecard achieved a ~3x separation in default rate between Low Risk (~12%) and High Risk (~34%) segments, with a reasonably balanced segment size distribution


Recommendations


->Treat missing DTI disclosure as a risk flag during underwriting rather than a neutral data gap

->Weight DTI and LTV more heavily than credit score in risk-based pricing decisions

->Apply additional verification or tiered pricing for loans in the High Risk segment
