#**Credit_Risk_Analysis**

##**Overview of the analysis**
Through the Credit Risk Analysis project, different models and algorithms of Machine Learning are used to assess data and assist with planning for loan programs in Fast lending which is a peer to peer lending services organization. Applying a variety of machine learning tools, we are looking for the best practice to provide the most accurate and correct results in terms of eligibility of the candidates. Our focus in this project, has been specifically on *supervised learning* Classification model. Using the models created by the algorithms, the patterns are built which can help us to make predictions on new data.

##**Results**
For all the *supervised learning* methods we used during this project, we followed through three basic steps for each method:
* A machine learning model and a dataset were selected
* Depending on the model, part/all of the data is analyzed by the model to find and build a pattern
* The model then can make predictions on new data using the patterns.

Here is brief description of the main three terms we have considered during this analysis:
- *Accuracy* score shows how well the model has predicted comparing the tested data with the pattern’s result.
- *Precision* tells us what percentage of True cases are actually true.
- *Sensitivity/recall* tells us what percentage of the True cases have truly and correctly been predicted.

1. Naive Random Oversampling
	- Accuracy: %65; 
	- High-Risk: 
		a. Precision: 0.01;
		b. Recall: 0.70
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.60

![imbal_classif_report_random_oversamp.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/imbal_classif_report_random_oversamp.png)

2. SMOTE Oversampling
	- Accuracy: %66; 
	- High-Risk:
		a. Precision: 0.01;
		b. Recall: 0.63
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.69

![imbal_classif_report_smote.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/imbal_classif_report_smote.png)

3. Cluster Centroid Undersampling
	- Accuracy: %54; 
	- High-Risk: 
		a. Precision: 0.01;
		b. Recall: 0.69
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.40

![imbal_classif_report_under_samp.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/imbal_classif_report_under_samp.png)

4. Combination Sampling With SMOTEENN
	- Accuracy: %64; 
	- High-Risk:
		a. Precision: 0.01;
		b. Recall: 0.72
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.57

![imbal_classif_report_smoteenn.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/imbal_classif_report_smoteenn.png)

5. Balanced Random Forest Classifier
	- Accuracy: %87; 
	- High-Risk: 
		a. Precision: 0.03;
		b. Recall: 0.70
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.87

![balanced_random_forest_classifier.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/balanced_random_forest_classifier.png)

6. Easy Ensemble AdaBoost Classifier
	- Accuracy: %94; 
	- High-Risk: 
		a. Precision: 0.09;
		b. Recall: 0.92
	- Low-Risk:
		a. Precision: 1.00;
		b. Recall: 0.94

![easy_ensemble_report.png](https://github.com/zkt2018/Credit_Risk_Analysis/blob/main/resources/easy_ensemble_report.png)

Among all methods and models we have used through this project, although the accuracy score is over %60 for 5 out of the models, the percentage of predicting the high risk applications is very low among all the six models.
The accuracy score has been the least when creating the pattern using the *Cluster Centroid Undersampling* which is pretty similar to *synthetic minority oversampling technique (SMOTE)* model. This model is an underampling approach to decrease the majority group instances. This algorithm generates synthetic data points (centroids) selected among the majority class clusters. Then, it undersamples the majority class down to the size of the samples from the minority class.
 
##**Summary**
Comparing all the six models together, it seems *Easy Ensemble AdaBoost Classifier* has given the highest accuracy, precision and recall percentages in both high-risk and low risk categories. And, even though the precision of the high-risk category is still very low in this model as well as the other ones, we can employ *Easy Ensemble AdaBoost Classifier* and analyse the data based on the recall or sensitivity.
