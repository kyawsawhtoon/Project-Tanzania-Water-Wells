# Project Goal
The goal of this project is to construct a classification model that can be used to predict the condition of water wells in Tanzania. This model will classify the condition of water wells into 3 categories namely -

functional - the waterpoint is operational and there are no repairs needed
functional needs repair - the waterpoint is operational, but needs repairs
non functional - the waterpoint is not operational
To construct this model, I will use the data from Taarifa and the Tanzanian Ministry of Water. My approach for this project is to follow the OSEMN framework. The steps of this framework is as follow -

Obtain the data
Scrub the data
Explore the data
Model the data
Interpret the data

# Project Conclusion
The Random Forest Classifier with GridSearchCV has the overall highest scores. The Accuracy and F1 scores around 70% is not great but it is signficantly better than 33% of randomly selecting between 3 labels.

One thing to focus here is the recall score of 'functional needs repair' and 'non functional' labels of each model. The recall score is vital it tells us the proportion of actual positives that was identified correctly by our model. In other words, it tells us our model's ability to accurately predict the percentages of water wells that are either functional but needs repair, or non functional. If our model has good recall scores for these two labels, the Tanzanian Ministry of Water can use it in this water well maintenance efforts. By focusing on the recall, we might be compromising the accuracy scores of these two labels. Accuracy tell us the proportion of positive identifications by our model that is actually correct. However, it is quite okay to compromise accuracy here for better recall scores because it will be more detrimental to have a non-functional or a water well that needs repairs identified as functional. In this case, the people who use this particular water well will be out of clean water. On the other hand, if a functional water well is predicted as non-functional or needs repair, it will just waste some of the maintanence team's time to check if the water well is as predicted.

The Random Tree Classifier with GridSearchCV has recall scores of 0.5 for 'functional needs repair' and 0.71 for 'non functional'. There are some models such as XGBoost and SVM which have higher recall scores for 'functional needs repair' label but the Random Tree Classifier with GridSearchCV model has the highest recall score for 'non functional'. Therefore, we will select the Random Tree Classifier with GridSearchCV as our model since it has the highest accuracy, f1 and the recall score for 'non functional' label.



# Repository Files
The followings are the file you can find in this repository and their descriptions.

Module 3 - Final Project (Pump it Up).ipynb - Module 3 Final Project's Jupyter Notebook.
presentation.pdf - High-level presentation of methodology and recommendations for non-technical stakeholders
README.md - Descriptions of contents of the repository
TrainingSetValues.csv -	The independent variables for the training set
TrainingSetLabels.csv - The dependent variable (status_group) for each of the rows in Training set values
TestSetValues.csv - The independent variables that need predictions
SubmissionFormat_Complete.csv	- The predictions generated by the final model
