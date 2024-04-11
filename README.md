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
  <img width="500" height="300" src="https://github.com/Boat2356/Exploratory-Data-Analysis-and-Heart-Disease-Prediction-Using-Machine-Learning/assets/140761543/d27c59e7-c1a2-4ed5-a3e0-230d548dcb26">
</p>



From above, the graph shows the relationship between the frequency of heart disease at different ages, with the x-axis being the age range and the y-axis being the frequency of people with and without heart disease, respectively.

In conclusion, the majority of people without heart disease are aged 65–69, followed by    60–64, and most people with heart disease are 80+, followed by 70–74.

