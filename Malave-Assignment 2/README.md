# Analysis of NYC SNAP Recepient data set — 09/2018 to 03/2025

## Data

This analysis uses a csv spreadsheets of the total amount of SNAP recipients in NYC divided by each borough's community district.

The spreadsheets come from the following sources:

- Human Resources Administration (HRA):
  - `Borough_Community_District_Report_20250423.csv`: Raw data of NYC SNAP recipients 

Each of the spreadsheets contain, among others, the following columns relevant to the analysis:

- `Borough Consultation Total SNAP Recipients` — Total count of SNAP benefits in the district
- `Month` — The date the data was recorded
- `Community District (CD)` —  The district of the borough

## Methodology

The notebook [`Malave_BronxSNAP_Assignment2.ipynb`](notebooks/Malave_BronxSNAP_Assignment2.ipynb) performs the following analyses:


##### Part 1: Initial Dataset Analysis

- First, I loaded my dataset and identified the length, how each column is formatted, and printed a preview of the first 5 rows.

- Afterwards, I identified the most important columns I need for my analysis, and stored it in the variable appropriately titled "columns." 


##### Part 2: Separating the Bronx from the other Boroughs

- Since my objective is to exclusively focus on SNAP Recepients in the Bronx, I had to create a new column formatted as a boolean titled "Bronx" that reads true if the column "Community District (CD)" containted the string "B"

- Then, using the new column, I created a subset of the dataset that only contained the rows that output true for "Bronx", titled "snap_data_bronx"

##### Part 3: Plotting Bronx CD1 on a line graph.

- Afterwards, I began to experiment by copying my previous code, creating a subset that excluded every community district except Bronx CD1. Now my objective was to plot the total SNAP recepients in Bronx CD1 on a line graph from 2018 to 2025.

##### Part 4: Bronx 2025 SNAP recepients
- Finally, I created one last subset of the raw data that exclusively looks at the total SNAP recepients as of March 2025, and organized it from most to least.
- This revealed that Bronx CD4 recieves the most SNAP benefits, which is also true of 2018.

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- Libaries: pandas, matplotlib
