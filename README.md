# LMAS INTAKE TO INCOME ANALYSIS PROJECT



## Instructions to run

The data is either included or pulled from an API in the project.

Census API does not require a key as long as you have less than 500 requests in a day from your IP address.

### Setup python environment

```python
bash
git clone https://github.com/CosmicIdes/LMAS_intake_to_income_analysis.git
cd LMAS_intake_to_income_analysis
```

Python environment:
```bash
python-m venv venv
```

Activate environment:
mac/linux
```bash
source venv/bin/active
```

windows/cmd
'''cmd
venv/Scripts/Activate
```

### Install modules/libraries 

```bash
python -m pip install -r requirements.txt
```

Run and review [census_income_data notebook](Notebooks/census_income_data.ipynb)

Run and review [lmas_intake_data notebook](Notebooks/lmas_intake_data.ipynb)

Run and review [comparison_nb notebook](Notebooks/comparison_nb.ipynb)


## Background info
This project examines the relationship between income levels in different parts of the Louisville Metro, KY area and the intake/outcome data of the local city/county animal shelter, Louisville Metro Animal Services (LMAS). The goal is to determine whether lower level income results in more lost, abandoned, or confiscated animals.The findings could help Louisville Metro Animal Services with decisions on policies and outreach to reduce the likelihood of an animal being lost, abandoned, or confiscated. 

To retrieve more up-to-date data, visit Louisville Metro's Open Data Portal [here](https://data.louisvilleky.gov/datasets/733145c30ad94d43bdc6aba7fd0fdb09_0/explore).


## Summary
In this project, I did some cleanup and EDA, before diving in and creating a few charts:

### In the lmas_intake_data notebook:
* Return and Adoption Rates at LMAS
    * This series of charts explores what the return and adoption rates are, and how they relate to each other.

* Return Reasons
    * A sunburst chart that displays the various reasons an animal was returned to LMAS. I ran this only on animals that had more than one entry.

* Intake According to Season
    * This heatmap displays what seasons animals are more likely to be taken into LMAS. It does not explore reasons, but seems like a good diving-off point for future analysis.

### In the census_income_data notebook:
* Median Income by Zip Code (2021 - 2024 years, separate chart for each year)
    * This geopandas map displays the income levels using a color gradient, giving a good idea of where income is concentrated in Louisville.

### In the comparison_nb notebook:
* Occurences of Animals Turned in to Louisville Metro Animal Services (LMAS) by Zip Code, all years
    * Bar chat highlighting the zip code with the most intake occurences.
* Zip Codes for Louisville Metro, KY
    * A return of the geopandas map to give a visual on where zip codes are located.
* 2024 Median Income by Zip Code (color) and Occurence of Strays (size)
    * A geopandas map with bubbles, visualizing occurence of strays to median income level.