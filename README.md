# HR Analytics & Employee Attrition Dashboard

An interactive **HR Analytics Dashboard** developed to analyze employee attrition, workforce characteristics, compensation, job satisfaction, overtime, business travel, and performance using **Power BI**.

The project transforms employee-level HR data into meaningful KPIs and interactive visualizations that help identify potential attrition patterns and support data-driven HR decisions.

## Project Objective

The objective of this project is to analyze employee data and answer key HR business questions such as:

* How many employees are currently represented in the dataset?
* What is the overall employee attrition rate?
* Which departments and job roles have higher attrition?
* Does overtime relate to employee attrition?
* How does job satisfaction vary across employees?
* Which age groups have higher attrition?
* How does monthly income vary across job roles?
* What workforce patterns can HR teams monitor to improve retention?

## Tools & Technologies

* **Power BI** – Dashboard development and interactive visualization
* **DAX** – KPI and analytical measure creation
* **Microsoft Excel / CSV** – Data preparation and storage
* **Power BI Slicers** – Interactive filtering
* **PDF Business Insights Report** – Summary of key findings and recommendations

## Dataset

The dataset contains employee-level HR information with fields including:

| Column             | Description                                |
| ------------------ | ------------------------------------------ |
| Employee_ID        | Unique employee identifier                 |
| Age                | Employee age                               |
| Department         | Employee department                        |
| Job_Role           | Employee job role                          |
| Monthly_Income     | Monthly employee income                    |
| Years_At_Company   | Employee tenure in years                   |
| Job_Satisfaction   | Job satisfaction rating                    |
| OverTime           | Whether the employee works overtime        |
| Business_Travel    | Frequency of business travel               |
| Performance_Rating | Employee performance rating                |
| Attrition          | Whether the employee left the organization |

## Dashboard KPIs

The dashboard provides the following key performance indicators:

* **Total Employees**
* **Attrition Count**
* **Attrition Rate**
* **Average Monthly Income**
* **Average Job Satisfaction**

Additional workforce metrics include average age, average tenure, overtime participation, and overtime-related attrition.

## Dashboard Visualizations

The HR Analytics Dashboard includes:

1. **Attrition by Department** – compares employee attrition across departments.
2. **Attrition by Job Role** – identifies job roles with higher attrition counts.
3. **Attrition by Overtime** – compares attrition across overtime groups.
4. **Attrition by Job Satisfaction** – examines attrition patterns across satisfaction ratings.
5. **Attrition by Age Group** – evaluates attrition across employee age groups.
6. **Employee Distribution by Department** – shows workforce composition.
7. **Average Income by Job Role** – compares compensation levels across roles.
8. **Performance and Attrition Analysis** – supports investigation of performance-related retention patterns.

## Interactive Filters

The dashboard includes slicers for:

* Department
* Job Role
* Overtime
* Business Travel
* Attrition
* Job Satisfaction
* Age Group

These filters allow users to explore the dashboard dynamically and focus on specific employee segments.

## Key DAX Measures

### Total Employees

```DAX
Total Employees =
COUNTROWS(hr_data)
```

### Attrition Count

```DAX
Attrition Count =
CALCULATE(
    COUNTROWS(hr_data),
    hr_data[Attrition] = "Yes"
)
```

### Attrition Rate

```DAX
Attrition Rate =
DIVIDE(
    [Attrition Count],
    [Total Employees],
    0
)
```

### Average Monthly Income

```DAX
Average Monthly Income =
AVERAGE(hr_data[Monthly_Income])
```

### Average Job Satisfaction

```DAX
Average Job Satisfaction =
AVERAGE(hr_data[Job_Satisfaction])
```

### Age Group

```DAX
Age Group =
SWITCH(
    TRUE(),
    hr_data[Age] < 25, "Under 25",
    hr_data[Age] <= 34, "25-34",
    hr_data[Age] <= 44, "35-44",
    hr_data[Age] <= 54, "45-54",
    "55+"
)
```

## Business Insights

The dashboard is designed to help HR teams identify areas that may require attention, including:

* Departments with comparatively higher employee attrition.
* Job roles that contribute a larger share of employee exits.
* Differences in attrition between employees who work overtime and those who do not.
* The relationship between job satisfaction and employee retention.
* Attrition patterns across different age groups.
* Compensation differences across job roles.
* Workforce composition and potential retention-risk segments.

These insights can support targeted retention initiatives, employee engagement programs, workload reviews, compensation analysis, and workforce planning.

## Recommendations

Based on the dashboard analysis, HR teams can consider:

* Monitoring departments and roles with higher attrition.
* Reviewing workload and overtime patterns among employees.
* Improving employee engagement and job satisfaction initiatives.
* Evaluating compensation and career-growth opportunities by role.
* Using targeted retention strategies for higher-risk employee segments.
* Continuously monitoring attrition KPIs through an interactive dashboard.

> **Note:** Business conclusions should be interpreted in the context of the available dataset. Observed relationships do not necessarily imply causation.


## How to Use

1. Open the Power BI `.pbix` file in **Microsoft Power BI Desktop**.
2. Refresh the dataset if required.
3. Use the slicers to filter employees by department, role, overtime, travel, attrition, satisfaction, and age group.
4. Review KPI cards and charts to identify workforce and attrition patterns.
5. Refer to `Business_Insights_Report.pdf` for the summarized business findings and recommendations.

## Project Outcome

This project demonstrates the use of **data analytics, DAX, Power BI visualization, and business intelligence** to turn raw HR data into an interactive decision-support dashboard.

It can be used as a portfolio project to demonstrate practical skills in:

* Data analysis
* Data visualization
* KPI development
* DAX calculations
* Dashboard design
* HR analytics
* Business insight generation

## Author

**HINIYASRI P**

HR Analytics & Employee Attrition Dashboard – Data Analytics Project
