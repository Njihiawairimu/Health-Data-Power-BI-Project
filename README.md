# Health Data Dashboard
## Objective:
To create an interactive dashboard using the  `weight-height dataset` to analyse health metrics like BMI and Age distribution. 
The dataset includes fields such as `gender`, `height`, `weight` and `born_year`.
## Project Overview

### Imported data
Imported csv.file to Power BI.
### Data Cleaning
Filtered the `born_year` column to remove null values.

#### Created new columns
- Calculated BMI (Body Mass Index)
The BMI is expressed in kg/m2, resulting from mass in kilograms and height in metres. Pounds (`weight`) and inches(`height`) are used, a conversion factor of 703 (kg/m2)/(lb/in2) is applied
```DAX
BMI = (DIVIDE('weight-height-updated'[Weight],('weight-height-updated'[Height]*'weight-height-updated'[Height]))* 703)
```


