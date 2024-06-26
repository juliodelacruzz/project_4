# project_4

### UC Berkeley Data Analytics and Visualization Bootcamp 2023-24
Group 4: Julio Dela Cruz, Everardo Garcia, Amanpreet Kaur, David Robles, Dylan Sui

Project Website URL: https://juliodelacruzz.github.io/project_4/

![Shutterstock_1910971966](https://github.com/juliodelacruzz/project_4/assets/149534473/be03a7a6-1184-4114-a883-bb4d03ee72e1)


## Description:

This database is from a large US company (no name given for privacy reasons). The management department is worried about the relatively high turnover. They want to find ways to reduce the number of employees leaving the company and to better understand the situation, which employees are more likely to leave, and why.

The data
The HR department has assembled data on almost 10,000 employees who left the company between 2016-2020. They used information from exit interviews, performance reviews, and employee records.

  - "department" - the department the employee belongs to.
  - "promoted" - 1 if the employee was promoted in the previous 24 months, 0 otherwise.
  - "review" - the composite score the employee received in their last evaluation.
  - "projects" - how many projects the employee is involved in.
  - "salary" - for confidentiality reasons, salary comes in three tiers: low, medium, high.
  - "tenure" - how many years the employee has been at the company.
  - "satisfaction" - a measure of employee satisfaction from surveys.
  - "bonus" - 1 if the employee received a bonus in the previous 24 months, 0 otherwise.
  - "avg_hrs_month" - the average hours the employee worked in a month.
  - "left" - "yes" if the employee ended up leaving, "no" otherwise.

## Instructions:

1. (Julio)  Using Logistic Regression model, I wanted to see how well the model performed in predicting if an employee would leave or not. After importing the data, I encoded the categorical columns and then split the data. I also scaled the data. From there I created the logistic regression model and use it both on the scaled training and test data. Afterwords, one of my groupmates brought up the idea of class imbalance and suggested we try it with one of our models. I proceeded to downsample the majority (people who stayed) to match minority class. The results were interesting as the model was less accurate, but had better predictive power for the minority class. It was then my responsibility to analyze the logistic model and the class imbalance. I was also in charge of creating the webpage and deploying it to github pages.


2. The model I tested was a Support Vector Machine (SVM): SVM is a powerful classification algorithm that finds the hyperplane that best separates data points of different classes. It can handle both linear and non-linear data.
As you can see, the accuracy is solid at 83%. We have two classes, one of employees who are not leaving, and the other of employees who are leaving.  Precision is strong at 83 and 82% for both classes. For employees not leaving, the recall is at 94%, which is great. But for employees who are leaving, the recall is only at 57%. This indicates the model only correctly identified 57% of the employees who are leaving. A little better than a coin toss. 

To improve the model, I introduced class weight parameter to assign higher weights to the minority class, employees who are leaving. I set the class weight parameter to ‘balanced’ which tells the model to automatically adjust weights inversely proportional to class frequencies in the input data. In other words, the model will pay more attention to correctly classify employees who are leaving. Doing this resulted in the following:
Lower accuracy score of 77%
Precision for those not leaving increased from 83% to 91%, while it decreased for those leaving from 82% to 59%
Recall for those not leaving decreased from 94% to 75%, but increased for those leaving from 57% to 83%

Using class weights has led to a trade off in the model’s performance
Pros
-	The model has a better recall for those leaving, which means it can better identify employees who are likely to leave
-	By adding class weights, the model is more balanced in terms of sensitivity to both classes
Cons
-	Reduced precision for identifying employees who are likely to leave
-	Negative impact on overall accuracy

Using class weights has effectively addressed the primary concern of improving recall for the leaving class. If the main objective is to identify employees at risk of leaving, then the benefits of higher recall may outweigh the drawbacks of lower precision and accuracy.
(David)


3. Using SQL I try to find the reasons why the employees left the company and at the same time I try to find some possible solutions. After analyzing different columns, I found why the employees left the company. When an employee does not feel valued, when no one in the company recognizes your work and you do not have a position promotion, it is evident that you will look for a place where you do feel valued and therefore can grow in your work life. That being said,  I compared the employees who left the company but were promoted vs the employees who left the company but were not promoted. Finally, I grouped employee data by number of projects, counting those who left with bonuses and those who left without bonuses, providing insight into attrition trends based on project participation and rewards received. As we can see in the photo below, giving a bonus to deserving employees is a great action to retain them in the company.

After analyzing our data sets in different ways and scenarios, I discovered possible reasons why employees left this company and once we identify the problem, we can propose possible solutions.

  - It is clear that when an employee does not feel that their work is taken into consideration and does not see job growth, it is very likely that they will resign.
  - Likewise, we discovered that giving bonuses can be a good incentive for employees to feel motivated and somehow valued, but it is still not enough to prevent an employee from leaving the company.
(Everardo)


4. Using Tableau, I effectively showcased the data by creating interactive and a visually appealing dashboard. I started by importing the dataset into Tableau and then utilized various features like drag-and-drop functionality to build visualizations such as bar charts, text table, and side by side circle comparisons. I ensured the data was organized logically and made use of filters, parameters, and calculated fields to provide users with dynamic insights. By employing color coding, tooltips, and labels, I enhanced the clarity of the visualizations and made them more engaging. Overall, my use of Tableau helped transform raw data into actionable insights that were easily understandable and accessible to my audience. (Dylan)


5. Using google colab notebook, I began by importing all necessary dependencies including machine learning libraries Scikit-learn, TensorFlow; visualization libraries Matplotlib, Seaborn; and Pandas. The working dataset was obtained as a csv file and read into a Pandas DataFrame. After preprocessing the data for datatypes, null values, and unique columns, I converted the categorical data into numerical data. The data was split into all other features(X) and the target(y) variable as employees who “left” the company. Then split again into train and test dataset. Data was scaled and then processed using a neural network model with defined nodes, hidden layers, and number of epochs. In order to optimize the model further, features were reassessed by creating a Correlation Matrix. Selected features were also visualized using FacetGrid, a multi-axes grid with subplots visualizing the distribution of these features against the target variable. Dataset was cleaned up based on these findings, split and scaled again. The neural network was trained with this training dataset and evaluated with the testing dataset again. Any other changes to optimizing the machine learning model and the resulting changes in model performance were documented at the end of the script. 


## Ethical Considerations:
The name of the company that this data came from is not named due to privacy reasons. Therefore, we are confident that we are ethically using this data for our project.


## Data Limitations:

- For confidentiality reasons, the data set does not provide company name, salary ranges, or employee names. 
- No employee demographic info (age, gender, education level); 
- No industry sector where company operates; 
- 2016-2020 are pre-/early pandemic years but work-from-home or flexible hours as additional employee incentives are not mentioned in the dataset.


## Kaggle metrics:
This score is calculated by Kaggle.

### Completeness · 100%

✔ Subtitle
✔ Tag
✔ Description
✔ Cover Image

### Credibility · 67%

✘ Source/Provenance
✔ Public Notebook
✔ Update Frequency

### Compatibility · 50%

✔ License
✔ File Format
✘ File Description
✘ Column Description

## Sources:

- https://www.kaggle.com/datasets/marikastewart/employee-turnover/data

## Built With:

- https://community.cloud.databricks.com/
- Tableau
- Python
- Pandas
- Sklearn
- Pathlib
- SQL
- TensorFlow
- Seaborn
- MatplotLib
