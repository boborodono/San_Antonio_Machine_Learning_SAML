![SAML](Wilder/PowerPoint/Logos/SAML%20(Banner%20(Landscape)).svg)
# Machine Learning for Predicting Strokes
<!-- Badges -->
![GitHub contributors](https://img.shields.io/github/contributors/boborodono/San_Antonio_Machine_Learning_SAML?color=3e92cc&label=Contributors&style=plastic) ![GitHub commits since latest release (by date including pre-releases)](https://img.shields.io/github/commits-since/boborodono/San_Antonio_Machine_Learning_SAML/v1.0.0/main?include_prereleases&label=Total%20Commits&style=plastic) ![GitHub last commit](https://img.shields.io/github/last-commit/boborodono/San_Antonio_Machine_Learning_SAML?label=Last%20Commit&style=plastic) ![GitHub repo size](https://img.shields.io/github/repo-size/boborodono/San_Antonio_Machine_Learning_SAML?color=ff3b3b&label=Repo%20Size&style=plastic) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/boborodono/San_Antonio_Machine_Learning_SAML?color=orange&label=Code%20Size&style=plastic)  ![GitHub top language](https://img.shields.io/github/languages/top/boborodono/San_Antonio_Machine_Learning_SAML?color=F37626&label=Jupyter%20Notebook&style=plastic)
<!-- ![Lines of Code](https://img.shields.io/tokei/lines/github/boborodono/San_Antonio_Machine_Learning_SAML?color=dark%20green&label=Lines%20of%20Code&style=plastic) -->
![GitHub followers](https://img.shields.io/github/followers/boborodono?label=Followers&style=plastic)
![GitHub watchers](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=ffffff&label=Watch&logo=github&style=social)


## Presentation

[SAML Presentation]("https://github.com/boborodono/San_Antonio_Machine_Learning_SAML/blob/main/Wilder/PowerPoint/SAML_Stroke_Presentation.pdf")<br/>


![Powerpoint](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=B7472A&label=Powerpoint&logo=microsoftpowerpoint&style=plastic)
<br/>



## Topic

### Why Choose This Topic?
This topic is dear to many of our team members. Some of us were personally affected by loved ones having a stroke or actively work in the healthcare industry. Additionally, strokes are on the rise in younger people, and are therefore affecting a larger portion of the population.
We are passionate about improving diagnosis options to prevent strokes. Having predictability may encourage preventative care or medication to reduce stroke risk.
<br></br>


### Questions We Want to Answer...
The goal of this project is to use patient data to train machine learning models.
**We hope to answer:**
1. How successfully can our model be used to predict stroke risk?
2. Which aspect is more accurate to predict risk: medical or personal data?
3. Can we link stroke risk to any specific factor using our machine learning model?

## Data Source
The [source data](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset) includes 5110 observations with 11 attributes. These attributes include medical and personal aspects of the patient such as age, average glucose level, BMI, marital status, and if the patient lives in a rural or urban area.


The dataset was submitted to Kaggle by user [fedesoriano](https://www.kaggle.com/fedesoriano). It is listed as a confidential datasource, but appears to be a cleaned subset of the Electronic Health Record (EHR) controlled by McKinsey & Company; originally used as part of their [Healthcare Hackathon](https://datahack.analyticsvidhya.com/contest/mckinsey-analytics-online-hackathon).

#### **🛠:** ![Kaggle](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=20BEFF&label=Kaggle&logo=kaggle&style=plastic)

<br/>

## Project Outline
![Outline](https://user-images.githubusercontent.com/91762315/158919235-8a4f7e26-c8f1-4b3e-92c1-d9233f8d6670.png)

#### **🛠:** ![Powerpoint](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=B7472A&label=Powerpoint&logo=microsoftpowerpoint&style=plastic)
<br/>

## Data Exploration & Preprocessing
To explore the data we did a general overview using pivot tables to identify any inconsistencies or odd data patterns. In doing so, we found the following:



#### Age 📃 [(Datasets)](/Resources/Age_Datasets)

We identified that the dataset includes information on children. After discussion, we decided to create age sets of 20 years for the model to run through. We believe that the youngest dataset will not have the same aspects as adults; marriage, smoking, and work type will not apply as frequently for patients under 20.



#### BMI 📃 [(Datasets)](/Resources/BMI_Datasets)
We identified that we have a large percentage of NaNs for BMI data. At first we decided to exclude these patients from our dataset. However, we determined that this data was still valuable based on the following:
- Out of 201 NaNs, 40 had a stroke. That's 20% of the deleted data.
- Without the NaNs, there are ~200 positive stroke cases, about 4% of the dataset (200/5000)
- With the NaNs, the positivity rate for all the other categories increases 1%, from 4 to ~5% (250/5000)
- This gives us significantly more data points to help train the model.



#### Glucose 📃 [(Datasets)](/Resources/Glucose_Datasets)
We chose to separate the data based on glucose levels as well. This included breaking out three groups; normal, prediabetic, and diabetic.

#### **🛠:** ![Jupyter](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F37626&label=Jupyter%20Notebook&logo=jupyter&style=plastic) ![Visual Studio Code](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=007ACC&label=VS%20Code&logo=visualstudiocode&style=plastic) ![Pandas](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=150458&label=Pandas&logo=pandas&style=plastic)
<br/>

## ERD
<img width="750" alt = "image" src="https://user-images.githubusercontent.com/46633669/159843815-3ba834eb-1571-480d-99c8-b2f9a88b496a.svg">

#### **🛠:** ![PostgreSQL](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=4169E1&label=PostgreSQL&logo=postgresql&style=plastic)
<br/>

## Feature Engineering and Selection

### Feature Selection
"ID#", a column listing unique identifier values to each sample, is dropped from the feature data in the ML model as it an arbitrary value lacking relationship with other features or target. So far, all other available data features are used in the ML model to predict target stroke cases. A further exploration of ML overfitting will be conducted to determine if any noisy features should be dropped from the ML model.

### Categorical Data
sklearn's OneHotEncoder is used to convert categorical data into numerical data. Categorical data such as "Gender" that contains only two values is split into two converse numerical columns where one of the two is dropped in order to mitigate redundancy in the ML model.

### Null Data
As discussed above, the BMI feature data consists 201 null values. Since a chunk of our positive stroke cases is contained in these 201 samples, we've decided to populate these null values rather than drop the rows entirely. So far, two methods of populating BMI null values have been attempted: sklearn's SimpleImputer replaces null BMI values with median BMI values and sklearn's KNNImputer predicts and populates null BMI values.

### Feature Scaling
sklearn's StandardScaler is used to scale feature data. Prior to scaling, most numerical data features contain only two unique values 0 and 1 as converted by sklearn's OneHotEncoder. Scaling is used to mitigate any ML model issues due to poor gradient descent.

### Resampling
As discussed above, our dataset contains mostly negative stroke cases. Possibly due to using overwhelmingly negative stroke case data, ML model prediction prior to resampling showed positive stroke case recall as poor as 0%. A SMOTE oversampling method has been utilized in ML models resulting in positive stroke case recall as high as 48%.

### Training and Testing

Training & testing data is split using sklearn's train_test_split. Our ML dataset contains 5109 samples with 80% allocated to training and 20% to testing; 4087 training samples and 1022 testing samples. There are 17 features in our X set against 1 target in our y set.

### Model Choice

Currently, sklearn's AdaBoostClassifier supervised ML model returns the greatest positive stroke case recall. 48% positive stroke case recall is achieved with an AdaBoostClassifier and the above Feature Engineering and Selection techniques above (both KNNImputer and SimpleImputer techniques have achieved 48% positive stroke case recall).
* Figure below gives 03/20/2022 AdaBoostClassifier ML model result using SMOTE oversampling and KNNImputer population of missing BMI data

![](Corcoran/ML_result_screenshots/AdaBoost_SMOTE_KNNImputer_03.20.2022.png)

#### **🛠:** ![Python](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=3776AB&label=Python&logo=python&style=plastic) ![Jupyter](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F37626&label=Jupyter%20Notebook&logo=jupyter&style=plastic) ![Visual Studio Code](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=007ACC&label=VS%20Code&logo=visualstudiocode&style=plastic) ![Pandas](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=150458&label=Pandas&logo=pandas&style=plastic) ![Scikit-Learn](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F7931E&label=Scikit-Learn&logo=scikitlearn&style=plastic)

<br/>

## Data Analysis

During early analysis we identified the following:
- In general, women have a higher stroke risk.
- Age is heavily related to stroke risk. The higher the age, the higher the risk. However, after retirement age, women have a much higher risk than men.
- Men have heart attacks more often than strokes. There is an increase in chance of cardiac episode once the patient has had a stroke.
- More of the women in our dataset have a higher instance of hypertension.
- Even though they had a higher instance of stroke cases, we see that women smoke less overall.
- We do not see a preliminary relationship between marriage status or home location as related to stroke and gender#.

#### **🛠:** ![Python](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=3776AB&label=Python&logo=python&style=plastic) ![Pandas](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=150458&label=Pandas&logo=pandas&style=plastic) ![Jupyter](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F37626&label=Jupyter%20Notebook&logo=jupyter&style=plastic) ![Visual Studio Code](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=007ACC&label=VS%20Code&logo=visualstudiocode&style=plastic) ![Scikit-Learn](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F7931E&label=Scikit-Learn&logo=scikitlearn&style=plastic)
<br/>


## Dashboard

### Technologies:

<img width="1123" alt="image" src="https://user-images.githubusercontent.com/85581208/159751965-51b9829d-a43f-41d2-a39a-9484d8a8b1c4.png">

#### **🛠:** ![Powerpoint](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=B7472A&label=Powerpoint&logo=microsoftpowerpoint&style=plastic)

### Dashboard Storyboard:

<img width="1123" alt="image" src="https://user-images.githubusercontent.com/46633669/159814732-7a407669-d7f6-4e67-b8a6-aefe8244c710.png">

#### **🛠:** ![Powerpoint](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=B7472A&label=Powerpoint&logo=microsoftpowerpoint&style=plastic) ![Tableau](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=E97627&label=Tableau&logo=tableau&style=plastic)
<br/>

### Interactive elements:
The dashboard will include filters to allow the user to separate the data based on gender and incidence of stroke.

#### **🛠:**
<br/>

## Communication Protocols

**Contact goals:**
- A minimum of twice weekly conversations through Slack
- Meeting at 6:30PM CT before class on Tuesdays and Thursdays
- Tracking deliverables through the Project Management spreadsheet


**The following will occur on an as-needed basis:**
- Video chat through Google Meet
- Feedback through GitHub pull requests

#### **🛠:** ![Slack](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=4A154B&label=Slack&logo=slack&style=plastic) ![Zoom](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=2D8CFF&label=Zoom&logo=zoom&style=plastic) ![Google Drive](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=4285F4&label=Google%20Drive&logo=googledrive&style=plastic) ![Github](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F05032&label=Github&logo=github&style=plastic)
<br/>

## Authors 👯‍♀️

| Name | My Repo     |  LinkedIn                |
| :-------- | :------- | :------------------------- |
| Jack Bauer | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/jackary24)|[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jack-bauer-/) |
| Kelsey Corcoran | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/stereo-chemistry)      | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kelsey-corcoran-59b6831b6/)|
| Katie Hopkins | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/HopkinsKV)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/hopkinskv/)                |
| Angela Pacatte | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/angepacatte)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/angela-barker-pacatte/)                |
| Bowen Wilder | [![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://github.com/boborodono)     | [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bowenwilder/)                |

<br/><br/>

#### **🛠:** ![Anaconda](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=f3f3f3f&label=Anaconda&logo=anaconda&style=plastic) ![Git](https://img.shields.io/github/watchers/boborodono/San_Antonio_Machine_Learning_SAML?color=F05032&label=Git&logo=git&style=plastic)
