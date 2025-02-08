# Predicting Student Dropouts Using Machine Learning and Analytical Techniques
**Dataset Link: [https://www.kaggle.com/yelp-dataset/yelp-dataset](https://www.kaggle.com/datasets/abdullah0a/student-dropout-analysis-and-prediction-dataset.)**
# 1. Overall Project Objectives
The problem this project aims to solve is predicting student dropout rates based on their social backgrounds and behavioral patterns. The goal of this project is to create models that can predict students who are inclined to dropuout with a focus on improving the true positive rate. True positive rate is the evaluating metric of maximizing interest because it correctly identifies as many actual at-risk students as possible. This focus is important because it allows organizaitons in educational sectors to take early action to assist the students who need it most.

# 2. Description of Data
The Dropout dataset is downloaded from Kaggle website. In total, there are 650 student records and 34 features. 

**Attributes of Dropout dataset are as following:**

School: Name of the school attended (e.g., MS).

Gender: Gender of the student (e.g., M for Male, F for Female).

Age: Age of the student.

Address: Type of residence (U for urban, R for rural).

Family_Size: Size of the family (GT3 for greater than 3, LE3 for less than or equal to 3).

Parental_Status: Living arrangement of parents (A for living together, T for living apart).

Mother_Education: Education level of the mother (0 to 4).

Father_Education: Education level of the father (0 to 4).

Mother_Job: Type of job held by the mother.

Father_Job: Type of job held by the father.

Reason_for_Choosing_School: Reason for selecting the school (e.g., course).

Guardian: Guardian of the student (e.g., mother).

Travel_Time: Time taken to travel to school (in minutes).

Study_Time: Weekly study hours (1 to 4).

Number_of_Failures: Number of past class failures.

School_Support: Whether the student receives extra educational support (yes/no).

Family_Support: Family provided educational support (yes/no).

Extra_Paid_Class: Participation in extra paid classes (yes/no).

Extra_Curricular_Activities: Involvement in extracurricular activities (yes/no).

Attended_Nursery: Attendance in nursery school (yes/no).

Wants_Higher_Education: Desire to pursue higher education (yes/no).

Internet_Access: Availability of internet at home (yes/no).

In_Relationship: Romantic relationship status (yes/no).

Family_Relationship: Quality of family relationships (scale 1 to 5).

Free_Time: Amount of free time after school (scale 1 to 5).

Going_Out: Frequency of going out with friends (scale 1 to 5).

Weekend_Alcohol_Consumption: Alcohol consumption on weekends (scale 1 to 5).

Weekday_Alcohol_Consumption: Alcohol consumption on weekdays (scale 1 to 5).

Health_Status: Health rating of the student (scale 1 to 5).

Number_of_Absences: Total number of absences from school.

Grade_1: Grade received in the first assessment.

Grade_2: Grade received in the second assessment.

Final_Grade: Final grade received (G3).

Dropped_Out: Indicator of whether the student has dropped out (True/False).

# 3. Direction of Training

1. Naive Baseline Model:
   
   Apply the naive basline model, model predicting the result with the most frequency in training data, and achieve 85% in accuracy.

2. Logistic Regression Model:

   Fit the logistc regression model and went through a features selection process to reduce multi-collinearity. The model ends up with features such as Grade_1, Grade_2, and Age. 

3. Classification Tree Model:

   Use cross-validation to train a classification tree model and show a tree graph based with clear splits on nodes resulting in highest impurity.

4. Random Forest Model:

   Use cross-validation and boostrap agrregation to train a random forest model. 

# 4. Findings

The three models we chose are Logistic Regression, Classification Tree, and Random Forest. In the context of student dropout prediction, TPR (True Positive Rate) is a key metric because it helps identify students who are actually at risk of dropping out of school, thus allowing schools to intervene promptly. At the same time, FPR (False Positive Rate)
also needs to be looked at as high FPR can lead to a waste of resources, e.g., allocating limited support resources to students who are actually not at risk. The numerical result shows that:

• Logistic Regression has the highest accuracy (0.944) and the lowest FPR (0.012), making it effective at correctly categorizing students and minimizing resource waste. However, the TPR is low (0.690) compared to the other models, indicating that more students who are at risk of dropping out of school are missed.

• Classification Tree has the highest TPR (0.828), indicating that it is effective in identifying most of the students at risk of dropping out. However, it has the lowest accuracy (0.877) and the highest FPR (0.114), indicating that more students who are not at risk of dropping out are misclassified as high risk, which may lead to wasted resources.

• Random Forest achieved a good balance between TPR (0.793) and FPR (0.048) while maintaining a high accuracy (0.928). Despite its balanced performance, it has a slightly lower TPR compared to the Classification Tree and may miss some of the students who are truly at risk.

Plus

• "Grade_1”, “Grade_2” appear to be determining of the result in all three models. 

• In the later validation process with boostrap and visualization of confidence interval, there is no statistical difference in terms of accuracy and TPR within these three models. The performance of FPR, however, can be shwon different according to the result. 



   
   

