
FINAL PROJECT - RIZ REZA YAW
# HI-2025_Final_Project
This is for our final project in HI-2025
## PROJECT DESCRIPTION
We decided to use a dataset that focused on Lung Cancer and the potential early stage risk factors. Lung cancer is the leading cause of cancer related death and we  wanted to create a predictive model that could predict whether or not someone has Lung Cancer or not based on the early risk factors. 

## METHOD
Since we are using Decision Tree and Naïve Bayes models, we only encoded the truly categorical text columns — GENDER and LUNG_CANCER. We used LabelEncoder to convert them into numeric form. The other variables (like SMOKING, ANXIETY, etc.) were already coded as 1 and 2, which represent categorical responses, so WE didn’t re-encode them. These models can handle that format directly, and keeping it simple helps avoid unnecessary complexity.

## RESULTS
Ultimately, we were able to create a successful model. Below are the results. 

Decision Tree Classifier (5-Fold Cross-Validation with Shuffling):
Accuracy: 91.91%
Sensitivity (Recall): 0.96
Specificity: 0.67
Positive Predictive Value (PPV): 0.95
Negative Predictive Value (NPV): 0.68
F1 Score: 0.95

Naïve Bayes Classifier (5-Fold Cross-Validation with Shuffling):
Accuracy: 88.03%
Sensitivity (Recall): 0.94
Specificity: 0.44
Positive Predictive Value (PPV): 0.92
Negative Predictive Value (NPV): 0.53
F1 Score: 0.93

Decision Tree Accuracy:   91.91%
Naïve Bayes Accuracy:     88.03%

Decision Tree performed better based on accuracy.
It is important to note that the dataset used in this study is imbalanced, with 87.4% of the cases classified as having lung cancer and only 12.6% as non-cancer. This imbalance can potentially bias the predictive models toward the majority class, leading to inflated performance metrics such as accuracy while compromising the model’s ability to correctly identify minority class instances. Although cross-validation was used to mitigate overfitting, future iterations of this analysis should consider applying resampling techniques such as the Synthetic Minority Over-sampling Technique (SMOTE) to balance the class distribution during training. This would help improve the model’s sensitivity to the minority class and enhance its generalizability, particularly for clinical applications where detecting non-cancer cases accurately is equally critical.

## DISCUSSION AND CONCLUSION
This project aimed to predict lung cancer outcomes using supervised machine learning models on a structured dataset. After data cleaning, label encoding, and feature normalization, we visualized key patterns in the data and built predictive models using Decision Tree and Naïve Bayes classifiers.

To ensure fair evaluation, we used 5-fold cross-validation with shuffling, which helps account for variability in data and avoids overfitting to a single train/test split. Our results showed that both models performed reasonably well, with the Decision Tree classifier achieving slightly higher accuracy and more consistent performance in identifying cancer-positive and cancer-negative cases.

The overall findings indicate that machine learning can be effectively used for predictive modeling in lung cancer data, even with a relatively small dataset.

However, this project also has several limitations:

 - Limited dataset size (n=309) may reduce the generalizability of the models.
 - No hyperparameter tuning was performed, which could improve model performance.
 - Imbalanced features and potential multicollinearity may affect the accuracy of Naïve Bayes, which assumes feature independence.
 - The dataset was not validated on an external or real-world clinical dataset, which is essential before clinical use.
 - Future work may include testing more advanced models (e.g., Random Forests or Support Vector Machines), applying SMOTE or other techniques to address potential class imbalance, and validating the model on external datasets.

Overall, this project demonstrates the potential of using simple machine learning algorithms for healthcare prediction tasks and sets the stage for more advanced exploration.

It is important to note that the dataset used in this study is imbalanced, with 87.4% of the cases classified as having lung cancer and only 12.6% as non-cancer. This imbalance can potentially bias the predictive models toward the majority class, leading to inflated performance metrics such as accuracy while compromising the model’s ability to correctly identify minority class instances. Although cross-validation was used to mitigate overfitting, future iterations of this analysis should consider applying resampling techniques such as the Synthetic Minority Over-sampling Technique (SMOTE) to balance the class distribution during training. This would help improve the model’s sensitivity to the minority class and enhance its generalizability, particularly for clinical applications where detecting non-cancer cases accurately is equally critical.
