# Student Performance Analytics System

## Overview

This project is a Python-based Student Performance Analytics System
implemented in a Jupyter/Google Colab notebook. It reads student records
from a CSV file, processes the marks using Pandas and NumPy, calculates
student performance, assigns grades, determines pass/fail status, and
performs basic class-level analysis.

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Jupyter Notebook / Google Colab

## Dataset

The notebook works with a CSV file named `Students_Records.csv`.

The dataset contains the following fields:

-   `Student_ID`
-   `Name`
-   `Department`
-   `Maths`
-   `Physics`
-   `Chemistry`
-   `Attendance`

The notebook processes 20 student records with Student IDs from 201 to
220.

## How the Code Works

### 1. Uploading the Dataset

The notebook uses Google Colab's file upload feature to upload the
student CSV file.

``` python
from google.colab import files
uploaded = files.upload()
```

### 2. Reading the Data

Pandas is used to load the uploaded CSV file into a DataFrame.

``` python
import pandas as pd

df = pd.read_csv('Students_Records.csv')
df.head()
```

### 3. Selecting Subjects

The three academic subjects used for performance calculations are:

-   Maths
-   Physics
-   Chemistry

### 4. Calculating Total and Average

The code calculates each student's total marks and average marks from
the three subjects.

The `Total` column represents the sum of Maths, Physics and Chemistry
marks, while the `Average` column represents their mean.

### 5. Grade Calculation

The notebook assigns grades according to the student's average marks:

  Average Marks    Grade
  ---------------- -------
  90 and above     A+
  80 to below 90   A
  70 to below 80   B
  60 to below 70   C
  50 to below 60   D
  Below 50         F

### 6. Pass/Fail Calculation

The notebook creates a `Pass_Fail` result for each student using the
subject marks and attendance condition implemented in the code.

The resulting analysis contains both `Pass` and `Fail` students.

### 7. Student Performance Analysis

The notebook performs the following analysis:

-   Finds the student with the highest average.
-   Finds the highest average score.
-   Calculates the average marks for Maths, Physics and Chemistry.
-   Identifies the subject with the best average.
-   Counts the number of passed students.
-   Counts the number of failed students.

## Output from the Current Notebook Run

The executed notebook produces the following analysis:

-   **Top Student:** Naveen
-   **Highest Average:** 97.66666666666667
-   **Maths Average:** 77.20
-   **Physics Average:** 73.10
-   **Chemistry Average:** 75.35
-   **Best Performing Subject:** Maths
-   **Best Subject Average:** 77.2
-   **Passed Students:** 13
-   **Failed Students:** 7

The calculated student-performance table contains:

-   `Student_ID`
-   `Name`
-   `Total`
-   `Average`
-   `Grade`
-   `Pass_Fail`

## Sample Result

    Student ID Name        Total   Average Grade   Result
  ------------ --------- ------- --------- ------- --------
           201 Naveen        293     97.67 A+      Pass
           202 Nithin        258     86.00 A       Pass
           203 Aryan         274     91.33 A+      Pass
           204 Abhinav       235     78.33 B       Pass
           205 Rajesh        251     83.67 A       Pass

## Main Pandas Operations Used

The notebook uses Pandas for:

-   Reading the CSV dataset.
-   Creating and working with a DataFrame.
-   Selecting subject columns.
-   Calculating column-wise totals and averages.
-   Finding maximum values.
-   Calculating subject-wise averages.
-   Counting pass/fail results.
-   Selecting the student associated with the highest average.

## NumPy Usage

NumPy is included in the notebook for numerical/data-analysis operations
used during the processing of student performance data.

## Running the Project

1.  Open `Student_Performance_Analytics_System.ipynb` in Google Colab or
    Jupyter Notebook.
2.  Make sure `Students_Records.csv` is available.
3.  Run the notebook cells in order.
4.  Upload `Students_Records.csv` when the upload cell is executed.
5.  Run the data-reading and processing cells.
6.  View the final student performance table and analysis results.

## Project Files

``` text
Student_Performance_Analytics_System.ipynb
Students_Records.csv
README.md
```

## Result

The notebook successfully processes the student records and generates
individual student performance information along with overall class
analysis. It provides total marks, average marks, grades, pass/fail
results, subject averages, the top student, and pass/fail counts.
