# Using Stroke Data for Machine Learning Predictions

*Note: The descriptions and explanations required in each segment's deliverables will be updated throughout the course of the project.*

## Topic

The goal of this project is to use patient data to train machine learning models.  
**We hope to answer:**
1. How successfully can our model be used to predict stroke risk? 
2. Which aspect is more accurate to predict risk: medical or personal data?
<br></br>

This topic is dear to many of our team members. Some of us were personally affected by loved ones having a stroke or actively work in the healthcare industry. Additionally, strokes are on the rise in younger people, and are therefore affecting a larger portion of the population.  
We are passionate about improving diagnosis options to prevent strokes. Having predictability may encourage preventative care or medication to reduce stroke risk. 


## Data Source
The [source data](https://www.kaggle.com/fedesoriano/stroke-prediction-dataset) includes 5110 observations with 11 attributes. These attributes include medical and person aspects of the patient such as age, average glucose level, BMI, marital status, and if the patient lives in a rural or urban area.


The dataset was submitted to Kaggle by user [fedesoriano](https://www.kaggle.com/fedesoriano). It is listed as a confidential datasource, but appears to be a cleaned subset of the Electronic Health Record (EHR) controlled by McKinsey & Company; originally used as part of their [healthcare hackathon](https://datahack.analyticsvidhya.com/contest/mckinsey-analytics-online-hackathon).

## Project Outline

## Data Exploration & Analysis

### Age
We identified that the dataset includes information on children. After discussion, we decided to create age sets of 20 years for the model to run through. We believe that the youngest dataset will not have the same aspects as adults; marriage, smoking, and work type will not apply as frequently for patients under 20.  

### BMI
We identified that we have a large percentage of NANs for BMI data. At first we decided to exclude these patients from out dataset. However, we determined that this data was still valuable based on the following:
- Out of 201 Nans, 40 had a stroke. That's 20% of the deleted dated
- Without the NANs, there are ~200 positive stroke cases, about 4% of the dataset (200/5000)
- With the NANs, the positivity rate for all the other categories increases 1%, from 4 to ~5% (250/5000)
- This gives us significantly more data points to help train the model.


## Preliminary work

### Data Preprocessing

### Feature Engineering and Selection

### Training and Testing

### Model Choice

## Dashboard

Tools:

Interactive elements:



## Communication Protocols

**Contact goals:**
- A minimum of twice weekly conversations through Slack
- Meeting at 6:30PM CT before class on Tuesdays and Thursdays
- Tracking deliverables through the Project Management spreadsheet


**The following will occur on an as-needed basis:**
- Video chat through Google Meet
- Feedback through GitHub pull requests


### Team Members
[Jack Bauer](https://github.com/jackary24)  
[Kelsey Corcoran](https://github.com/stereo-chemistry)  
[Katie Hopkins](https://github.com/HopkinsKV)  
[Angela Pacatte](https://github.com/angepacatte)  
[Bowen Wilder](https://github.com/boborodono)  


