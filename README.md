# Data Immersion & Wrangling Project

## Project Objective
The goal of this project was to take a raw, "dirty" employee dataset and transform it into an analysis-ready format using Python and Pandas.

## Data Dictionary
| Column Name | Description | Data Type | Business Relevance |
| :--- | :--- | :--- | :--- |
| **Model** | Subscription/Plan type (Basic, Intermediate) | Categorical | Segmenting employee benefits |
| **Name** | Full name of the employee | String | Personal identification |
| **Employee_ID** | Unique numeric identifier | Integer | Primary key for data integrity |
| **Job_Level** | Employee rank (Analyst, Executive, etc.) | Categorical | Compensation and hierarchy analysis |
| **Attendance** | Binary status (Present/Absent) | Boolean/Cat | Tracking productivity/presence |
| **Salary** | Monthly base pay | Float | Fixed operational cost |
| **Bonus** | Performance-based incentive | Float | Variable operational cost |
| **Total_Compensation**| Sum of Salary + Bonus | Float | **(Engineered)** Total cost per employee |

## Cleaning Steps Taken
1. **Column Renaming:** Simplified verbose headers (e.g., "Please select your Manager Name" → "Manager_Name").
2. **Data Type Correction:** Converted the `Date` column from string to datetime objects.
3. **Typos & Formatting:** Fixed "Anyalst" spelling error and stripped extra whitespace from the "Model" column.
4. **Feature Engineering:** Created the `Total_Compensation` column to provide a holistic view of pay.
5. **Deduplication:** Verified unique records based on ID and Model type.

## How to Run
1. Ensure you have `pandas` and `openpyxl` installed: `pip install pandas openpyxl`
2. Run the `cleaning_script.py` provided in this repo.
3. The cleaned file will be exported as `cleaned_employee_data.csv`.
