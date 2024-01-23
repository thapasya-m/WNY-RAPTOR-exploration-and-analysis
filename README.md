# WNY Raptor - Exploratory Data Analysis & Statistical Testing

# Overview
This documentation contains Python codes for preprocessing, analyzing, visualizing tracking data and statistical testing of three birds: Maverick, Mo (deceased), and McDonnell. The data includes location information and timestamps, allowing us to explore the birds' movements and behavior over time.

## Part 1

## Data files
Key files located in folder `/Data/Part1-Bird_profiles_and_folium_mapping`
- `Maverick`: "WNYRWC01-7262.csv"
- `Moe`: "WNYRWC02-9422.csv"
- `McDonnell`: "LocationData-GNSS-[20230501-20231024].csv"


## Package installation

```sh
!pip install folium
```

## Instruction
1. Open Google Colab and upload the data files. 
```
from google.colab import files
uploaded = files.upload()
```
2. Select `Run all` option.
## Code Structure
The code is organized into 3 main sections, each corresponding to a different bird:

### Maverick (bird1)
- Read and filtered tracking data from the "WNYRWC01-7262.csv" file.
- Calculated and printed key information such as the minimum and maximum timestamps, duration, and days since banded.
- Generated a `folium` map showing Maverick's route with markers for the initial and final destinations.
### Mo (bird2)
- Read and filtered tracking data from the "WNYRWC02-9422.csv" file.
- Performed data cleaning by removing outliers.
- Calculated and printed key information similar to Maverick's section.
- Plotted a scatter plot of Mo's location coordinates.
- Generated a `folium` map displaying Mo's route with markers for the initial and final destinations.
### McDonnell (bird3)
- Reads and filtered tracking data from the "LocationData-GNSS-[20230501-20231024].csv" file.
- Cleaned the data by removing irrelevant information.
- Calculated and printed key information, including the duration since the first ping and days since release.
- Generated a `folium` map illustrating McDonnell's route with markers for the initial and final destinations.

## Results
- The code generates visualizations and key statistics for each bird, providing insights into their movements and tracking history.

## Part 2

## Data files
Key files are located `Part2_Exploratory_Correlation_DATA`:
- Ecotopia Data (`Part2_Exploratory_Correlation_DATA/mcdonell-LocationData.csv`)
- External Data (`Part2_Exploratory_Correlation_DATA/external-dataset/`)
    - Contains location-based weather data
- Movebank Data (`Part2_Exploratory_Correlation_DATA/MoveBankData/`)

## Installation 

```
!pip install seaborn pandas scikit-learn-extra scikit-learn 

```

**incase of installation issue, use**

```
import sys
!{sys.executable} -m install seaborn pandas scikit-learn-extra scikit-learn
```

## Code Structure

The notebook contains series of exploratory analysis done for the three raptors in our dataset.

1. [Raptor timeline](Codes/Part2_Exploratory_Correlation_analysis.ipynb#Raptor-timeline---overview)

2. [Pings by month](Codes/Part2_Exploratory_Correlation_analysis.ipynb#ping-frequency---month)

3. [Pings by season](Codes/Part2_Exploratory_Correlation_analysis.ipynb#Ping-by-Season)

4. [Pings by time of day](Codes/Part2_Exploratory_Correlation_analysis.ipynb#Ping-by-time-of-day)

5. [External Data exploration & granger causality](Codes/Part2_Exploratory_Correlation_analysis.ipynb#Method:-clustering-area-of-movement-and-merging-environmental-data)

## Part 3

## Code Content
Section 1: Import Data:
The code imports data from the provided CSV files for analysis.

Section 2: Exploratory Data Analysis:
Conducts exploratory analysis for each bird separately (Maverick, Moe, McDonnell):
Creates new features like season, time of the day, and year-month for temporal analysis.
Plots event counts by year-month for Maverick and Moe.
Generates correlation heatmaps for movement variables for Maverick and Moe.
Analyzes average movement by season and time of the day for Maverick and Moe.

Section 3:Statistical Significance Testing:
Conducts statistical tests like Kruskal-Wallis and Wilcoxon tests for each bird's movement variables (speed, heading, altitude, etc.) across different seasons or time periods.

## Usage Instructions

## Data Import
Ensure the paths to the CSV files are correctly specified or replace them with the appropriate file paths.
Exploratory Data Analysis:
Run the code sections under each bird's section (Maverick, Moe, McDonnell) to visualize their movement patterns.

## Statistical Significance Testing
Execute the code sections to conduct statistical tests on movement variables for each bird.

## Interpretation
Review statistical test results to understand if there's a significant difference in movement variables across seasons or time periods.

### Notes:
Dependencies: The code utilizes Python and several libraries such as Pandas, Matplotlib, Seaborn, and Scipy. Ensure these libraries are installed in the Python environment before running the code.

Data Preparation: The provided code assumes the CSV files contain the necessary columns for analysis. Ensure the data format matches the expected structure for the code to run correctly.
