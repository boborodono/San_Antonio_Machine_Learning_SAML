![SAML](Wilder/PowerPoint/Logos/SAML%20(Banner%20(Landscape)).svg)
<h1 align="center">Predicting Strokes with Machine Learning</h1>

<!-- Badges -->
<p align="center">
   <a href=""><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/boborodono/San_Antonio_Machine_Learning_SAML?color=3e92cc&label=Contributors&style=plastic"/>
   </a>
   <a href=""><img alt="GitHub commits since latest release (by date including pre-releases)" src="https://img.shields.io/github/commits-since/boborodono/San_Antonio_Machine_Learning_SAML/v1.0.0/main?include_prereleases&label=Total%20Commits&style=plastic"/>
   </a>
   <a href=""><img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/boborodono/San_Antonio_Machine_Learning_SAML?label=Last%20Commit&style=plastic"/>
   </a>
   <a href=""><img alt="GitHub Repo Size" src="https://img.shields.io/github/repo-size/boborodono/San_Antonio_Machine_Learning_SAML?color=ff3b3b&label=Repo%20Size&style=plastic"/>
   </a>
   <a href=""><img alt="Github Code Size in Bytes" src="https://img.shields.io/github/languages/code-size/boborodono/San_Antonio_Machine_Learning_SAML?color=orange&label=Code%20Size&style=plastic"/>
   </a>
   <a href=""><img alt="GitHub Top Language" src="https://img.shields.io/github/languages/top/boborodono/San_Antonio_Machine_Learning_SAML?color=F37626&label=Jupyter%20Notebook&style=plastic"/>
   </a>
   <a href=""><img alt="Github Followers" src="https://img.shields.io/github/followers/boborodono?label=Followers&style=plastic"/>
                                                                                                                                </a>
   <a href=""><img alt="Github Watchers" src="https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=ffffff&label=Watch&logo=github&style=social"/>
   </a>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Table of Contents

- [Presentation & Dashboard](#presentation--dashboard)
- [Topic](#topic)
  * [Why Would We Want to Predict Strokes?](#why-would-we-want-to-predict-strokes)
  * [Questions We Want to Answer...](#questions-we-want-to-answer)
- [Data Source](#data-source)
- [Project Outline](#project-outline)
- [Data Exploration & Preprocessing](#data-exploration--preprocessing)
- [ERD](#erd)
- [Feature Engineering and Selection](#feature-engineering-and-selection)
  * [Feature Selection](#feature-selection)
  * [Categorical Data](#categorical-data)
  * [Null Data](#null-data)
  * [Feature Scaling](#feature-scaling)
  * [Resampling](#resampling)
  * [Training and Testing](#training-and-testing)
  * [Model Choice](#model-choice) 
- [Data Analysis](#data-analysis)
- [Communication Protocols](#communication-protocols)
- [Authors](#authors)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Tech Stack
<!-- Badges -->
<p align="center">  
   
   <a href="">![Mac OS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)</a>
   <a href="">![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)</a>
   <a href="">![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)</a>
   <a href="">![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)</a>
   <a href="">![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)</a>
   <a href="">![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)</a>
   <a href="">![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)</a>
   <a href="">![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)</a>
   <a href="">![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)</a>
   <a href="">![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)</a>
   <a href="">![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)</a>
   <a href="">![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)</a>
   <a href="">![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)</a>
   <a href="">![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)</a>
   <a href="">![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)</a>
   <a href="">![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)</a>
   <a href="">![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)</a>
   <a href="">![Microsoft PowerPoint](https://img.shields.io/badge/Microsoft_PowerPoint-B7472A?style=for-the-badge&logo=microsoft-powerpoint&logoColor=white)</a>
   <a href="">![Tableau](https://img.shields.io/badge/Tableau-%E97627CC.svg?&logo=tableau&color=e97627&logoColor=white&style=for-the-badge)
   <a href="">![Slack](https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white)</a>
   <a href="">![Zoom](https://img.shields.io/badge/Zoom-2D8CFF?style=for-the-badge&logo=zoom&logoColor=white)</a>
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Presentation & Dashboard

[SAML Presentation(Github)](/Wilder/PowerPoint/SAML_Stroke_Presentation.pdf) - [(Github Pages)](https://boborodono.github.io/SAML_PDF/SAML_Stroke_Presentation.pdf)<br/>

[SAML Dashboard(Tableau Public)](https://public.tableau.com/app/profile/katie.hopkins/viz/SAML-StrokeData/MedicalDashboard)<br/>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
 
# Topic

## Why Would We Want to Predict Strokes?
This topic is dear to many of our team members. Some of us were personally affected by loved ones having a stroke or actively work in the healthcare industry. Additionally, strokes are on the rise in younger people, and are therefore affecting a larger portion of the population.
We are passionate about improving diagnosis options to prevent strokes. Having predictability may encourage preventative care or medication to reduce stroke risk.

<hr>

## Questions We Want to Answer...
The goal of this project is to create a predictive analysis from stroke patient data using machine learning.
**We hope to answer:**
1. How successfully can our model be used to predict stroke risk?
2. Which aspect is more accurate to predict risk: medical or personal data?
3. Can we link stroke risk to any specific factor using our machine learning model?

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Data Source
The [source data](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset) includes 5110 observations with 11 attributes. These attributes include medical and personal aspects of the patient such as age, average glucose level, BMI, marital status, and if the patient lives in a rural or urban area.

The dataset was submitted to Kaggle by user [fedesoriano](https://www.kaggle.com/fedesoriano). It is listed as a confidential datasource, but appears to be a cleaned subset of the Electronic Health Record (EHR) controlled by McKinsey & Company; originally used as part of their [Healthcare Hackathon](https://datahack.analyticsvidhya.com/contest/mckinsey-analytics-online-hackathon).

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Project Outline
![Outline](https://user-images.githubusercontent.com/91762315/158919235-8a4f7e26-c8f1-4b3e-92c1-d9233f8d6670.png)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Data Exploration & Preprocessing
To explore the data we did a general overview using pivot tables to identify any inconsistencies or odd data patterns. In doing so, we found the following:

### Age 📃 [(Datasets)](/Resources/Age_Datasets)

We identified that the dataset includes information on children. After discussion, we decided to create age sets of 20 years for the model to run through. We believe that the youngest dataset will not have the same aspects as adults; marriage, smoking, and work type will not apply as frequently for patients under 20.
- The dataset was split into generational bins for further analysis

| Generation | Age Range | 
| :-------- | :------- |
| Gen Z | 0 - 20 | 
| Millenial | 20 - 40 | 
| Gen X | 40 - 60 | 
| Boomer | 60 - 80 | 
| Greatest Gen | 80 - 100 | 

<hr>

### BMI 📃 [(Datasets)](/Resources/BMI_Datasets)
- The dataset was split into BMI Class bins for further analysis

| BMI Class | BMI Range | 
| :-------- | :------- |
| Underweight | 0 - 18.5 | 
| Healthy Weight | 18.5 - 25 | 
| Overweight | 25 - 30 | 
| Obese(Low-Risk) | 30 - 35 | 
| Obese(Medium-Risk) | 35 - 40 |
| Obese(High-Risk) | 40 - 100 |

We identified that we have a large percentage of NaNs for BMI data. At first we decided to exclude these patients from our dataset. However, we determined that this data was still valuable based on the following:
- Out of 201 NaNs, 40 had a stroke. That's 20% of the deleted data.
- Without the NaNs, there are ~200 positive stroke cases, about 4% of the dataset (200/5000)
- With the NaNs, the positivity rate for all the other categories increases 1%, from 4 to ~5% (250/5000)
- This gives us significantly more data points to help train the model.

<hr>

### Glucose 📃 [(Datasets)](/Resources/Glucose_Datasets)
We chose to separate the data based on glucose levels as well. This included breaking out three groups; normal, prediabetic, and diabetic.
- The dataset was split Glucose Level Class bins for further analysis

| Glucose Level Class | Glucose Range | 
| :-------- | :------- |
| Normal | 0 - 100 | 
| Prediabetic | 100 - 125 | 
| Diabetic | >125 |

<hr>

### Categorical Metrics

|Personal Criteria | Medical Criteria |
|--|--|
|<table> <tr><th>Personal Category</th><th>Criteria</th></tr><tr><td>Ever Married</td><td>Yes</td></tr><tr><td></td><td>No</td></tr><tr><td>Work Type</td><td>Private</td></tr><tr><td></td><td>Self-Employed</td></tr><tr><td></td><td>Government Job</td></tr><tr><td></td><td>Children</td></tr><tr><td>Residence Type</td><td>Urban Job</td></tr><tr><td></td><td>Rural</td></tr><tr><td>Smoker</td><td>Never</td></tr><tr><td></td><td>Former</td></tr><tr><td></td><td>Current</td></tr><tr><td></td><td>Unknown</td></tr> </table>|<table> <tr><th>Medical Category</th><th>Criteria</th></tr><tr><td>BMI</td><td>0-100</td></tr><tr><td>Glucose</td><td>0-125</td></tr><tr><td>Hypertension</td><td>Yes</td></tr><tr><td></td><td>No</td></tr><tr><td>Heart Disease</td><td>Yes</td></tr><tr><td></td><td>No</td></tr> </table>| 

<hr>

## Initial Dataset EDA
| Stroke Dataset Stats | 
| :----: |
| <img src="https://user-images.githubusercontent.com/46633669/161340184-364dca84-c274-4aae-ab33-1281bd174f2b.png" width="200" height="200"> |
| Sample Size: 5,109 entries |

### Age
Age Histogram  |Age Stacked Bar |
| :----: | :----: |
| <img src="https://user-images.githubusercontent.com/46633669/161337039-6099826a-117c-4002-b269-66afbbe97e05.png" width="300" height="300"> | <img src="https://user-images.githubusercontent.com/46633669/161337083-7a922d01-9188-49f0-a8a2-3bf755ee6e74.png" width="300" height="300"> | 
| There are more possible stroke cases from 0 - 60 years old. However, positive stroke cases are more prevalent with age. | This shows that a higher proportion of positive stroke cases occur as age increases. |

### Gender
| Gender Histogram | Gender Stacked Bar |
|  :----: | :----: |
| <img src="https://user-images.githubusercontent.com/46633669/161338306-cb6b0deb-d357-4837-9c62-c3c53651d39d.png" width="300" height="300"> | <img src="https://user-images.githubusercontent.com/46633669/161337113-64cab7dd-efcb-4693-94de-961ce105f4ce.png" width="300" height="300"> | 
- According to the data, significantly more women were admitted for possible cases of a stroke. 
- The percentage of positive stroke cases is about even between men and women. 
 
 ## Personal Criteria
 
 
 
 
 
 
 #### Medical Criteria
 
 
 
 
 
 Ever Married Stacked Bar | Work Type Stacked Bar | Residence Type Stacked Bar | Smoker Histogram |Smoker Bar Chart | BMI Histogram | BMI Stacked Bar | Glucose Histogram | Glucose Stacked Bar | Hypertension Stacked Bar | Heart Disease Stacked Bar |
| :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- | :------- |
| <figure><img src="https://user-images.githubusercontent.com/46633669/161340184-364dca84-c274-4aae-ab33-1281bd174f2b.png"><figcaption>Sample Size: 5,109 entries</figcaption></figure> |<figure><img src="https://user-images.githubusercontent.com/46633669/161337039-6099826a-117c-4002-b269-66afbbe97e05.png"><figcaption>There are more possible stroke cases from 0 - 60 years old. However, positive stroke cases are more prevalent with age.</figcaption></figure> |
<img src="https://user-images.githubusercontent.com/46633669/161337083-7a922d01-9188-49f0-a8a2-3bf755ee6e74.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161338306-cb6b0deb-d357-4837-9c62-c3c53651d39d.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161337113-64cab7dd-efcb-4693-94de-961ce105f4ce.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161337144-a897cf4c-fa70-4857-bd8c-54496a6c9bfe.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161337167-64497c22-10f6-46e7-add1-282996a11aab.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161337196-5fd8f76b-d974-48db-aa66-659a202fea8a.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161338425-8ee707a1-bbcd-4efc-8694-3ac7a2d6e643.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161344765-fe6ae917-fa6a-4d30-bc74-4e05a3109daf.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161337215-666b14c2-40c2-4b18-9f33-4dc37147eee8.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161337226-fea3db85-228f-4430-82f5-3a5041e08cf9.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161337247-95020749-5298-46cc-a5c3-39f44ff3b82f.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161337262-cb52c482-43ec-4aa5-b16c-275163e36972.png" width="200" height="200"> |
<img src="https://user-images.githubusercontent.com/46633669/161337278-d4ab810d-7d5a-4c75-867c-4b86b9e08594.png" width="200" height="200"> | <img src="https://user-images.githubusercontent.com/46633669/161337287-5239847c-913d-4416-b027-9cea1bd34190.png" width="200" height="200"> |
| Sample Size: 5,109 entries  
| There are more possible stroke cases from 0 - 60 years old. However, positive stroke cases are more prevalent with age.  
| This shows that a higher proportion of positive stroke cases occur as age increases.  
| According to the data, significantly more women were admitted for possible cases of a stroke.  
| The percentage of positive stroke cases is about even between men and women. 
| More instances of stroke were reported among patients that were married at one point in time. 
| "Self-Employed" workers have the highest prevalance of positive stroke cases but not statistically different from patients employed by "Private" or "Govt" organizations. 
| No perceivable difference detected in instances of stroke between those in "Rural" v. "Urban" Residences. 
| Most patients never smoked but many patient's smoking history is "Unknown". 
| Most "Former" and "Current" smokers had a higher prevalence of positive stroke cases but the results were not significant. 
| A majority of patients are "Overweight" or "Obese." 
| "Overweight" or "Obese" patients have a higher prevalence for developing a stroke. 
| Most patients were in the "Normal" Glucose Level range. 
| Patients diagnosed as "Diabetic" had a higher prevalence of stroke cases. 
| Patients diagnosed with Hypertension had a a higher prevalence of stroke cases. 
| Patients diagnosed with Heart Disease had a a higher prevalence of stroke cases. |


### Splitting the Data into Medical and Personal Criteria 

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# ERD
<img width="1123" alt = "image" src="https://user-images.githubusercontent.com/46633669/159843815-3ba834eb-1571-480d-99c8-b2f9a88b496a.svg">

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Feature Engineering and Selection

## Feature Selection
"ID#", a column listing unique identifier values to each sample, is dropped from the feature data in the ML model as it an arbitrary value lacking relationship with other features or target. So far, all other available data features are used in the ML model to predict target stroke cases. A further exploration of ML overfitting will be conducted to determine if any noisy features should be dropped from the ML model.

<hr>

## Categorical Data
sklearn's OneHotEncoder is used to convert categorical data into numerical data. Categorical data such as "Gender" that contains only two values is split into two converse numerical columns where one of the two is dropped in order to mitigate redundancy in the ML model.

<hr>

## Null Data
As discussed above, the BMI feature data consists 201 null values. Since a chunk of our positive stroke cases is contained in these 201 samples, we've decided to populate these null values rather than drop the rows entirely. So far, two methods of populating BMI null values have been attempted: sklearn's SimpleImputer replaces null BMI values with median BMI values and sklearn's KNNImputer predicts and populates null BMI values.

<hr>

## Feature Scaling
sklearn's StandardScaler is used to scale feature data. Prior to scaling, most numerical data features contain only two unique values 0 and 1 as converted by sklearn's OneHotEncoder. Scaling is used to mitigate any ML model issues due to poor gradient descent.

<hr>

## Resampling
As discussed above, our dataset contains mostly negative stroke cases. Possibly due to using overwhelmingly negative stroke case data, ML model prediction prior to resampling showed positive stroke case recall as poor as 0%. A SMOTE oversampling method has been utilized in ML models resulting in positive stroke case recall as high as 48%.

<hr>

## Training and Testing

Training & testing data is split using sklearn's train_test_split. Our ML dataset contains 5109 samples with 80% allocated to training and 20% to testing; 4087 training samples and 1022 testing samples. There are 17 features in our X set against 1 target in our y set.

<hr>

## Model Choice
We started with sklearn's Random Forest Classifier (RFC). These models give the highest overall accuracy, but the poorest positive stroke case recall. After preprocessing, RFC models achieve correctly label 28%-40% of positive strokes using different data preprocessing methods.  

As of now, sklearn's AdaBoostClassifier supervised ML model returns the greatest positive stroke case recall. 48% positive stroke case recall is achieved with an AdaBoostClassifier and the above Feature Engineering and Selection techniques above (both KNNImputer and SimpleImputer techniques have achieved 48% positive stroke case recall). Currently, sklearn's Support Vector Classifier (SVC) has achieved the greatest 92% positive stroke case recall with lower overall accuracy than the AdaBoostClassifier and RandomForestClassifier models.
* Figure below gives 03/20/2022 AdaBoostClassifier ML model result using SMOTE oversampling and KNNImputer population of missing BMI data

![](Corcoran/ML_result_screenshots/AdaBoost_SMOTE_KNNImputer_03.20.2022.png)

* Figure below gives 03/24/2022 SVC ML model result using RandomOverSampler oversampler and SimpleImputer population of missing BMI data with median BMI feature value.

![](Corcoran/ML_result_screenshots/SVC_ros_SimpleImputer(median)_03.24.2024.png)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Data Analysis

During early analysis we identified the following:
- In general, women have a higher stroke risk.
- Age is heavily related to stroke risk. The higher the age, the higher the risk. However, after retirement age, women have a much higher risk than men.
- Men have heart attacks more often than strokes. There is an increase in chance of cardiac episode once the patient has had a stroke.
- More of the women in our dataset have a higher instance of hypertension.
- Even though they had a higher instance of stroke cases, we see that women smoke less overall.
- We do not see a preliminary relationship between marriage status or home location as related to stroke and gender#.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Communication Protocols

**Contact goals:**
- A minimum of twice weekly conversations through Slack
- Meeting at 6:30PM CT before class on Tuesdays and Thursdays
- Tracking deliverables through the <a href="https://docs.google.com/spreadsheets/d/1dhVx7JtsV96xwiIY83Ls-zlMphNlS3TNKQlNlZLgGN4/edit?usp=sharing">![Project Management](https://img.shields.io/badge/Project%20Management-4285F4?style=plastic&logo=googledrive&logoColor=white)</a> spreadsheet

**The following will occur on an as-needed basis:**
- Video chat through Google Meet
- Feedback through GitHub pull requests

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
# Authors
| Author | My Repo     |  LinkedIn                |
| :-------- | :------- | :------------------------- |
| Jack Bauer | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/jackary24)|[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jack-bauer-/) |
| Kelsey Corcoran | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/stereo-chemistry)      | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kelsey-corcoran-59b6831b6/)|
| Katie Hopkins | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HopkinsKV)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hopkinskv/)                |
| Angela Pacatte | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/angepacatte)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/angela-barker-pacatte/)                |
| Bowen Wilder | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/boborodono)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bowenwilder/)                |

 <a href="">![SAML](https://custom-icon-badges.herokuapp.com/badge/custom-badge-white.svg?style=for-the-badge&color=white&logo=saml&label=SAML&logoColor=white)</a>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/fire.png)
