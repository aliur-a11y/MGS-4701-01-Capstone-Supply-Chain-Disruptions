# MGS-4701-01-Capstone-Supply-Chain-Disruptions
Introduction
Background
Modern supply chains are highly intricate systems involving regional suppliers, transportation, and production facilities. When one part of the chain is disrupted, it causes a "ripple effect" leading to delays, increased costs, revenue loss, and decreased customer satisfaction. Common disruptions include cyber-attacks, labor strikes, factory incidents, and port congestion. Rather than relying on reactive strategies, this project utilizes machine learning and predictive analytics to help businesses prepare for future disruptions and estimate recovery durations.

Explore
* Which operational and logistical variables drive disruption outcomes?
* How disruption types (e.g., natural disasters, cyberattacks) relate to recovery time.
* The effectiveness of machine learning for estimating recovery risk.
* The most significant variables for model predictions.

Executive Summary
The research attempts to identify factors that influence supply chain recovery outcomes using the following methodologies:
* Data Sourcing: Utilized a Kaggle dataset containing 100,000 disruption events across five industries.
* Data Preprocessing: Cleaned 15 variables, performed feature engineering, and normalized data using scaling techniques.
* Exploratory Data Analysis (EDA): Summarized characteristics through statistical summaries and visual plotting (histograms, box plots, scatter plots).
* Correlation Analysis: Generated heatmaps to identify strong relationships between features and the target variable, full_recovery_days.
* Dimensionality Reduction: Used Principal Component Analysis (PCA) to interpret the complex dimensions of the data.
* Predictive Modeling: Built a Random Forest Regressor to handle non-linear relationships and assess feature importance.

Results
Exploratory Data Analysis:
* Electronics is the most represented industry, and the Asia-Pacific region is the dominant supplier region.
* Cyberattacks and geopolitical issues show wider variability and generally longer recovery periods compared to port congestion.
* Higher disruption severity and production impact are strongly associated with longer recovery times.
Predictive Analytics:
* A Random Forest Regressor was selected for its ability to handle non-linear relationships and provide feature importance insights.
* PCA revealed that 16 components were required to explain 80% of the variance, highlighting the dataset's complexity.

Methodology
Data Collection & Preprocessing
* Source: Supply Chain Disruption and Recovery dataset from Kaggle.
* Cleaning: Verified null values and dropped the disruption_id column as it lacked predictive power.
* Feature Engineering: Created severity_impact by multiplying disruption severity and production impact percentage to capture compound effects.
* Encoding: Applied label encoding for ordinal features (supplier size/region) and one-hot encoding for mitigation strategies (response_type).
* Scaling: Normalized continuous variables like revenue_loss_usd using StandardScaler.
* Splitting: Used an 80/20 train-test split for model evaluation.
EDA with Visualization
* Histograms: Plotted recovery time distributions to check for skewness.
* Box Plots: Identified outliers representing valid high-impact crises rather than data errors.
* Heatmaps: Used to identify the strongest statistical predictors for the target variable.
Predictive Analytics
* Primary Model: Random Forest Regressor.
* Principal Component Analysis (PCA): Conducted on standardized, one-hot encoded predictor matrices to identify key data dimensions like "disruption intensity" and "supplier resilience".
* Evaluation Metrics: Measured performance using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared ($R^2$).

Conclusion
* Severity & Recovery: Disruptions with higher severity scores and larger production impacts consistently lead to longer recovery periods.
* Disruption Specificity: Because different types of disruptions (like cyber incidents) are more unpredictable, businesses require flexible, industry-specific contingency plans.
* Supplier Resilience: Larger suppliers use backup systems more frequently; relying on a single Tier 1 supplier significantly increases financial risk.
* Proactive Planning: Using predictive models allows organizations to prioritize high-severity risks and allocate resources more effectively before a crisis escalates.

Additional Things to Consider
* Complex Variables: PCA showed that supply chain outcomes are influenced by many independent factors rather than just a few variables.
* Non-linear Relationships: The findings highlight a need for machine learning models that can specifically handle non-linear relationships between operational variables. 
