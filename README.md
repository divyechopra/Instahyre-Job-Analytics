# Project Name: Instahyre Job Analytics

<p align="center">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/989db426-1fbc-48da-b19e-96f48a6a4e56" alt="WhatsApp Video 2023-07-24 at 10 15 43 AM">
</p>


## Introduction

The project's objective is to gather job-related information from Instahyre using Python's Selenium library and organize it in a specified format. The collected data will then be converted into three separate tables: jobs, company, and details, utilizing the Pandas library. To enable user-friendly searches, a search bar will be implemented using the Flask web framework, allowing users to look up skills. The search results will display essential details, such as the most common experience level, industry, and company class where the skill is in demand, along with the number of available job opportunities. To enhance user experience, the FuzzyBuzzy library will be employed to correct any input errors made by users in the search bar.


## Problem Aimed to Solve:

1. Automate the job search process - Save time and effort.
2. Provide comprehensive job details - Rich information for users.
3. Enhance search query accuracy - Improve search results precision.
4. Analyze job market trends - Identify employment patterns and demands.
5. Increase job matching efficiency - Connect candidates with suitable positions.


## Data Description

- *Jobs Table*:

Column Name    | Description
---------------|-----------------------------------------------------------
JobID          | Primary key for Jobs table
Designation    | The designation of the job
Industry       | Industry of the company from which the job is
Location       | Location of the job
Skills         | Skills required for the job
DetailID       | A key to map with details table, as every job has some description
CompanyID      | A key to map with company table, as one company can have multiple jobs

- *Company Table:*

Column Name         | Description
--------------------|-------------------------------------------------
Company ID          | Primary key for Company table
Name                | Name of the company posting the job listings
Founded             | Founded year of the company
Employees           | Total number of employees in the company


- *Details Table:*

Column Name           | Description
----------------------|--------------------------------------------------
DetailID              | Unique identifier for each set of additional details
Skills                | Skills or qualifications required for the job
Involvement           | The nature of involvement in the job
Exp                   | Year of experience needed for the job
HR                    | Name of HR who posted the job
 

## Methodology

The following methodology was used to accomplish the project objectives:

1. _Data Scraping:_ Job data was obtained from Instahyre using Python's Selenium library, considering specific criteria like job titles, locations, and company names.

2. _Data Conversion:_ Utilizing Pandas, the scraped data underwent transformation into three tables: jobs, company, and details.

3. _Data Cleaning and Preparation:_ The data cleaning phase involved eliminating irrelevant data, handling missing values, standardizing formats, removing duplicates, cleaning text, managing outliers, type conversion, consistency checks, categorical data normalization, and ensuring data integrity.

4. _Company Classification:_ Companies were classified into five classes (Class0 to Class4) based on employee count and company age using K-Means clustering. The optimal number of clusters was determined using the Elbow Method.

<p align="center">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/43bacef2-db64-4f2a-a307-e6e5b96cdeb6" width="400">
</p>

<h5 align=center>
  Elbow Method
</h5>
   
<p align="center">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/fa6b5ce2-5d9c-4db9-bc1c-ada96d473c3e" width="500" length="500">
</p>
 <h5 align=center>
 Scatter Plot of Clusters
 </h5>
   
5. _User-Friendly Interface:_ A Flask web framework introduced a search bar for users to look up skills. FuzzyBuzzy library corrected any input errors. Search results displayed the most common experience level, industry, company class related to the skill, and the number of available job opportunities.

## Results

### 1. This webpage is designed to accept user input.
<p align="center">
  <img width="800" alt="image" src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/0d02507f-987f-40b6-b530-e908b1bfe407">
</p>



### 2. The webpage generates output based on the skills searched by the users.

<p align = "center">
<img width="800" alt="image" src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/1fe97a0d-e5ae-4e96-936f-bec335579119">
</p>


### 3. This webpage showcases a comprehensive list of jobs related to specific skills entered by users, along with supplementary information.

<p align = "center" >
  <img width="800" alt="image" src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/92e83334-888c-45de-9c2e-7eaa58014c20">
</p>

## A short demo video of our app (Deployed on the local host server)

https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/d516df5b-5701-4d54-8a32-30623148e4f7


## Challenges:

- Creating Webpage with the help of HTML and CSS.
- User Input Text Processing and learning Fuzzy wuzzy.
- Creating a backend with Flask and returning output to a webpage.
- Understanding the different ways to deploy the model.

## References

- Python Software Foundation. (2022). Python Language Reference, version 3.10. Retrieved from https://docs.python.org/3/reference/index.html
  
- Selenium with Python: https://selenium-python.readthedocs.io/
  
- Wikipedia contributors. (2023, April 13). Flask (web framework). In Wikipedia, The Free Encyclopedia. Retrieved 15:48, April 22, 2023, from "https://en.wikipedia.org/wiki/Flask_(web_framework)"

- Scikit-learn developers. (n.d.). Clustering. Retrieved April 22, 2023, from "https://scikit-learn.org/stable/modules/clustering.html"

- FuzzyBuzzy. (n.d.). FuzzyBuzzy Documentation. Retrieved April 22, 2023, from "https://pypi.org/project/fuzzybuzzy/"


