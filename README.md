Enhancing Preventive Care Engagement Using Data-Driven Approaches
Overview
This project focuses on improving preventive care engagement among members of a health insurance plan. Preventive care is critical for early detection of health issues, reducing long-term healthcare costs, and improving overall health outcomes. However, a significant portion of members disengage from preventive care services, leading to gaps in care. This project leverages advanced data analytics and machine learning techniques to identify members at risk of disengagement and proposes actionable strategies to improve engagement.

Objectives
The primary objectives of this project are:

Identify At-Risk Members: Predict which members are likely to miss preventive care visits.

Understand Key Drivers: Analyze demographic, behavioral, and healthcare utilization factors that influence preventive care engagement.

Propose Interventions: Recommend targeted strategies to improve preventive care participation among disengaged members.

Methodology
![image](https://github.com/user-attachments/assets/fc6a2dae-7045-4d9e-9a55-3629ee82d9ea)

1. Data Preparation
Data Aggregation: Multiple datasets were aggregated to create a comprehensive member-level view, including demographics, healthcare utilization, and quality metrics.

Feature Engineering: Key features were engineered, such as compliance ratios (e.g., HEDIS compliance) and year-over-year visit ratios (e.g., primary care visits in 2022 vs. 2021).

Data Imputation: Missing values were handled using techniques like mean imputation and zero imputation, depending on the context.

2. Modeling
Model Selection: The XGBoost algorithm was chosen for its ability to handle complex interactions and provide feature importance rankings.

Hyperparameter Tuning: Random Search with 3-fold cross-validation was used to optimize hyperparameters, achieving an AUC-ROC score of 0.782.

Feature Selection: Iterative feature reduction was performed to retain the top 30 most impactful features, such as preventative_visit, generic_grouper, and total_net_paid_pmpm_cost.

3. Model Interpretation
SHAP Analysis: SHAP (SHapley Additive exPlanations) values were used to interpret the model's predictions and understand the contribution of each feature.

Key Insights:

Members with lower healthcare costs and fewer prescriptions were more likely to miss preventive care.

Veterans, especially those with disabilities, showed higher disengagement rates.

Members with long gaps since their last claim were less likely to engage in preventive care.

Key Findings
Low-Cost Members: Members with lower healthcare expenditure and fewer prescriptions were the least likely to attend preventive visits.

Veterans and Disabled Members: Veterans, particularly those with disabilities, had the highest preventive care gaps.

Long Gaps Since Last Claim: Members who had not filed a claim in over 160 days were significantly less likely to engage in preventive care.

Unattributed Providers: Members without an attributed primary care provider were more likely to miss preventive visits.

Recommendations
Based on the analysis, the following strategies are recommended to improve preventive care engagement:

Automated Outreach Campaigns: Use SMS, email, and phone reminders to target low-engagement members, especially those with low healthcare costs and prescription usage.

Pharmacy Partnerships: Collaborate with pharmacies to offer preventive services during prescription pickups and over-the-counter purchases.

Veteran-Specific Programs: Develop tailored outreach programs for veterans, including in-home screenings and partnerships with veteran organizations.

Incentives for High-Risk Members: Offer financial incentives, such as waived copays, to encourage preventive care participation.

Digital Engagement Tools: Promote online scheduling and reminders through web portals to increase accessibility and convenience.

Tools and Technologies
Programming Languages: Python (Pandas, NumPy, Scikit-learn)

Machine Learning Framework: XGBoost

Model Interpretation: SHAP (SHapley Additive exPlanations)

Visualization: Tableau, Matplotlib, Seaborn

Future Scope
Geospatial Analysis: Incorporate geographic data to identify regions with limited access to healthcare services.

Social Determinants of Health (SDOH): Integrate SDOH data to better understand barriers to preventive care, such as income, education, and transportation.

Natural Language Processing (NLP): Analyze unstructured data (e.g., call center transcripts) to uncover additional insights into member behavior and preferences.

Psychographic Data: Explore member attitudes and trust in healthcare providers to design more personalized engagement strategies.

Conclusion
This project demonstrates the power of data-driven approaches in identifying and addressing gaps in preventive care engagement. By leveraging advanced analytics and machine learning, targeted interventions can be designed to improve member health outcomes and reduce long-term healthcare costs. The insights and recommendations provided here offer a roadmap for enhancing preventive care participation and ensuring better health for all members.

References
Chen, T., & Guestrin, C. (2016). XGBoost: A scalable tree boosting system. Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD '16).

Lundberg, S. M., & Lee, S.-I. (2017). A unified approach to interpreting model predictions. Proceedings of the 31st International Conference on Neural Information Processing Systems (NIPS '17).

Obermeyer, Z., & Emanuel, E. J. (2016). Predicting the future—Big data, machine learning, and clinical medicine. The New England Journal of Medicine.

