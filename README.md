Title: Unveiling the Relationship between Restaurant Inspection Grades and Economic Development in NYC: A Data Science Journey
Introduction:
New York City (NYC) combines different types of restaurants and eateries, not only a melting pot of cultures but also a paradise for the culinary. In this huge city, it is essential to ensure the safety of the food and it remains the biggest concern regarding the safety of the individuals. In this complex mix of regulatory compliance and economic development, which have been twisted together in way such that it is difficult separate them, this offers a unique way through which to explore the complicated and complex pictorial designs of New York City's restaurant landscape. In this blog, the relationship between restaurant inspection grades and economic prosperity is explained through a data-driven journey by leveraging machine learning models and interdisciplinary insights of New York City.
Literature Review:
Before going through the exploration we have to consider the existing literature, where the significance of integrating restaurant inspection data with business acceleration information is provided. In this literature review, the first dataset gave current inspection data for permitted restaurants and college cafeterias provided a comprehensive look at food safety adhering to regulations in NYC. The dataset ensures a focus on establishment which are currently in operation and maintains the integrity of the analysis where the inactive restaurants and other with dismissed violations were excluded.
The impact of New York City Business Acceleration on new businesses and job creation was tracked by using the second dataset which complemented this regulatory perspective. We can explore the correlation between businesses that receive support from New York City Business Acceleration and their compliance with food safety regulations using the above datasets. The accelerated businesses could be compared by different compliance profile by using this unique intersection which could unveil patterns and dependencies, shedding light on them.
Unit of Analysis:
We focused our attention on individual restaurants and college cafeterias in New York City. In our quest for insights, a unique establishment, as identified by its unique identifier (CAMIS), represented as an independent observation within the dataset. To ensure the relevance and timeliness in the analysis, primarily the focus was on active restaurants that have undergone inspections in the last three years. A detailed exploration of the intersection between food safety regulations and economic support initiatives allows few factors by using a granular examination of them which influence inspection outcomes and business success in the context of the diverse and dynamic NYC restaurant landscape by using this approach.
Importance of Research:
This research is crucial for several reasons:
Public Health Impact: Understanding and predicting restaurant inspection grades is essential for safeguarding public health and preventing foodborne illnesses.
Regulatory Compliance Insights: Analyzing the relationship between establishment details and inspection outcomes provides valuable insights for regulatory bodies to optimize inspection processes.
Economic and Business Development: Exploring the intersection of economic development and regulatory compliance can inform policies that support business growth while ensuring public safety.
Predictive Analytics for Stakeholders: The predictive models developed in this research offer stakeholders proactive tools to anticipate and address compliance issues, fostering a more efficient regulatory environment.
Approach:
I embark on a systematic approach to data analysis with research questions in mind,:
Data Collection and Inspection: We gather datasets from both sources, ensuring completeness and compatibility and conducted a primary inspection whether the data has any discrepancies or any other challenges that are to be faced during this approach.
Exploratory Data Analysis (EDA): conducted a thorough EDA to identify patterns, distributions, and outliers by exploring the relationships between the variables ensuring the quality of data.
The exploratory data analysis of the restaurant inspection dataset indicated that it contained 219,276 records with 27 columns. The data types showed a mix of categorical and numerical features, with many columns containing object data types, suggesting the need for data preprocessing and transformation to ensure consistency and facilitate analysis.
The data contained a variety of unique values across its categorical columns. 'CAMIS', a unique identifier, had 28,784 different values, indicating a large number of records. 'DBA' (Doing Business As) had 22,483 unique values, suggesting a diverse set of businesses. Other columns, like 'BORO', had only six unique values, reflecting the limited number of boroughs in New York City. These variations in unique counts across columns indicated a rich dataset with both broad and narrow scopes, which could impact the modeling approach and analysis.
Inspection data:
The inspection scores' distribution was skewed to the left, indicating that most scores were high, with a lower score tail.
The mode was above 90, suggesting that most inspections resulted in high scores.
Scores ranged from 0 to nearly 100, showing a significant spread and variability.
The presence of peaks at intervals, particularly around 100, hinted at potential scoring system characteristics or patterns in inspection outcomes.
The high concentration of scores near 90 suggested that most inspected entities performed well according to the criteria.
The lower count of scores near 0 might have indicated non-compliance cases, exceptional circumstances, or data errors.

Grades:
Grade A was the most common, with over 175,000 instances, indicating a high occurrence of top performance.
Grade B, with a significantly lower count, was the second most frequent, suggesting a smaller subset achieved this level.
Grades N, C, and Z had much lower counts, indicating that they were less frequently assigned.
Grade P had the fewest occurrences, indicating it might be a special category or rarely awarded.
The significant drop from grade A to other grades suggested a skewed distribution, potentially due to lenient criteria or high overall performance.

Cuisines:
American cuisine dominated the dataset with the highest count among the top 10, indicating a significant presence, likely due to its broad categorization or regional preference.
Chinese cuisine was the second most common, suggesting it also had a strong presence in the dataset, though significantly less than American cuisine.
Coffee/Tea and Pizza were also popular, each with substantial counts, indicating a preference for these types of establishments or dishes.
Latin American and Mexican cuisines had similar counts, hinting at a shared cultural background or similar popularity levels.
The lowest counts among the top 10 were for Caribbean, Japanese, and Italian cuisines, suggesting these were less prevalent but still among the most common.
This distribution indicated that while American cuisine was the most prominent, there was considerable diversity in other popular cuisines, highlighting cultural variety in the dataset's context.

Inspection Dates:
The distribution of inspection dates showed sparse early data, with near-zero counts in the early 1900s, indicating minimal inspections or data collection at that time.
There was a sharp increase in inspections from the late 1990s into the 2020s, with counts rising rapidly, suggesting a significant boost in inspection activity in recent years.
The graph indicated a spike in inspection counts near the early 2020s, implying specific events or regulatory changes led to heightened inspection frequency.
The lowest values of inspection counts occurred in the early 1900s, likely due to fewer regulations, less data collection, or a smaller scope of inspectable entities.
The highest values appeared just before 2020, with the rapid increase in counts potentially driven by regulatory changes or improved data collection practices.
The sharp increase in inspections could be attributed to regulatory changes or improved data collection, leading to more comprehensive reporting.
The data suggested a need for resource allocation to manage the increased inspection workload, indicating organizations may need more inspectors or efficient processes.
The significant rise in inspections highlighted the importance of policy analysis and predictive planning, allowing organizations to anticipate future trends and allocate resources accordingly.

Inspection Scores:
The box plot for inspection scores indicated that the median score was above 50, suggesting that more than half of the scores were in the higher range.
The interquartile range (IQR) was relatively narrow, indicating that the middle 50% of the scores were clustered closely together, showing consistent performance.
Several outliers were observed above the upper whisker, suggesting the presence of some exceptionally high inspection scores.
The highest scores were represented by these outliers, pointing to exceptional compliance or outstanding performance in some inspections.
The lowest value was not at zero, suggesting that there were no extremely low scores, indicating a general adherence to expected standards.
The data suggested a consistent performance across most inspections, with only a few cases scoring significantly higher than the rest.
The outliers might require further investigation to understand the factors contributing to their high scores and to see if these practices could be adopted more widely.
This box plot's interpretation indicated that most facilities or items inspected were meeting standards, with no significant low-scoring outliers. This could suggest effective compliance or potentially less stringent criteria.

Inspection Scores by Grade:
The boxplot displayed inspection scores by grade, with the widest interquartile range (IQR) observed for Grade A, suggesting the highest variability in scores within this grade. The median score for Grade A was around 90, with several outliers above the upper whisker.
Grade B exhibited a narrower IQR compared to Grade A, with a median score around 80 and fewer outliers, indicating more consistent scores but at a lower level.
The median score for Grade C was about 60, with a smaller IQR, indicating that establishments in this grade tended to score within a narrower range and at a lower level compared to Grades A and B.
Grade N had a very narrow IQR with a median score close to 20, suggesting consistent low scores for this grade, without any outliers.
Grade P also displayed a narrow IQR, with a median score around 10, suggesting that establishments in this grade consistently received very low scores with no outliers.
Grade Z showed a median score near 40, with a few outliers indicating better performance compared to Grades N and P but lower than Grades C, B, and A.
The highest scores were observed in the outliers of Grade A, possibly due to exceptional compliance with inspection criteria.
The lowest scores were mainly found in Grades N and P, indicating significant deficiencies or serious issues with compliance or performance.

These insights suggested that inspection scores generally declined from Grade A to Grade Z. Grades A, B, and C had broader score distributions, while Grades N, P, and Z were more concentrated at the lower end of the scale. This pattern might guide decision-making regarding targeted inspections, training, or enforcement to improve compliance among lower-performing grades.
Inspection Scores by Borough:
The box plot displayed the distribution of inspection scores across five boroughs: Bronx, Brooklyn, Manhattan, Queens, and Staten Island, with each borough having a similar median score at approximately 90, suggesting comparable central tendencies.
The interquartile range (IQR) indicated that Manhattan had a slightly tighter distribution of scores, showing less variability, while the Bronx, Brooklyn, and Staten Island displayed slightly larger spreads, indicating greater score variability in these boroughs.
The whiskers, representing the range excluding outliers, demonstrated that the lowest scores in all boroughs hovered just above 50, suggesting a common baseline level of compliance.
Outliers were observed in all boroughs, with the highest outlier score, above 175, in Brooklyn. This indicated that some establishments consistently scored significantly higher than the median.
The spread in the lower quartile was larger in the Bronx, Brooklyn, and Staten Island, implying that these boroughs had more instances of lower inspection scores compared to Manhattan and Queens.
The consistent median scores across boroughs suggested that, on average, inspection outcomes were uniform, indicating a consistent level of compliance.
The presence of high outliers in all boroughs could be due to exceptional performance or different interpretations of scoring criteria, indicating a need for further investigation.
The larger spread of lower scores in the Bronx, Brooklyn, and Staten Island suggested these boroughs might require additional support or targeted interventions to improve compliance and reduce variability.

These insights could help regulatory agencies focus their efforts on reducing score variability in certain boroughs and investigate high outliers to ensure consistent grading standards.
Correlation Matrix:
The heatmap displayed strong positive correlations among geographical features, with ZIPCODE, Community Board, Council District, Census Tract, BIN, and BBL showing high correlation values, often above 0.90.
SCORE, the inspection result variable, exhibited low correlations with the geographical features, with the strongest negative correlation at -0.45 with Latitude and Community Board.
INSPECTION_YEAR and INSPECTION_MONTH had little to no correlation with other features, indicating no clear time-based trends in inspection results.
The highest non-trivial correlations were between Community Board and BIN (0.99) and between Community Board and BBL (0.99), suggesting redundancy in the geographical data.
The absence of strong correlations with SCORE implied that inspection scores were not significantly influenced by location, hinting at consistent inspection standards across regions.
The slight negative correlations between SCORE and some geographical features suggested minor trends, though these were not strong enough to indicate significant biases or patterns.
The high correlation among geographical features suggested a potential for data simplification to avoid redundancy.

Despite the lack of strong correlations, it was crucial to note that correlations do not imply causation, and further analysis would be required to determine any causal relationships or significant patterns.
Data Cleaning and Preprocessing: addressed the missing values, outliers, and inconsistencies in datasets by standardizing the textual data for consistent merging and allotting different date fields to appropriate format.
The inspection data exhibited various degrees of missing values across its columns, with some columns like GRADE DATE and GRADE having over 50% missing data. Additionally, the Location Point1 column had a complete 100% missing value rate, indicating it might require removal. Missing data in key columns such as SCORE, ZIPCODE, VIOLATION CODE, and VIOLATION DESCRIPTION suggested that imputation or other preprocessing techniques would be necessary to ensure data completeness and reliability.
After applying imputation methods, the percentage of missing values in most columns was significantly reduced. The categorical columns, such as DBA, ACTION, GRADE, and CUISINE DESCRIPTION, had no missing values. However, some columns like VIOLATION CODE and VIOLATION DESCRIPTION still had a small percentage of missing data, indicating room for further data cleaning.
After addressing missing values, the dataset's percentage of missing data across all columns was reduced to zero. The imputation process used various strategies, including mode-based filling for categorical data and median-based filling for numerical data. Additionally, forward filling was employed for date columns to ensure continuity. As a result, the dataset no longer contained any missing values across all its critical columns, making it ready for further analysis and modeling.
The dataset was checked for duplicate rows, and it was found that there were no duplicate records, indicating that the data was clean in terms of redundancy. This ensured that further analysis and modeling would not be affected by repeat or identical entries.
After preprocessing the business acceleration dataset, there were 4,938 unique business names, 5,050 unique establishment streets, and 297 unique ZIP codes. In addition, 330 unique types of cuisine, 86 distinct values for the number of employees, and 2 unique categories indicating missing values in the "Type of Cuisine" column were observed. The dataset also had additional one-hot encoded categorical columns indicating establishments by borough, business sector, and establishment category, with values typically having 2 unique representations due to binary encoding.
Outlier Handling for Inspection Data
In the analysis of numerical outliers, the following was observed:
The majority of the outliers were associated with SCORE, with a total of 10,724 outliers, indicating significant variability in inspection scores.
INSPECTION_YEAR had 15,629 outliers, suggesting fluctuations over the time range examined.
Latitude and Longitude had 7,276 and 10,789 outliers, respectively, pointing to inconsistencies in geographical data.
Census Tract had 11,296 outliers, hinting at possible discrepancies in data classification.

Conversely, some features, such as ZIPCODE, BIN, BBL, and Community Board, had no outliers, indicating stability in these areas.
After removing outliers, the dataset's shape changed to 169,641 rows and 29 columns. This reduction from the original dataset indicates that a significant portion of data points were considered outliers and excluded from the analysis, suggesting that they fell outside the typical range or distribution of the dataset. This step likely improved the dataset's reliability by focusing on the majority of data within a consistent range.
Merging Datasets: merged datasets using common keys and validate the merged dataset for ensuring correctness and completeness.
After merging, This dataset contains information on various establishments, including inspection details, business sector, and employee count. The first four rows represent data for the same entity, "Kings Kitchen" in Manhattan, with different inspection dates indicating multiple inspections. The fifth row indicates a different "Kings Kitchen" in Brooklyn, showing similar business sector and employee information, but with variations in ZIP code, phone number, and inspection details.
Feature Engineering: extracted the relevant features and create new variables if needed such as from dates, such as month or season.
This chart showed the cumulative explained variance against the number of principal components, providing insights into how much variance was retained as additional components were included:
The curve had an "elbow" shape, with a steep rise followed by a flattening as more components were added. This indicated diminishing returns in explained variance after a certain point.
The cumulative explained variance approached 1.0, indicating that almost all data variance was captured when using enough components.
The steepest increase occurred with the first few components, suggesting that they explained a significant proportion of the variance.

The optimal number of components was determined by where the curve flattened, typically where adding more components provided minimal additional explained variance. This "elbow" appeared at about nine components, suggesting that these captured the critical variance while avoiding over-complexity.
PCA Components Matrix:
The PCA components matrix revealed the contributions of various features to the principal components, indicating which variables were most influential in explaining the dataset's variance:
Strong Loadings: SCORE, ZIPCODE, and geographical indicators like Latitude and Longitude had substantial loadings in the first few principal components, suggesting that these features contributed significantly to the overall variance.
Specific Patterns: Community Board and Council District had high positive loadings in the first component, indicating a strong correlation with the principal direction of variance.
Variability: Other features, such as INSPECTION_YEAR and INSPECTION_MONTH, showed variable loading across multiple components, reflecting a diverse influence on the dataset's structure.

This analysis highlighted the most significant features and indicated which variables could be key drivers in further analysis or modeling.
The most significant features by PCA components were identified as follows:
Component 1 highlighted geographical identifiers such as Community Board, BIN, BBL, ZIPCODE, and Council District, indicating a strong geographic influence.
Component 2 focused on Opening Year, Number Of Employees, Type_of_Cuisine_Missing, Longitude, and Latitude, suggesting a connection between organizational attributes and location.
Component 3 also emphasized Longitude, Latitude, and Census Tract, indicating the continued importance of geographical variables.
Component 4 included INSPECTION_YEAR, INSPECTION_MONTH, and Longitude, suggesting a time-based influence on these principal components.
Component 5 shifted towards Opening Month, Opening Year, Type_of_Cuisine_Missing, SCORE, and CAMIS, highlighting a mix of time-based and inspection-related features.

Overall, this breakdown shows a balance between geographical, temporal, and organizational variables, suggesting a multi-faceted structure within the dataset.
Machine Learning Model : the classification models that were suited for predicting inspection grades were selected which includes
Random Forest:
The Random Forest classifier achieved an accuracy of 99.79%, indicating a high level of predictive accuracy.
Confusion Matrix:
Grade 0 showed the highest accuracy with only a few misclassifications.
Grades 1, 2, 3, and 5 had nearly perfect confusion matrices with minimal misclassifications.
Grade 4 exhibited the most misclassifications, with 8 instances where the predictions were incorrect.

Classification Report:
Precision, recall, and f1-score were generally high across all grades, with most values close to 1.00.
The f1-score for Grade 4 was lower at 0.82, indicating less reliable predictions for this category.
The weighted average of precision, recall, and f1-score across all grades was close to 1.00, reflecting a well-balanced model.

Insights:
The high accuracy suggests that the Random Forest classifier is robust and effective.
The lower scores for Grade 4 may indicate a need for additional model tuning or data refinement in this category.

XGBoost:
The XGBoost classifier achieved an accuracy of 99.79%, indicating a high level of correct predictions.
Confusion Matrix:
Grade 0 had nearly perfect classification, with 12,451 correctly identified out of 12,455.
Grades 1, 2, 3, and 5 were also well classified, with the majority of instances correctly predicted.
Grade 4 showed some misclassification, with 6 out of 26 instances wrongly predicted.

Classification Report:
Precision, recall, and f1-score for Grade 0 were all 1.00, indicating perfect or near-perfect classification.
Grades 1, 2, 3, and 5 also had high precision and recall, suggesting consistent performance across these grades.
Grade 4 had a precision of 1.00 but a recall of 0.77, indicating some underperformance in identifying all instances of this grade.

Insights:
XGBoost showed exceptional performance across most grades, with high accuracy, precision, recall, and f1-score.
Grade 4 was the exception, where the lower recall indicated that not all instances were correctly identified.

Feature Importance Analysis: assessed the importance of different features in analyzing inspection grades and to identify influential factors feature important analysis was utilised.
The feature importance plot highlighted the influence of various features on the prediction for a single instance regarding "Class 1".
Features with negative impact included Feature 3 (approximately -0.71), Feature 13 (around -0.88), Feature 10 (about -0.84), and Feature 2 (just below -0.83).
The only feature with a positive influence was Feature 4, with a value slightly over 0.43, suggesting a weaker contribution to the prediction.
This plot represented local explanations, focusing on individual instances, rather than global trends, making it less applicable to the entire dataset.
Without specific context on what the features represent, the reasons for the observed trends were speculative and subject to further investigation.

Hyperparameter Tuning: fine-tuneed model hyperparameters to enhance performance by using techniques like cross validation for optimal parameter selection.
Hyperparameter Tuning: A grid search was conducted to find the best hyperparameters for a Random Forest model. The parameters explored included different numbers of estimators, maximum features, and maximum depth.
Optimal Configuration: The best configuration found was with a max_depth of None, max_features set to 'sqrt', and n_estimators set to 100.
Cross-Validation Accuracy: Using 5-fold cross-validation, the best score achieved with this configuration was 99.60%, indicating a highly accurate model.
Efficiency and Performance: These results suggest that even with a smaller number of estimators (100), the model achieved high accuracy, demonstrating an efficient and effective setup.

Conclusion:
The project concluded that analyzing restaurant inspection data, combined with business acceleration data, provided valuable insights into trends and patterns affecting compliance and business success. By removing outliers, handling missing values, and conducting exploratory data analysis, the project identified critical factors influencing inspection outcomes.
The machine learning models built and evaluated, including Random Forest, and XGBoost, demonstrated varying levels of accuracy, with Random Forest emerging as the most effective model with an accuracy of 99.79%. The project employed hyperparameter tuning and model interpretation techniques, like LIME, to optimize and explain model predictions.
Overall, the project successfully addressed the business case of improving regulatory compliance, enhancing resource allocation for inspections, and supporting business development in the restaurant sector. The insights derived from this project can inform strategies to improve public health, guide restaurant operations, and support business success in New York City and potentially other regions with similar regulatory frameworks.
