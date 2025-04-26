# Immigration Detention Facilities Data Analysis

This repository contains code and data analysis focusing on cleaning, analyzing, and visualizing immigration detention facilities data in the United States.

## Project Overview

This project processes a messy dataset of immigration detention facilities to identify and visualize the top 10 largest facilities by total population. The workflow includes:

1. Data cleaning (handling missing values, fixing formatting issues)
2. Data analysis (creating a Total Population column and finding top facilities)
3. Data visualization (creating and saving bar charts of the top facilities)

## Repository Structure

```
data-screening-exercise/
│
├── src/
│   ├── data-cleaning-script.ipynb      # Jupyter notebook for data cleaning
│   └── data-analysis-visualization-script.ipynb  # Jupyter notebook for analysis & visualization
│
├── cleaned_ice_detention.csv           # Cleaned dataset
├── messy_ice_detention.csv             # Original messy dataset
├── requirements.txt                    # Project dependencies
├── RR-Data Processing and Analysis Exercise.pdf  # Exercise instructions
├── top_10_detention_facilities.png     # Main visualization of top facilities
└── top_10_states_population.png        # Additional visualization by state
```

## Requirements

Dependencies are listed in `requirements.txt`. Install them using:

```bash
pip install -r requirements.txt
```

## How to Execute

1. Clone this repository:
```bash
git clone https://github.com/Nandansingh007/data-screening-exercise.git
cd data-screening-exercise
```

2. Set up a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Run the Jupyter notebooks in sequence:
   - First run `src/data-cleaning-script.ipynb` to clean the messy dataset
   - Then run `src/data-analysis-visualization-script.ipynb` to analyze and visualize the data

## Data Cleaning Process

The data cleaning notebook (`data-cleaning-script.ipynb`) performs the following operations:
- Removes header rows from the messy dataset
- Fixes formatting issues in facility names and locations
- Adding State value where there is null according to the City Name
- Handles missing dates in the "Last Inspection End Date" column and replacing null date values with the default value
- Ensures proper data types for all columns
- Saves the cleaned data to `cleaned_ice_detention.csv`

## Analysis and Visualization

The analysis notebook (`data-analysis-visualization-script.ipynb`) performs:
1. Loading of the cleaned data
2. Creation of a "Total Population" column by summing Levels A through D
3. Identification of the top 10 largest detention facilities
4. Generation of visualizations:
   - `top_10_detention_facilities.png`: Bar chart of the top 10 facilities by total population
   - `top_10_states_population.png`: Additional visualization showing population by state

## Visualization Interpretation

The main visualization (`top_10_detention_facilities.png`) shows the top 10 detention facilities ranked by total population. Each bar represents a facility, with longer bars indicating larger populations.

The state-based visualization (`top_10_states_population.png`) provides an overview of which states have the highest detention populations, offering a geographic perspective on the data.

## Resources Used

- Pandas and NumPy for data manipulation
- Matplotlib and Seaborn for data visualization
- Use Geolocator library to find state by the city Name
- Jupyter notebooks for interactive development
