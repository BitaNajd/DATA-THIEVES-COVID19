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
We would suggest to see higher no. of deaths in less development countries. If there is no obvious correlation a deeper analysis of single aspect must be done.

## Dataset
API - connection: EUROSTAT (Statistical Office of the European Union)
https://ec.europa.eu/eurostat/web/json-and-unicode-web-services/getting-started/rest-request

API - download of json-files: WHO (World Health Organization)
https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest#81415d42-eb53-4a85-8484-42d2349debfe

File download of csv-files: Robert-Koch-Institut
https://npgeo-corona-npgeo-de.hub.arcgis.com/datasets/dd4580c810204019a7b8eb3e0b329dd6_0

File download: Human development index (HDI) 
http://hdr.undp.org/en/content/human-development-index-hdi


## Database
What is the structure of your database? Have you created more than one table and if yes, how are they related to each other?
---> SQL

## Workflow
We started the project with a proper initial project execution planning using a Mind Map, Kanban board, time schedule as well as assigning different main roles (Project Manager, MySQL specialist, Pyhton/Plotting Specialist). Although having these roles, every disciplines supported each other as often as necessary for a common understanding and skill sharpening. 
Then, data from different sources for further inspection were collected and processed in parallel in MySQL and Python. This approach was necessary due to the huge amount of data availabe for which MySQL with its User Interface allowed a better initial data inspection. Processing the data to generate plots was then done in Python with the Matplotlib Libary.  

## Organization
It is beneficial to have all project management topics in one document, therefore we used a MIRO Whiteboard incl. a Kanban board, Mind map and time schedule.

What does your repository look like? Explain your folder and file structure.

-- 1x folder Data
-- 1x folder Jupyter Notebook with 1 joined Notebook
-- 1x folder with Presentation and MIRO board, both as PDF. The MIRO board export resolution is unfortunately very low due to the "free user" account.

## Links
Include links to your repository, slides and kanban board. Feel free to include any other links associated with your project.

[Repository](https://github.com/)  


