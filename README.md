# HR-Analytics
 I completed a full HR Analytics Dashboard project using Power BI — inspired by the #Codebasics playlist “Data Analyst Project for Beginners (HR Analytics)”.

🚀 Project Overview

The goal of this project is to analyze employee attendance data and deliver insights that help HR teams track:

Presence percentage

Work-from-home (WFH) trends

Sick leave patterns

Monthly and employee-level performance

Attendance consistency across teams

The final output is an interactive Power BI dashboard designed for HR managers to make better workforce planning decisions.

🛠️ Tools & Technologies

Power BI

Power Query

DAX (Data Analysis Expressions)

Excel / CSV dataset

Data Modelling

📂 Dataset

The dataset includes employee attendance information such as:

Date

Employee ID

Department

Work status (Present, WFH, Sick Leave, etc.)

(Note: A sample/cleaned dataset is included for demonstration purposes.)

📐 DAX Measures Used

Below are the key DAX formulas used to calculate core HR KPIs:

Total Days = COUNTROWS(Employee_Attendance)

Present Days = 
CALCULATE(
    COUNTROWS(Employee_Attendance),
    Employee_Attendance[Status] = "Present"
)

WFH Days =
CALCULATE(
    COUNTROWS(Employee_Attendance),
    Employee_Attendance[Status] = "Work From Home"
)

Sick Leave Days =
CALCULATE(
    COUNTROWS(Employee_Attendance),
    Employee_Attendance[Status] = "Sick Leave"
)

Presence % = DIVIDE([Present Days], [Total Days], 0)

WFH % = DIVIDE([WFH Days], [Total Days], 0)

Sick Leave % = DIVIDE([Sick Leave Days], [Total Days], 0)


These measures were used to build visualizations and trend-line insights across months, employees, and departments.

📊 Dashboard Features

Monthly presence, WFH, and sick leave trend analysis

Department-wise attendance performance

Employee-level drill-down insights

Interactive slicers for department/date/employee

Clean, professional layout with reusable KPI cards

📘 Learnings

Through this project, I practiced:

end-to-end data cleaning and transformation

creating DAX measures and calculated columns

designing a visually compelling, business-ready dashboard

improving data storytelling and insight presentation

📎 Files Included

.pbix file (Power BI dashboard)

Dataset/ folder (sample dataset)

README.md (this file)

Images/screenshots of the dashboard

🤝 Contributions

Feel free to fork, open issues, or suggest improvements.
Feedback is always welcome!
