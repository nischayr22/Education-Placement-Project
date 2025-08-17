# Education-Placement-Project

## Project

For this project, I utilised a Kaggle dataset (sourced in the notebook) that expresses features of Students and whether they have achieved a placement or not. The features that were in the dataset are the following:
1.   College_ID - Unique ID for the college
2.   IQ - IQ score of the student
3.   Prev_Sem_Result - GPA of the previous semester
4.   CGPA	- Cumulative Grade Point Average (range: ~5.0 to 10.0)
5.   Academic_Performance	- Annual academic rating (scale: 1 to 10)
6.   Internship_Experience - Whether the student has completed any internship
7.   Extra_Curricular_Score	Involvement in extracurriculars (score from 0 to 10)
8.   Communication_Skills	- Soft skill rating (scale: 1 to 10)
9.   Projects_Completed	- Number of academic/technical projects completed (0 to 5)
10.  Placement - Final placement result (Yes = Placed, No = Not Placed)

The purpose of this project, was to see what features were most likely to be predictors in whether a student would achieve placement or not. Additionally, in doing this, building a machine learning model to predict whether a student will achieve placement or not. Ultimaley, an accurate model can be used to determine what areas students need to improve on to increase their chances they will achieve placement.

## Notebook

(For a full view of the project access the Education_Project.ipynb)

For this project I followed through a data analysis and machine learning methodology:

1. Firstly, the data needed to be uploaded and ready to access for the project.
2. Secondly, to make sure the data was ready for analysis it needed to be cleaned of null values, duplicates, outliers and required label encoding as some of the features were objects of boolean value.
3. The next step, was exploratory data analysis (EDA). This was done to get a view of the relationships of the variables to see the correlation with the target variable (placement) and to check for any multicollinearity that would affect the machine learning model.
4. After, I utilised hyperparameterisation on multiple models, using GridSearchCV to gain insight on what the best model and its parameters would be to build the most accurate predictor. Models used were: Support Vector Machine, Logistic Regression, Decision Tree, Random Forest, K-Nearest Neighbour, and Ridge Regression.
6. Once the best model is found, I tested all models to gain a view on its precision, training accuracy and testing accuracy to evaluate the models.

## Results

The results from the EDA showed that when it came to placement, it did not only come down to students' academic performance. Whilst academic performance was a key feature and positively correlated towards placement, it was more of a combination of academic performance, practical skills, and soft skills. This is because the EDA showed that Projects Completed and Communication were key features (and positively correlated towards placement) in determining the outcome of placement. 

For the machine learning model, whilst Random Forest was found to be the highest predictor (and Decision Tree a close second), the results indicated that there could have been overfitting since both models hit close to 1.0 accuracy score. Additionally, it was found in the dataset that it was extremely unbalanced as there were a lot more instances for the non-placement data than the placement data. This could also mean the models were undertrained for placement since the most common error for precision was false positive.

## Challenges and Future

The main challenge faced was the data imbalance and this needed to be mitigated with synethetic data. I think in the future more real world data for the placement class will be needed to gain a more accurate model and a better understanding of the patterns and relationships for this class.
