# CPSC_368_group_12_project

## Overview
Our project focuses on identifying crucial intervention points for reducing greenhouse gas emissions in food production and waste management across four East Asian countries: China, Japan, Republic of Korea, and Mongolia. We specifically examined the change in emissions from 2000 to 2020, revealing a significant increase, with China identified as a high-emission zone. A detailed examination in China, using pie charts and heatmaps, highlighted household contributions to emissions through activities like crop residues, rice cultivation, food transport, and household consumption. Our findings suggest that reducing emissions from food transport and household consumption can significantly impact sustainable development efforts and help lower the overall carbon footprint of the food sector. This project aligns directly with climate and sustainability goals, addressing urgent environmental challenges by linking food system improvements to broader emission reduction efforts.

## Database Setup
The SQL operations for this project are executed on the UBC CS Oracle database server. The teaching team can use the following credentials to log in and perform the necessary SQL operations:

- SSH Server: remote.students.cs.ubc.ca


### SSH and SQL*Plus Login Procedure
1. Open a terminal or SSH client.
2. Connect to the UBC CS Oracle database server via SSH:
   ```sh
   ssh cyz1016@remote.students.cs.ubc.ca
   ```
3. Enter the password when prompted.
4. Once logged in, start SQL*Plus with the following command:
   ```sh
   rlwrap sqlplus ora_cyz1016@stu
   ```
5. Enter the SQL*Plus password when prompted to connect to the Oracle database.

### SQL DDL File Execution
After logging in to SQL*Plus, you may execute the DDL files provided as part of the project documentation. To run a DDL file, use the following SQL*Plus command:
   ```sql
   start cs368_assignment_5.sql
   ```

## Running the Code
Once the DDL files have been executed and the database has been populated with the required tables and data, you can proceed to run the data analysis code.

## Cleanup
In case of resetting the database environment, the following SQL commands are used to drop the tables:
```sql
DROP TABLE FOODWASTE_CAUSE_EMISSION;
DROP TABLE CO2_EMISSION_CONTRIBUTE_TOTAL_EMISSION;
DROP TABLE FOODWASTE_CONTRIBUTE_TOTAL_EMISSION;
DROP TABLE FOODWASTE;
DROP TABLE TOTAL_EMISSION_PER_COUNTRY;
DROP TABLE AGRI_FOOD_CO2_EMISSION;
```
Please note that dropping tables is irreversible and should be done with caution.

## Dependencies
Ensure that the Python environment is set up with the required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`, `oracledb`) to run the data analysis scripts.

## Running the Analysis
The analysis comprises several steps:
1. Extraction of food waste and emissions data from the database.
2. Comparison of GHG emissions between the years 2000 and 2020 for the east aisa countries.
3. Detailed analysis within China, identifying household contributions to GHG emissions.
4. Visualization of emissions data through pie charts and heatmaps.
5. Identification of significant emission sources within household activities.

## Visualization
The code generates several plots:
- Bar charts for comparing emissions over the years.
- Pie charts for distribution of food waste patterns.
- Heatmaps for correlation analysis between agricultural activities and emissions.

Ensure that the plotting libraries are correctly installed and configured to display graphics on your system.

## Closure
Remember to close the database connection after the analysis is complete using the `connection.close()` method.

