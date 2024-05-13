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

1. (Julio)


2. (David)


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
