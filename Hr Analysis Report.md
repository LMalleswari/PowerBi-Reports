
# Project Title

# Hr Analysis Report

### Dashboard Link : https://app.powerbi.com/groups/me/reports/8b343ee2-98f5-436d-bc46-9544334ef810/ReportSection?experience=power-bi

## Problem Statement

This dashboard helps the HR team analyze employee attrition by examining critical factors such as education, salary, age, years of experience, job role, and department. By visualizing these metrics, the dashboard provides insights into patterns and trends contributing to employee turnover. It enables HR professionals to identify high-risk groups and underlying causes of attrition, such as salary discrepancies or job dissatisfaction in specific roles or departments. This data-driven approach supports the development of targeted retention strategies, improving overall employee satisfaction and reducing turnover rates, ultimately enhancing organizational stability and performance.
The analysis highlights that attrition is particularly high among employees earning a salary of up to 5K, with 1 to 1.5 years of experience, and within the age group of 26-35. 

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : It was observed empty values were present in the dataset,so replaced the categorical null vaules with default value and numeric value with 0 or mean of the column.And also indentified the duplicate rows and deleted the duplicates. 

- Step 5 : create a new measure to calculate AttritionRate. 

- Step 6 : In the report view,under visualizations select Donut chart ,add EducationFieldcolumn in Legend and Sum of attritionCount column to values to show Attrition by education.

![Attrition By Education](https://github.com/user-attachments/assets/df6115fc-ce12-4750-91ed-8f1250e862b5)

- Step 7 : In the report view,under visualizations,select matric and add JobRole to rows ,JobSatisfaction to columns and Sum of AttritionCount to values to show JobRole and count of Employees.

![Job roles](https://github.com/user-attachments/assets/1e105f5f-8299-49f3-a92f-7c6fad847a67)

- Step 8 : In the report view,under visualizations,select stacket column chart and add Agegroup to X-axis and Sum of AttritionCount to Y-axis to show Attrition by Age.

![Attrition by Age](https://github.com/user-attachments/assets/c76eecfd-7a07-4764-866b-316e91a512d8)

- Step 9 : In the report view,under visualizations,select stacket bar chart and add SlarySlab to Y-axis and Sum of AttritionCount to x-axis to show Attrition by Salary.

![Attrition by salary](https://github.com/user-attachments/assets/0e89fae2-419c-4269-8843-97cc6d7098be)

- Step 10 : In the report view,under visualizations,select stacket bar chart and add SlaJobRole to Y-axis and Sum of AttritionCount to x-axis to show Attrition by job. 

![Attirtion by JobRole](https://github.com/user-attachments/assets/16f99130-6e29-4622-b380-1b0eb7fba8e3)

- Step 11 : In the report view,under visualizations,select Area chart and add YearsAtCompany to x-axis and Sum of AttritionCount to y-axis to show Attrition by Experience. 

![Attrition by Experience](https://github.com/user-attachments/assets/ab5bb8df-9ea2-4fcd-b31d-7c6f353f5e7f)

- Step 12 : In the report view,under visualizations,select card and add EmpId count to field to show Counts of Employee. 

- Step 13 : In the report view,under visualizations,select card and add AttritionRate to field to show Attrition Rate of Employee. 

     New measure was created to find AttritionRate of Employees.
     Following DAX expression was written for AttritionRate
      AttritionRate = sum(HR_Analytics[AttritionCount])/SUM(HR_Analytics[EmployeeCount])

- Step 14 : In the report view,under visualizations,select card and add AttritionCount to field to show Counts of Attrition. 

![Cards](https://github.com/user-attachments/assets/3f9b7849-6def-4d34-bef2-0ba11c57276e)

- Step 15 : In the report view,under visualizations,select slicer and add department to field to show all departments. 

![Departments](https://github.com/user-attachments/assets/419bc3b4-679c-4230-a213-cfb9775caff6)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.
The analysis highlights that attrition is particularly high among employees earning a salary of up to 5K, with 1 to 1.5 years of experience, and within the age group of 26-35. 

![Report](https://github.com/user-attachments/assets/6395db1e-156c-4c09-8d16-2ea6eec40775)
