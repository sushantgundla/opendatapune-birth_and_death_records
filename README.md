# Open Data Hackathon - Birth and Death records
Data cleaning and analysis of the birth and death records for the Open Data Hackathon organized by PMC Open Data Portal.

Problem Statement: [opendatapune/birth_and_death_records](https://github.com/opendatapune/Problem-Statements/wiki/Birth-and-Death-records)
1. Combine various years datasets into a clean machine-readable CSV
2. Derive date-wise, month-wise, year-wise totals by gender and type (birth/death).
3. See monthly trends and year-on-year trends
4. Locate anomalies in the data
5. Compare with historical events, passing of laws like legislation on early sex determination, weather events
6. Compare between the genders
7. Create time series based visualizations, similar to stock market / currency charts.

## Getting Started

### Prerequisites

1. Install and setup Anaconda
Find a easy installation and setup guide using this [link](https://www.datacamp.com/community/tutorials/installing-anaconda-windows)
Make sure you install Anaconda for python 3.6 or above

2. Install required packages:
Open Anaconda prompt and run these commands
```
conda install pandas,numpy, matplotlib, plotly
```
Verify Installation by running
```
import pandas as pd
pd.__version__
```

3. Download the data sets:
[Dataset for birth_and_death_records](http://opendata.punecorporation.org/Citizen/CitizenDatasets/Index?categoryId=50)


## Use Cases

### 1. Converting xlsx files to pure text csv files

We have taken the input dataset ad converted it into pure text CSV format for easy cleaning process.
"xlsx_to_csv.py" is a script that will automatically convert all the original datasets stored in folder datasets to text csv format and store them in converted/datsets.

To convert the datasets:
1. Open Anaconda prompt and go to folder opendatapune-birth_and_death_records/converted_datasets.
2. Run the commands stored in conversion_commands.txt for the required conversion.
Example:
```
python xlsx_to_csv.py ../datasets/"List of Birth And Death rate for the year 2010.xlsx" 2010 birth_and_death_2010.csv
```
After running all the commands u will see that all the xlsx files are converted to csv files and a essage "Successfully completed" id shown after each conversion

### 2. Data Cleaning

The csv files are then cleaned using "Data_Cleaning_Preparation.ipynb"
Steps in cleaning:
1. Corrected miss interpreted dates to dd/mm/yyyy
2. Split the "Date of Event" and replaced it with "Day", "Month" and "Year"
3. Used one-hot-encoding technique to store "Type" and "Gender" attributed
   Note : "Type"   -> "Birth" = 0 / "Death" = 1
          "Gender" -> "Male" = 0 / "Female" = 1
4. Created Cleaned datasets from year 2010 to 2018 and stored them in folder "converted_datasets"
5. Combined data from years 2010 to 2018 into single dataset "combined_cleaned_birth_and_death_2010-2018.csv"

How to run:
1. Open Anaconda prompt
2. Go to folder "opendatapune-birth_and_death_records"
3. Type following command to open jupyter notebook
   ```
   jupyter notebook
   ```
4. Open "Data_Cleaning_Preparation.ipnyb" and run each row one by one to clean 

### 3. Data Processing

Processed the combined raw dataset to get the following information:
1. Number of male,female and total births and deaths per day
   stored in file "*Day_wise_information.csv*" in folder "Insights"
2. Number of male,female and total births and deaths per month
   stored in file "*Month_wise_information.csv*" in folder "Insights"
3. Number of male,female and total births and deaths per year
   stored in file "*Year_wise_information.csv*" in folder "Insights"
4. Male,female and total *Population Growth* per year for 
   stored in file "*Year_wise_information.csv*" in folder "Insights"

### 4. Data Visualization

Visualized the information extracted from the data through following plots:
1. Daily Birth and Death Trend 
2. Monthly Birth and Death Trend
3. Yearly Birth and Death Trend
4. Trend for Male Births
5. Trend for Female Births
6. Trend for Total Births
7. Trend for Male Deaths
8. Trend for Female Deaths
9. Trend for Total Deaths
10. Yearly population growth
11. Yearly Increase/Decrease in Birth Rate
12. Average per Month
13. Swine-flu vs road accidents deaths
14. Seasonal Decompositional analysis for Birth Trend
15. Seasonal Decompositional analysis for Death Trend

How to run:
Open Plots "*Data_Visualization.ipynb*" and run all code blocks

Where to find plots:
   - Plots can be visualized in the "*Data_Visualization.ipynb*" file
   - Plots are stored in "plots" folder in image format as well as html format.
   - Plots can be viewed online through the links provided below
   
Note: Make use of these *interactive features* of plots for Visualization.
   - Legend(top right) can be used to show or hide a particular trace/bar on the map.
   - Buttons(top left) can be used to select predifined configuration of traces/bars.
   - Hovering over the plot shows the values corresponding to x axis for all traces/bars.
   - Range slider(below x axis) can be used choose the range to display on the plot.
   - pinch to zoom in/out oprion is available
   
### 5. Analysis and Insights
1. Insights on Daily information
   stored in file "*Daily_Insights.csv*" in folder "Insights"
2. Insights on Montly information
   stored in file "*Monthly_Insights.csv*" in folder "Insights"
3. Birth and Death Records not registered in "Detected cases and deaths due to diseases" dataset
   stored in file "*Recording_differences_between_datasets.csv*" in folder "Insights"

## Built With

* [Anaconda]() - The web framework used
* []() - Dependency Management
* []() - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc

## Resources

https://www.hindustantimes.com/pune-news/why-are-we-driving-ourselves-to-death-are-the-roads-in-pune-safe/story-xr4ZCTYgiBp0TXD5Krc20M.html
https://timesofindia.indiatimes.com/city/pune/road-fatalities-highest-in-pune-mumbai-reveals-state-cid-report/articleshow/62287516.cms
https://timesofindia.indiatimes.com/city/pune/referral-cases-raise-swine-flu-death-count-in-state/articleshow/67315778.cms
