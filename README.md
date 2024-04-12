# Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning
## The origin and significance
Cardiovascular disease is the world's leading cause of death. According to statistics from the World Health Organization (WHO), the number of deaths due to cardiovascular disease accounts for 31 percent of all worldwide deaths. For Thailand, statistics by the Ministry of Health show that the risk of death from cardio is rising every year. The cause of cardiovascular disease is caused by a few factors, such as age, sex, behavior, and health behaviors such as smoking, alcohol consumption, unhealthy eating, overweight or obesity, high blood pressure, and high blood cholesterol levels.

Today, cardiovascular diagnosis can be done in a variety of ways, such as an electrocardiogram (ECG), CT, or echocardiogram. However, these methods are not very accurate, so there is machine learning that can use data analysis and learning from data to build models that can predict future outcomes. Machine learning can be applied to many problems, including diagnostic problems.

Based on the above data, the researchers were interested in exploratory data analysis to look at the trends and relationships of each variable and then using machine learning to help predict cardiovascular disease by testing the performance of the models using methods such as the confusion matrix and the AUC-ROC curve, then performing hyperparameter tuning to improve the model performance.

## Objectives
- To analyze cardiovascular information using Exploratory data analysis. (EDA)
- To predict cardiovascular disease by creating a Machine Learning Model using Logistic Regression, Decision Tree, and Random Forest methods and measuring the performance of all three models.

## The scope of the project
- The data used to analyze data by EDA and predict heart disease using Machine Learning is obtained from https://www.kaggle.com/datasets/alphiree/cardiovascular-diseases-risk-prediction-dataset
- The source of this dataset is from the Non-Contact Disease Risk and Injury Behavior Survey (BRFSS), conducted by the Centers for Disease Control and Prevention (CDC) in the United States, which collects data from surveys of US residents on health risk behavior and use of health services.
- The data set has a total of 308855 rows, 19 columns.
- The objective of this project is to study the relationship information of each variable from the EDA and create a machine learning model for all three methods of cardiovascular prediction Logistic Regression, Decision Tree, and Random Forest, with tools to measure the performance of prediction, including Confusion Matrix, Validation Curve, and Learning Curve.
- The variable studied to predict is cardiovascular disease.

## Workflow
### Modeling process

<p align="center">
  <img width="700" height="600" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/63521c34-d937-4b91-96d1-65b1e8ebe218">
</p>

### Data collection
The dataset of this work comes from the Non-Communicable Disease and Injury Risk Behaviors Survey (BRFSS) project run by the Centers for Disease Control and Prevention (CDC) in the United States, which collects data from surveys of U.S. residents on health risk behaviors and the use of health services. The Dataset consists of 308855 rows and 19 columns.

| ตัวแปร (Variables)  | คำอธิบาย (Definition) | ประเภทของข้อมูล (Data Types) |
|     :---:     |     :---:     |     :---:     |
|General Health	|ระดับสุขภาพโดยทั่วไป|	Ordinal |
|Checkup|	ช่วงเวลาครั้งล่าสุดที่ตรวจสุขภาพ|	Ordinal|
|Age (Category)|	ช่วงอายุ|	Nominal|
|Sex|	เพศ|	Nominal|
|Exercise	|ออกกําลังกายหรือไม่|	Nominal|
|Heart Disease|	เป็นโรคเกี่ยวกับหัวใจและหลอดหรือไม่|	Nominal|
|Skin Cancer|	เป็นโรคมะเร็งผิวหนังหรือไม่|	Nominal|
|Other Cancer|	เป็นโรคอื่นๆที่เกี่ยวข้องกับมะเร็งหรือไม่|	Nominal|
|Depression|	เป็นโรคซึมเศร้าหรือไม่|	Nominal|
|Diabetes|	เป็นโรคเบาหวานหรือไม่|	Nominal|
|Arthritis|	เป็นโรคข้อเสื่อมหรือไม่|	Nominal|
|Smoking History|	มีประวัติการสูบบุหรี่หรือไม่|	Nominal|
|Height|	ส่วนสูง|	Continuous|
|Weight|	น้ำหนัก|	Continuous|
|BMI|	ดัชนีมวลกาย	|Continuous|
|Alcohol consumption|	ปริมาณการดื่มแอลกอฮอล์ (g) / เดือน|	Continuous|
|Fruit consumption|	ปริมาณการกินผลไม้ (g) / เดือน|	Continuous|
|Green vegetable consumption|	ปริมาณการกินผักใบเขียว (g) / เดือน|	Continuous|
|Fried potato consumption|	ปริมาณการกินมันฝรั่งทอด (g) / เดือน|	Continuous|

### Data Exploration (Exploratory Data Analysis: EDA)
- An example of finding Missing Values.

<p align="center">
  <img width="350" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/ea2c0827-7473-4d9d-b7a0-a2240bc000db">
</p>

From above, there are no missing values, so we will move on to the next step.

- An example of plotting a graph to find the relationship of variables and trends of data.

<p align="center">
  <img width="600" height="350" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/929a1140-e34e-4af6-b595-a0781c8c3a70">
</p>

From above, the graph shows the relationship between the frequency of heart disease at different ages, with the x-axis being the age range and the y-axis being the frequency of people with and without heart disease, respectively.

In conclusion, the majority of people without heart disease are aged 65–69, followed by    60–64, and most people with heart disease are 80+, followed by 70–74.

### Data Preparation
<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/7783aae2-0e84-4eb9-9567-95c1ec9f63c0">
</p>

From the image, there are 2 variables with ordinal scale data type
- General Health level (General_Health), which is sorted as follows: Poor, Fair, Good, Very Good, and Excellent.
- The last time you went to a health check (Checkup), which is sorted below: Within the past year, Within the past 2 years, Within the past 5 years, 5 years ago, and Never.

<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/6b39e3eb-3e45-4da3-bfc6-49f5e70384d1">
</p>

From the image, there are 8 variables with nominal scale data type, which are unsorted data, such as gender, only male and female. Exercise will only be exercised (1.0) and non-workout (0.0) and use One-Hot Encoder to convert data into quantitative data.

<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/511e6f14-b3e2-49c9-adde-d886bf6f0ad0">
</p>

From the image, the map function will be used to change the data of age, the original form is nominal in the form of quantitative data using the average between the age range, for example, the age range 18-24 will convert to (18+24)/2 = 22 and the diabetes is changed to the form of Binary (0 and 1).

### Algorithms of predictive modeling
In this step, I will give an example of using a Logistic Regression algorithm to train a model and evaluate the results using the method Classification Report, Confusion Matrix, AUC-ROC Curve, Validation Curve, and Learning Curve.

- Logistic Regression

<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/14c080e5-a59d-4b67-943f-3e8f7d17d3c9">
</p>

Split train data and test data. Then use StandardScaler with train data to adjust the quantitative data to a normal distribution format. Then use SMOTE oversampling with the train data set to divide the data for each class in training equally. The principle of oversampling is to randomly increase the number of minority data to be equal to the main group (Major class) and then use the function. LogisticRegression to fit the model.

- Classification Report on testing data

<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/848601c8-8474-4a77-8de1-fa5ffc99a5e4">
</p>

- Accuracy: The model has a pretty good overall predictive performance.
- Precision: The model is quite accurate in predicting cases where people do not have heart disease. But there is accuracy in Predict in cases where people have poor heart disease.
- Recall: The model can detect people who have and don't have heart disease.
- F1-Score: The model is balanced between Precision and Recall in Class 0, but has imbalances in Class 1.

### Confusion Matric and AUC-ROC Curve
<p align="center">
  <img width="600" height="350" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/97296218-dab0-44f6-8acb-90d00d1789e7">
</p>

- True Negative (TN): The model predicted that it is not a heart disease, which the real result is not a heart disease, by predicting 63096 people
- False Negative (FN): The model predicted that it is not a heart disease, which the real result is a heart disease by predicted 1856 people
- False Positive (FP): The model predicted a heart disease, which the real result is not a heart disease by predicting 22070 people
- True Positive (TP): Model predicted as heart disease, which results are heart disease, by predicted 5635 people
- The AUC-ROC Curve measures the proportions of Sensitivity (Recall) and (1-Specificity), where the Specificity is available from TN / (TN + FP), which from the image has an AUC of 82.21%, which shows that the model has a good overall performance.

### Validation Curve and Learning Curve
<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/a1091ff7-adfe-43a0-8035-2b8bcd4104af">
</p>

- From the validation curve graph, the x-axis is the C value (inverse of regularization strength). If the C value is large, it will make the model less complicated. And if the C value
Less will make the model very complicated and the Y axis is Score.
- From learning curve graph, the x-axis is the amount of training data used, and the y-axis is the accuracy value, which shows that the best range is the entire graph two will converge.

### Hyperparameter Tuning
In this step, I use GridSearchCV to find the best set of parameters for Logistic Regression model and train it on the training dataset.
<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/1db735ae-6b79-4166-bbf1-0a2e5a70a7a8">
</p>

- Results of Classification report and Confusion Matrix after Hyperparameter Tuning.
<p align="center">
  <img width="400" height="400" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/d7ac78d9-3197-4a1e-9a3a-91c61190d3ce">
</p>

- Results of AUC-ROC Curve after Hyperparameter Tuning
<p align="center">
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/0492dc9b-ec35-426e-83d1-d4682b0965f0">
</p>

## Conclusion
The study focuses on data analysis using Exploratory data analysis (EDA) and predicting heart disease using machine learning methods, addressing bias in training data due to unbalanced instances. The model uses Logistic Regression, Decision Tree, and Random Forest algorithms, with resampling techniques like SMOTE. The experiment results show that the Logistic Regression model has the highest accuracy of 74% and the highest area under the ROC curve value of 0.84. After Hyperparameter Tuning, the model is the most efficient, with an overall accuracy of 74% and the highest area under the ROC curve value of 0.82.

## Recommendation
- In this project, only one sampling technique (resampling techniques) is used, namely oversampling with SMOTE, to adjust the balance of the training data of the learning model to deal with the problem of data asymmetry. Therefore, there may be a need for other data balancing techniques to train learning models that can learn data and predict values with better accuracy and efficiency than this project, such as the undersampling technique.
- The scope of primary variables used to predict heart disease is quite wide. Therefore, when it is used, it may not be accurate enough. Therefore, it is necessary to add initial variables that help make the prediction more narrow, such as blood pressure, heart rate, blood cholesterol levels, etc.
- Researchers may add algorithms to evaluate the results. To get a variety of results and be able to expand further, such as the XGBoost algorithm or CatBoost Classifier, etc.

