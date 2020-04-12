<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# DATA-THIEVES-COVID19 - RESEARCH
- Bita Najd
- Jens Kleiber
- Thomas Bentler

Ironhack Data Analytics Berlin March 2020 - Project Week 3


## Content
- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Dataset](#dataset)
- [Database](#database)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
As students of the Data Analytics Bootcamp of the cohort 03/2020 the project “Data Thief” has the goal to apply all acquired skills of the first module. The task consists of choosing a topic and find all the relevant data by connecting to an API, finding a dataset or scraping data from the web. These data then must be organized, cleaned, analyzed and presented.
Due to the actual worldwide spread of the Coronavirus we investigated correlations between socio-economic aspects and no. of deaths.


## Questions & Hypotheses
Our main question is: Are there correlations between socio-economic topics and deaths caused by Corona virus in Europe?
We would suggest to see higher no. of deaths in less developped countries. If there is no obvious correlation a deeper analysis of single aspect must be done. 
We looked at the following indices:
 
    - Human Development Index per country
    - Number of practicing physicians per 100.000 inhabitants per country
    - Public Health care spending in Euro per capita per country
    - Pre-Corona death rate per 100.000 inhabitants for pneumonia per country
    - Pre-Corona death rate per 100.000 inhabitants for chronic diseases per country
    - Population density as population per square kilometer per country
    - Gross domestic product in Euro per Head per country
    - Total annual number of nights spent in hotels per country
    - Total annual number of air passengers per country


## Dataset
API - connection: EUROSTAT (Statistical Office of the European Union)
https://ec.europa.eu/eurostat/web/json-and-unicode-web-services/getting-started/rest-request

API - download of json-files: WHO (World Health Organization)
https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest#81415d42-eb53-4a85-8484-42d2349debfe

File download of csv-files: Robert-Koch-Institut
https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/dd4580c810204019a7b8eb3e0b329dd6_0

File download: Human development index (HDI) 
http://hdr.undp.org/en/content/human-development-index-hdi

Kaggle - Novel Corona Virus 2019 Dataset
https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset

## Database
While we investigated many differnt data sources, we mainly used a local MySQL database as a central data repository to join together data we collected from just two major sources, the WHO and the statistical office of the European Union, Eurostat. From the WHO we collected the number of confirmed SARS CoV2 infections, number of Covid19 deaths and number of recovered for the latest date we had access to at this time, which was April7, 2020. While are aware that this is a simplified approach and other considerations would lead to a different choice of datapoints, also to serve as a proof of concept we used this data from this date as a snapshot to compare the socio-economic statstical data from Eurostat with. From Eurostat we collected the data as stated above in Questions & Hypotheses. We created a new MySQL Scheme 'newcovid'. Through data collections via the institutions API and ensuing conversions from 'JSON stat' to pandas dataframe to csv we imported the data into SQL format. We checked for integrity and adaequacy of the datatypes used: Text, Int and Double. The main data from these Eurostat tables were extracted and joined into a new SQL master table on the name of the respective country, misleadingly called 'geo' in Eurostat format. We then joined WHO data as described in this same paragraph above on the name of the country into the new master table. In this new master table, we compared WHO data with Eurostats data at a glance, we looked at possible correlations and exported subsets as csv files. These then we transformed to panda dataframe as a prerequisite for matlib plot.


## Workflow
We started the project with a proper initial project execution planning using a Mind Map, Kanban board, time schedule as well as assigning different main roles (Project Manager, MySQL specialist, Pyhton/Plotting Specialist). Although having these roles, every disciplines supported each other as often as necessary for a common understanding and skill sharpening. 
Then, data from different sources for further inspection were collected and processed in parallel in MySQL and Python. This approach was necessary due to the huge amount of data availabe for which MySQL with its User Interface allowed a better initial data inspection. Processing the data to generate plots was then done in Python with the Matplotlib Libary. 

We set up a project repository on github and while sharing all data we each were colecting, agreed for the explorative part of the project to seperately work in each one's personal folder in the 'WiP', work in progress section of the repository, before combining our work in one central notebook and consolidating all data in one central data structure on the repository.

## Organization
It is beneficial to have all project management topics in one document, therefore we used a MIRO Whiteboard incl. a Kanban board, Mind map and time schedule.

What does your repository look like? Explain your folder and file structure.

-- 1x folder Data
-- 1x folder Jupyter Notebook with 1 joined Notebook
-- 1x folder with Presentation as PDF. 

## Links
Include links to your repository, slides and kanban board. Feel free to include any other links associated with your project.

[Repository](https://github.com/)  


