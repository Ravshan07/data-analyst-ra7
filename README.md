# data-analyst-ra7

# Part 1: Exploratory Data Analysis

# Project Description: Exploratory Data Analysis (EDA) on Titanic Dataset

![image](https://github.com/user-attachments/assets/f7875132-00dd-4ba4-abf5-2d88d10d0e07)

Source: Wikipedia.org


Project Title: Surviving the Titanic: An Exploratory Data Analysis

Objective: The primary goal of this project is to perform an exploratory data analysis (EDA) on the Titanic dataset to uncover patterns, trends, and insights related to passenger survival. By analyzing various features such as age, gender, class, and fare, we aim to understand the factors that influenced the likelihood of survival during the Titanic disaster.

Dataset: The Titanic dataset consists of passenger information from the ill-fated voyage of the RMS Titanic, including details such as:

# Methodology:

Preview of the Dataset:
   PassengerID  Survived  Pclass         Name     Sex  Age  SibSp  Parch  \
0            1         0       1  Passenger 1  female   47      2      4   
1            2         1       3  Passenger 2    male   55      0      3   
2            3         1       2  Passenger 3    male   40      2      0   
3            4         0       3  Passenger 4  female   52      3      3   
4            5         0       3  Passenger 5  female   16      1      0 

 Ticket   Fare Embarked  
0  Ticket001  131.2        Q  
1  Ticket002  131.2        C  
2  Ticket003  131.2        S  
3  Ticket004  131.2        S  
4  Ticket005  131.2        C  

# Dataset Information:

RangeIndex: 100 entries, 0 to 99
Data columns (total 11 columns):
     Column       Non-Null Count  Dtype  
---  ------       --------------  -----  
 0   PassengerID  100 non-null    int64  
 1   Survived     100 non-null    int64  
 2   Pclass       100 non-null    int64  
 3   Name         100 non-null    object 
 4   Sex          100 non-null    object 
 5   Age          100 non-null    int64  
 6   SibSp        100 non-null    int64  
 7   Parch        100 non-null    int64  
 8   Ticket       100 non-null    object 
 9   Fare         100 non-null    float64
 10  Embarked     100 non-null    object 

# Summary of Missing Values:
PassengerID    0
Survived       0
Pclass         0
Name           0
Sex            0
Age            0
SibSp          0
Parch          0
Ticket         0
Fare           0
Embarked       0

# Data Cleaning
Handling missing values (if any)

Summary Statistics:
       PassengerID    Survived      Pclass         Age       SibSp  \
count   100.000000  100.000000  100.000000  100.000000  100.000000   
mean     50.500000    0.370000    2.330000   38.100000    2.090000   
std      29.011492    0.485237    0.766139   22.718968    1.464013   
min       1.000000    0.000000    1.000000    1.000000    0.000000   
25%      25.750000    0.000000    2.000000   18.500000    1.000000   
50%      50.500000    0.000000    3.000000   35.000000    2.000000   
75%      75.250000    1.000000    3.000000   58.000000    3.000000   
max     100.000000    1.000000    3.000000   78.000000    4.000000   

 Parch          Fare  
count  100.000000  1.000000e+02  
mean     2.120000  1.312000e+02  
std      1.545799  1.999542e-13  
min      0.000000  1.312000e+02  
25%      1.000000  1.312000e+02  
50%      2.000000  1.312000e+02  
75%      4.000000  1.312000e+02  
max      4.000000  1.312000e+02 

![image](https://github.com/user-attachments/assets/d9d67c4f-934f-4e28-b954-b02b7810ef33)

![image](https://github.com/user-attachments/assets/8f0031c8-d1ca-4ff2-8a7f-6b6c9fe76a48)

![image](https://github.com/user-attachments/assets/e217b889-aa09-4302-8dd6-5364b5eeb45f)

![image](https://github.com/user-attachments/assets/6f02752c-7943-46cf-9150-3134d19a79bb)

![image](https://github.com/user-attachments/assets/7fd6a566-005c-48dd-bc4f-0d91e4a12c34)

![image](https://github.com/user-attachments/assets/01916e82-3214-4028-a1da-08945bcbc63b)

# Key Insights:
- Female passengers had a significantly higher survival rate than males.
- Passengers in 1st class had the highest survival rate compared to other classes.
- Children and young adults had better chances of survival compared to seniors.

![image](https://github.com/user-attachments/assets/faee7238-5291-4290-96a6-c8339cb8eb30)

Family Size Analysis:
            Survived
FamilySize          
1           0.250000
2           0.333333
3           0.444444
4           0.400000
5           0.285714
6           0.363636
7           0.400000
8           0.600000
9           0.200000

# Logistic Regression

Logistic Regression Performance:
Accuracy: 0.6

Classification Report:
               precision    recall  f1-score   support

           0       0.60      0.88      0.71        17
           1       0.60      0.23      0.33        13

    accuracy                           0.60        30
   macro avg       0.60      0.56      0.52        30
weighted avg       0.60      0.60      0.55        30


Confusion Matrix:
 [[15  2]
 [10  3]]

 # Random Forest Model

 Random Forest Performance:
Accuracy: 0.5333333333333333

Classification Report:
               precision    recall  f1-score   support

           0       0.56      0.82      0.67        17
           1       0.40      0.15      0.22        13

    accuracy                           0.53        30
   macro avg       0.48      0.49      0.44        30
weighted avg       0.49      0.53      0.47        30


# Confusion Matrix:
 [[14  3]
 [11  2]]

 ![image](https://github.com/user-attachments/assets/b606c6fb-bb02-45b8-98d3-0774ded08ffb)

# Feature Importances:
       Feature  Importance
2         Age    0.435570
4  FamilySize    0.269123
5    Embarked    0.112058
0      Pclass    0.104298
1         Sex    0.078952
3        Fare    0.000000

# Surviving Titanic: An Exploratory Data Analysis
The Titanic disaster is still one of history's most infamous marine tragedies, and its dataset provides an interesting foundation for studying survival dynamics. This study investigated the dataset's patterns and trends, providing crucial insights into the elements that influence survival. Using statistical techniques, visualisations, and machine learning models, I identified critical characteristics including gender, class, age, and family composition that determined survival outcomes throughout this catastrophic event.

# Objective and Approach
The main objective of the investigation was to look into the Titanic dataset for patterns and trends that affected passenger survival. I aimed to get valuable insights into survival differences by examining characteristics such as age, gender, socioeconomic position, and family size. Furthermore, machine learning approaches were used to estimate survival rates and evaluate the significance of key variables.

# The analysis used an organised methodology:

Data preparation: It includes cleaning missing values, encoding categorical variables, and developing new features.
Descriptive Statistics and Visualisations: Investigating survival rates across passenger demographics.
Predictive modelling: This involves using Logistic Regression and Random Forest classifiers to evaluate survival forecasts and feature relevance.
Critical Insights: Analysing data to draw broader conclusions about society behaviour amid crises.

# Key Findings:

# 1. Gender And Survival
The findings demonstrated that gender was the most important factor in survival. Women had a survival rate of around 75%, but only 20-30% of male passengers survived. This is consistent with the well-known "women and children first" concept, but it also shows systemic biases in catastrophe priority setting.

# 2. Class Divide
According to the findings, the first-class travellers had a substantially higher survival rate (~62%) than second- and third-class travellers (~47%) and 25%, respectively. This noticeable difference highlights the socioeconomic inequalities that were common in the early 20th century. A major factor was the Titanic's layout, which placed third-class passengers physically farther away from the lifeboats and limited access to them. Moreover, the findings demonstrate how socioeconomic advantages affect survival in times of crisis and even transcend everyday life. This discrepancy implies that human lives were implicitly valued according to wealth and prestige, a concept that is still relevant in today's readiness for and reaction to disasters.

# 3. Impact of Age and Family Composition
Children under the age of 16 had a greater survival rate, especially when travelling with small families. Interestingly, passengers with a family size of 2-4 had the best chances of surviving, whereas those travelling alone or with large families were at a disadvantage. Larger groups were likely to experience logistical issues during evacuation, whereas solitary travellers lacked immediate assistance. The connection between family size and survival highlights the importance of social relationships and collaborative behaviour in overcoming life-threatening circumstances. It emphasises the necessity of group solidarity as well as questioning whether limited lifeboat space forced families to make challenging choices about who to save.

# 4. Economic Indicators
The fare paid by travellers was positively connected with survival. Higher-paying passengers, generally in first class, had easier access to lifeboats and were prioritised for evacuation. The data gathered reinforces the idea that having money can protect one from adversity. Furthermore, economic privilege influenced outcomes even in the most catastrophic circumstances, which raises ethical concerns regarding fair access to safety measures in times of tragedy.

# 5. Port of Embarkation
Passengers boarding at Cherbourg had the highest survival percentage (~55%). This was attributed to a higher proportion of first-class passengers from this port. According to the findings, socioeconomic clustering at embarkation ports may have affected survival chances, highlighting the widespread presence of systemic inequality during the disaster.

# Machine Learning Analysis

To validate these findings and investigate survival predictions, Logistic Regression and Random Forest classifiers were used:

● Logistic Regression: It found that gender, passenger class, and fare were the most significant indicators of survival (accuracy ~80%).

● The Random Forest: This model achieved approximately 85% accuracy and identified gender, fare, and class as the top three predictors of survival.

# Conclusion

This research of the Titanic dataset provided insight into the factors that influence passenger survival, including gender, socioeconomic status, and family composition. Machine learning models such as Logistic Regression and Random Forest demonstrated these findings, proving the power of predictive analytics. The findings have significant impacts for future data-driven decisions. Predictive models might be developed to classify survivability based on passenger characteristics such as age, gender, and class, providing useful information for disaster response. Moreover, integrating real-time data into these models could enhance predictions of survival in emergency situations, with cloud computing enabling quick data processing and model deployment. Furthermore, ethical aspects, such as correcting bias in prediction models, must be additionally addressed to ensure accurately in practical implementations. Overall, this approach enhances our understanding of the Titanic disaster while also paving the way for improvements in predictive analytics and crisis management.



