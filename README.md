## Salary Data analysis

The data used in this assignment is “Salary dataset based on country and race”. The data is collected from the companies HR Database and consists of some key variables that can be used in the analysis.
All the variables in the dataset need to be studied carefully to find the potential problems that could arise while analysing the data and rectify it at the initial stage of the analysis. 

**The main business question is - What are the main factors affecting the running of the company?**
1. Does the company mostly hire younger employees as compared to older employees with more experience?
2. Are male employees paid a higher salary with respect to education level?
3. Is there any significance between race and education level of an employee?
4. What is the role of years of experience along with the education level when it comes to the salary?

Targeting this, a jupyter notebook has been used to write codes to clean and filter the data. 
The data has been imported and saved as df. 
The dataset contains 6704 entries. We then find missing values in the dataset which must be dealt with as it can cause complications during analysis processes. 
Now, after the data cleaning and summarising is done, we move on to Hypothesis testing:

In the next steps, to further analyse the dataset, we use inferential tools and machine learning methods like hypothesis, simple linear regression etc. Firstly, we start by formulation of hypothesis based on the business questions that we are targeting.  

## Hypothesis Formulation and Testing:

1. Does the company mostly hire younger employees as compared to older employees with more experience?

H0: Hiring employees from lower age groups has no effect on the company
H1: Hiring employees from lower age groups affects the company

This hypothesis is formulated to check if the age of the employees being recruited has any effect on the company and if so, how to go about this.
To test this, we identify that the most crucial variable is: Age of the employees and perform the test using this.
I have chosen the Two Tailed z - Test. This test is used if the sample size is greater than 30 and the population mean, and standard deviation are known. In case the sample size was less than 30, then we use the t – Test. Therefore, in this test we choose a random sample of size 100 (n) from the population and perform z test using the formula  . This follows the Central Limit Theorem (CLT), that is, as the number of samples increases, they are considered normally distributed. 
A Two tailed z test is used to check if there is any significant difference due to lower age groups in the company. We set the α value to 0.05 which means that the level of significance is 95% allowing for a 5% chance of being wrong and it also reduces the risk of committing a Type 1 error (false positive). The null hypothesis contains the “equals” sign as it signifies that lower age groups do not cause any difference in the company while the alternative hypothesis has the “not equal” sign to check if there is a significant difference or not. 

H0: μ = μ0
H1: μ ≠ μ0

**Conclusions:**

From the above test, we can conclude that: 
Since the z test statistic lies between the z critical values, that is, it is not below -1.96 or above 1.96 = 
-1.96 < -0.85 < 1.96.  
Therefore, we cannot reject the null hypothesis since we do not have evidence. Accepting the null hypothesis, H0: μ = μ0, we see that hiring employees from lower age groups does not affect the company, which could imply that age is just a number and does not have an incredibly significant role in the running of the company. What really matters is the knowledge, ideas, skills and working experience that an employee possesses through jobs, research papers, projects and even self-studies.
This will in turn benefit the company and help in the various aspects like fresh ideas from the younger crowd who might be more up to date with the trends and patterns going around. This can benefit areas like sales and marketing, advertising, on platforms like Instagram, Twitter and even the newest social media platforms like threads. 


2. Are male employees paid a higher salary than female employees with respect to education level? 
H0: Gender and education level are not significant to the salary of the employee
H1: Gender and education level are significant to the salary of the employee

This hypothesis is formulated to check if there is any significant effect of two crucial variables gender and education level on the salary of an employee. Gender equality in the workplace is an important aspect now. Previously, females were not given high levels of education but that has gradually been changing and can be seen in the given statistics as well. Although not as much as males but females are also being recognised. The “Other” gender is also slowly gaining recognition though with a lot of struggles as people are still stuck in the old ways of looking at things. Using the data, we formulate this test to understand this component from a company perspective.
To test this, I have used the Chi - Square Test: , where  is the observed frequency and  is the expected frequency.
Since gender and education level are two nominal categorical variables, that is, they have no natural ordering, this test is used to check if there is a relationship between the two variables or if it is due to chance. 
Chi - Square test is used to compare observed and expected frequency. It is used to bridge the gap in predicted and actual data which in turn informs us about the relationship between the variables. 
In order to run this test, we create a pivot table for gender, education level and the count of gender to obtain the frequencies, both observed and expected. The expected frequencies are calculated using the formula: 

We calculate the p-value using the excel function: CHITEST (observed values, expected values).
Again, we set the α value to 0.05 with 95% level of significance and we know that:
If p-value < 0.05, then we reject the null hypothesis.
If p-value > 0.05, then we accept the null hypothesis.

**Conclusion:**

From the above test, we can infer that the p-value = 3.9579E-73 is < 0.05. 
Therefore, we have enough evidence to reject the null hypothesis which states that gender and education level are not significant to the salary of the employee. 
So, we can conclude that gender and education level are significant to the salary and therefore, salary is a dependent variable that is affected by these two variables. 
Hence, it is important to constantly up skill and increase one's knowledge about things around as the world is constantly evolving and new things are being created and discovered at all times. 

3. Is there any significance between race and education level of an employee?

H0: The education level of different races is not significant for employment
H1: The education level of different races is significant for employment

The employees from the 10 different races come from different countries, are hired for different job roles, have different years of experience and salaries. However, education level might be significantly affected by the race of the employee. Different countries have different customs and beliefs. Some are still backward and do not think a remarkably high level of education could alter one's career in a significant way. Therefore, we try to understand and check this notion and bridge this gap by offering corrective methods for the situation if required we use this hypothesis.
In this hypothesis test, the main goal is to infer whether different education levels of the employees from the multiple races have a significance on their employment or not.
Again, the variables race, and education level are categorical variables so therefore we use the 
Chi – Square Test:  , where is the observed frequency and   is the expected frequency.
Chi - Square test is used to compare observed and expected frequency. It is used to bridge the gap in predicted and actual data which in turn informs us about the relationship between the variables. 
In order to run this test, we require observed frequencies that can be obtained from the data, expected frequencies that are calculated using the formula: 
Using the data, we create a pivot table for race and education level, using the count of race which gives us the observed frequencies and then we calculate the expected frequencies using the above given formula. 

We calculate the p-value using the excel function: CHITEST (observed values, expected values).
Again, we set the α value to 0.05 with 95% level of significance and we know that:
If p-value < 0.05, then we reject the null hypothesis.
If p-value > 0.05, then we accept the null hypothesis.

**Conclusion:**

From the above test, we can infer that the p-value = 0.455435 is > 0.05. 
Therefore, we have enough evidence to accept the null hypothesis which states that race and education level are not significant to the salary of the employee. 
From this we understand that race and education level are two independent variables not directly affecting the employee's salary together. 
Independently, education level is not as significant as one might think. 
Some job titles might require a higher level of education in a particular subject before offering significant jobs in the industry, however some jobs just require more practice and work experience in a practical setting. Higher education is also looked at as a time-consuming and costly plan and therefore one must deicide according to their line of work if this is worth going through with or not. 
Similarly, the salary of different races also depends on the culture and background of the countries with respect to the education level they attain and consider good enough, either for their personal satisfaction or for society.

4. What is the role of years of experience along with the education level when it comes to the salary?
 
H0: Salary is not affected by the education level and years of experience of an employee
H1: Salary is affected by the education level and years of experience of an employee

To inspect this hypothesis, I have used a correlation test between two variables – Years of Experience and Salary. Correlation is a statistical measure that gives us information about the degree of which two variables are codependent or correlated to each other. 
It can be either positive or negative and lies between –1 and 1. Here, we calculate the correlation coefficient which informs us of the degree of which change in one variable predicts change in the other variable. 
I have used R software to verify this correlation coefficient value and have also fitted a linear regression model for Salary and Years of experience to further understand the relationship between the variables.
R Codes:
> correlation=cor(data$Salary,data$Years.of.Experience)
> correlation
[1] 0.808961

**Conclusions:**
From the calculations, we can conclude that the correlation value is 0.8089610, which is quite high. 
Since the value lies between 0.7 and 0.9, therefore there is high positive correlation between the salary of an employee and the years of experience, which means that as the years of experience increases, the salary also increases as it is a dependent variable.

**Linear regression model:**
> Linear_model=lm(data$Salary~data$Years.of.Experience)
> Linear_model
Call:
lm(formula = data$Salary ~ data$Years.of.Experience)
Coefficients:
             (Intercept)  data$Years.of.Experience  
                   58287                      7047  
> summary(Linear_model)
Coefficients:
                         Estimate Std. Error t value Pr(>|t|)    
(Intercept)              58287.00     632.51   92.15   <2e-16 ***
data$Years.of.Experience  7046.64      62.56  112.64   <2e-16 *** 

Multiple R-squared:  0.6544,    Adjusted R-squared:  0.6544 

**Conclusions:**

From the regression model we can check if the model is a good fit for the prediction of the given variables in the company.
From the regression statistics we see that:
Y is the Salary, the dependent variable and X is years of experience, the independent variable
The multiple R value is the same as the correlation coefficient as it is its absolute value
The Adjusted R Square value is slightly less than 0.7 which means that the model good, but it is not the best fit 
More number of “*” indicates that the value is more significant 
The regression equation is given by Y = β0 + β1.X1 +…+
Where β0 is the Y intercept, β1 is the slope coefficient, X is the independent variable and is an 	error term.
The regression equation for this model is:
Salary = 58287 + 7046.64 * Years of experience

Example:
If years of experience = 4, Salary = 86,473.55$
If years of experience = 11, Salary = 1,35,800.04$
…...
If years of experience = 21, Salary = 2,06,266.36$
which represents the dependence of the variables.


## Overall conclusion:

From all the previous analysis and the different tools used, the areas of focus have been identified and many conclusions have been drawn for areas of improvement in the company. The company deals with the making and manufacturing of sound boards for dogs and hence deals with several different employees whose area of focus is very different from one another. 
1. The analysis predicts that age does not affect the functioning of the company. However, since the company deals with a fairly new concept, employees belonging to a younger age group might be more innovative when it comes to creation, development, and marketing strategies of the product. A lot of social media (like Instagram reels, trends, twitter etc.) usage also goes into the promotion of a company which can be easily understood and handled by them. Although, older, more experienced employees could benefit the company in managerial, HR roles and to see through the smooth running of the company.
2. When it comes to the topic of gender in the company, we conclude that salary is affected by gender which is a major issue. The female gender has always been targeted in a work environment and now the minority gender has also been added to this category. One would think these traditions of underestimating women would have been mitigated from the current job scenario, however it is still very prominent in many companies. In view of this the company must strive to overcome this bias and adopt new ways to practice equal pay. Males, females, and all other gender identities should be judged based on their skills, knowledge and performance in their specific area of work. Incentives, commissions and bonuses should be provided to all employees depending on the level of work they complete, and they should be rewarded accordingly. A policy should be drawn up, and all varying information should be clearly stated and based only on the job role and level.
3. Race and education level are not significant to each other. Some minority races in the company like Korean’s, Black, African American’s, Hispanic understand the importance of education, however they also believe that there are other practical skills that are important in a workplace. Additionally, the company must also focus on the diversification of the company and to do so, the company must set up a separate quota to hire a specific percentage of employee's belonging to these races, communities for more networking, etc. The company can also include tie-ups with universities for employees to obtain higher education while they continue to work.
4. In some companies the recruitment team looks to hire people with a specific number of years of experience for a particular job title. For example: a senior data associate job would require a minimum of 5 years of experience unlike a data analyst fresher job that would require 0-1 years of experience. Hence, in such cases experience plays an important role.
Therefore, the company must carefully analyse the job and come up with a detailed set of requirements prior to the hiring process for effective communication with potential employees.
