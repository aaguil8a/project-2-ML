# Student Math Performance

For this project, I took dataset from Kaggle about final scores of students at the end of a math programs with several features that might or might not impact the future outcome of these students. To that end, the following was asked when investigating this dataset: what factors influence students’ final grades in math course subjects? 


# Dataset

soure: https://www.kaggle.com/janiobachmann/math-students

* Entries: 395
* Features: 33
* Target: G3 (final grade numeric: from 0 to 20)


# Features:

Attributes for both student-mat.csv (Math course) and student-por.csv (Portuguese language course) datasets:

1 school - student's school (binary: 'GP' - Gabriel Pereira or 'MS' - Mousinho da Silveira)

2 sex - student's sex (binary: 'F' - female or 'M' - male)

3 age - student's age (numeric: from 15 to 22)

4 address - student's home address type (binary: 'U' - urban or 'R' - rural)

5 famsize - family size (binary: 'LE3' - less or equal to 3 or 'GT3' - greater than 3)

6 Pstatus - parent's cohabitation status (binary: 'T' - living together or 'A' - apart)

7 Medu - mother's education (numeric: 0 - none, 1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)

8 Fedu - father's education (numeric: 0 - none, 1 - primary education (4th grade), 2 â€“ 5th to 9th grade, 3 â€“ secondary education or 4 â€“ higher education)

9 Mjob - mother's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'athome' or 'other') 10 Fjob - father's job (nominal: 'teacher', 'health' care related, civil 'services' (e.g. administrative or police), 'athome' or 'other')

11 reason - reason to choose this school (nominal: close to 'home', school 'reputation', 'course' preference or 'other')

12 guardian - student's guardian (nominal: 'mother', 'father' or 'other')

13 traveltime - home to school travel time (numeric: 1 - <15 min., 2 - 15 to 30 min., 3 - 30 min. to 1 hour, or 4 - >1 hour)

14 studytime - weekly study time (numeric: 1 - <2 hours, 2 - 2 to 5 hours, 3 - 5 to 10 hours, or 4 - >10 hours)

15 failures - number of past class failures (numeric: n if 1<=n<3, else 4)

16 schoolsup - extra educational support (binary: yes or no)

17 famsup - family educational support (binary: yes or no)

18 paid - extra paid classes within the course subject (Math or Portuguese) (binary: yes or no)

19 activities - extra-curricular activities (binary: yes or no)

20 nursery - attended nursery school (binary: yes or no)

21 higher - wants to take higher education (binary: yes or no)

22 internet - Internet access at home (binary: yes or no)

23 romantic - with a romantic relationship (binary: yes or no)

24 famrel - quality of family relationships (numeric: from 1 - very bad to 5 - excellent)

25 freetime - free time after school (numeric: from 1 - very low to 5 - very high)

26 goout - going out with friends (numeric: from 1 - very low to 5 - very high)

27 Dalc - workday alcohol consumption (numeric: from 1 - very low to 5 - very high)

28 Walc - weekend alcohol consumption (numeric: from 1 - very low to 5 - very high)

29 health - current health status (numeric: from 1 - very bad to 5 - very good)

30 absences - number of school absences (numeric: from 0 to 93)

these grades are related with the course subject, Math: 31 G1 - first period grade (numeric: from 0 to 20)

31 G2 - second period grade (numeric: from 0 to 20)

32 G3 - final grade (numeric: from 0 to 20, output target)


# Observation

## Q1: What is the overall student performance?

![image](https://user-images.githubusercontent.com/55922514/144203442-74e30344-38eb-4a8c-8d31-e374b7042e0d.png)





For the most part, students did not do that well since only 209 passed while 186 failed.





## Q2: How much does absence influence students’ final grade?

![image](https://user-images.githubusercontent.com/55922514/144205086-5e0cf999-7120-42b0-917e-d94bee174f38.png)






We can see that given more absences, then students do worse in final grade.



## Q3: How much does first grade and mid grades affect students’ final grade?

![image](https://user-images.githubusercontent.com/55922514/144214239-88c2888d-e5f9-4367-8487-a810332a2bdf.png)


![image](https://user-images.githubusercontent.com/55922514/144214268-470013bb-6b89-4488-9be3-3d1750636139.png)





We see that if students do well in prior grading periods that will influence how well he/she does in final grades.

## General observations

There are not many variables that show an influence on students’ final grades, which is interesting in itself since that may indicate the right kind of data was not gathered.

# Feature Importance

Feature|Importance|
|---|---
G2| 0.767002
absences| 0.122073
reason_home| 0.013175
age| 0.013127








# Models Eva

Models|R^2|RMSE
---|---|---
Baseline Model|0.06%|4.80
Linear Regression|78.11%|2.25
Decision Tree|80.49%|2.12
Bagged Tree|85.59%|1.82
Random Forest|85.86%|1.80

Random Forest did best since it had the lowest prediction error.
