# Prediction of Drug vs Placebo for Cirrhosis: Research & Recommendations
## Performing Data Analysis on Drug vs Placebo Clinical Trial
##### Jalicia Harris

#### Researched and analyzed data from 10 year (1974-1984) Mayo Clinic trial of patients that participated in a randomized placebo-controlled trial of the drug D-penicillamine.
Business question: What machine learning model could best predict which patients where prescribed D-Penicillamine, a placebo, or did not participate in the trial but provided medical information?
### Data Source:

- Cirrhosis Prediction Dataset: https://drive.google.com/file/d/1-DZ3MeCQwj1mEsejLeIjDmvHEMTZsRoe/view?usp=drive_link

- Original Source: fedesoriano. (August 2021). Cirrhosis Prediction Dataset. Retrieved [Date Retrieved] from https://www.kaggle.com/fedesoriano/cirrhosis-prediction-dataset

 - This dataset contained 418 rows and 20 columns
### Data Description:

A total of 424 PBC patients, referred to Mayo Clinic during that ten-year interval, met eligibility criteria for the randomized placebo-controlled trial of the drug D-penicillamine. The first 312 cases in the dataset participated in the randomized trial and contain largely complete data. The additional 112 cases did not participate in the clinical trial but consented to have basic measurements recorded and to be followed for survival. Six of those cases were lost to follow-up shortly after diagnosis, so the data here are on an additional 106 cases as well as the 312 randomized participants.
###Data Dictionary:

1. ID: unique identifier
2. N_Days: number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986
3. Status: status of the patient C (censored), CL (censored due to liver tx), or D (death)
4. Drug: type of drug D-penicillamine or placebo
5. Age: age in [days]
6. Sex: M (male) or F (female)
7. Ascites: presence of ascites N (No) or Y (Yes)
8. Hepatomegaly: presence of hepatomegaly N (No) or Y (Yes)
9. Spiders: presence of spiders N (No) or Y (Yes)
10. Edema: presence of edema N (no edema and no diuretic therapy for edema), S (edema present without diuretics, or edema resolved by diuretics), or Y (edema despite diuretic therapy)
11. Bilirubin: serum bilirubin in [mg/dl]
12. Cholesterol: serum cholesterol in [mg/dl]
13. Albumin: albumin in [gm/dl]
14. Copper: urine copper in [ug/day]
15. Alk_Phos: alkaline phosphatase in [U/liter]
16. SGOT: SGOT in [U/ml]
17. Triglycerides: triglicerides in [mg/dl]
18. Platelets: platelets per cubic [ml/1000]
19. Prothrombin: prothrombin time in seconds [s]
20. Stage: histologic stage of disease (1, 2, 3, or 4)
## Analytical Insights from Data Analysis
![image](https://github.com/Jalicia-Harris/Drug-vs-Placebo-for-Cirrhosis/assets/128429809/66c8b595-3dae-4c58-ba72-a0016c5d5d5f)
- The histogram above displays the distribution of the number of days between registration and the earlier of death, transplanation, or study analysis time July 1986. The most amount of patients (over 25) remained in the trial for roughly 1050 days.

![image](https://github.com/Jalicia-Harris/Drug-vs-Placebo-for-Cirrhosis/assets/128429809/85edb27c-b126-47f4-84d7-b5fcdc910d0f)

- The bar graph above shows the sex of the patients that were prescribed the drug or a placebo based off the number of days patients remained in the trial. Male patients who were given a placebo remained in the program the longest on average but also have the highest range of days participated.
## Best Production Machine Learning Model:
- The chosen model for making predictions was the KNN Model tuned with the best hyperparameters and estimators using GridSearchCV.
-  Although the overall test score drop by 3%, this still produces the highest metrics from all the other tested and tuned models.

Using this model to make predictions would be fairly reliable in predicting if patients were given D-Penicillamine or didn't participate it the trial but not so well or being given a placebo.

![image](https://github.com/Jalicia-Harris/Drug-vs-Placebo-for-Cirrhosis/assets/128429809/e3d8d367-0327-4ac4-b193-2eac9ea277dc)

###Train
                  precision    recall  f1-score   support


        Placebo       0.70      0.44      0.54       116

       accuracy                           0.72       313
      macro avg       0.77      0.76      0.75       313

###Test
                  precision    recall  f1-score   support


        Placebo       0.63      0.32      0.42        38

       accuracy                           0.69       105
      macro avg       0.70      0.70      0.67       105


## Recommendations

- Based on the extensive analysis of the data, patients who didn't take part in the trial should be removed or replaced with participants as not to possibly skew the test results.
- Test results including vitals, overall health, etc., after the trial was completed could be added to the dataset for better prediction making.
### For Further Information

##### For any additional questions, please contact:
- Jalicia Harris(Data Science Student)
- jaliciadharris@gmail.com
