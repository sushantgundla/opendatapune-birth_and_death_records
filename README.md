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
conda install pandas,numpy, matplotlib
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

The csv files are then cleaned using "clean.ipynb"
Steps in cleaning:
1. Corrected miss interpreted dates to dd/mm/yyyy
2. Split the "Date of Event" and replaced it with "Day", "Month" and "Year"
3. Used one-hot-encoding technique to store "Type" and "Gender" attributed
   Note : "Type"   -> "Birth" = 0 / "Death" = 1
          "Gender" -> "Male" = 0 / "Female" = 1
4. Combined data from years 2010 to 2018 into single dataset "combined_cleaned_birth_and_death_2010-2011.csv"

Open in Anaconda prompt type following command to open jupyter notebook
```
jupyter notebook
```
Then open "clean_visualize.ipnyb" and run each row one by one to clean and visualize 

### 3. Data Processing

Processed the combined raw dataset to get the following information:
1. Number of Male/female births/deaths per day
2. Number of Male/female births/deaths per month
3. Number of Male/female births/deaths per year


### 4. Visualization

Visualized the information extracted from the data through following plots:
1. Total male births vs month (per year) 
2. Total female births vs month (per year)
3. Total births vs month (per year)
4. Total male deaths vs month (per year)
5. Total female deaths vs month (per year)
6. Total deaths vs month (per year)
7. Month-wise trend of births vs years (male/female/total)
8. Month-wise trend of deaths vs years (male/female/total)
9.
10.


All the plots are stored in "Plots" folder.

### 5. Insights



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
