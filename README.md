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

###1. Data Cleaning

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

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
