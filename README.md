# Project Name: Instahyre Job Analytics

<p align="center">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/989db426-1fbc-48da-b19e-96f48a6a4e56" alt="WhatsApp Video 2023-07-24 at 10 15 43 AM">
</p>


## Introduction

The project's objective is to gather job-related information from Instahyre using Python's Selenium library and organize it in a specified format. The collected data will then be converted into three separate tables: jobs, company, and details, utilizing the Pandas library. To enable user-friendly searches, a search bar will be implemented using the Flask web framework, allowing users to look up skills. The search results will display essential details, such as the most common experience level, industry, and company class where the skill is in demand, along with the number of available job opportunities. To enhance user experience, the FuzzyBuzzy library will be employed to correct any input errors made by users in the search bar.


<p align="center">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/2f1b7538-3774-4549-ac1b-0f88175979eb" width="385">
  <img src="https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/2fef555a-a30d-4511-890e-2d32f49e714e" width="400">
</p>

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

### 1. This is the webpage that will take input from users and generate output according to searched skills.

<p>
  <img src="https://drive.google.com/uc?export=download&id=1fwhxw2c6r0E55K9SPt5cZ6wCjC8GnK5h" width="1200">
</p>


<!-- ![Sample_User_interface](https://drive.google.com/uc?export=download&id=1fwhxw2c6r0E55K9SPt5cZ6wCjC8GnK5h) -->

### 3. This is the webpage that shows all the listed jobs for the particular skills with some additional information.

<p>
  <img src="https://drive.google.com/uc?export=download&id=1hOy90FuvOg4csqVpLOLrg37hgQE-1hii" width="1200">
</p>
<!-- ![Sample_User_interface](https://drive.google.com/uc?export=download&id=1hOy90FuvOg4csqVpLOLrg37hgQE-1hii) -->
   
## Limitation
   
- One limitation of this project is the dependency on the structure and layout of the Instahyre website. If Instahyre changes its webpage structure or adds additional security measures, it may affect the data scraping process and require adjustments to the scraping code.
- Another limitation of the project is that the accuracy and effectiveness of NLP in improving user input may vary depending on the complexity of the queries and the available training data. Ongoing research and improvements in NLP techniques can help enhance the accuracy and performance of user input correction.

## Challenges: 
   
- One of the main challenges faced in this project is implementing natural language processing (NLP) techniques to improve user input. NLP is a complex field, and incorporating it to enhance user input requires in-depth research and understanding. Overcoming the challenge of integrating NLP effectively to correct user input errors can be time-consuming and technically demanding.

- Another challenge which faced in this project was the initial difficulty in creating a webpage for user input after learning Flask from various sources. While Flask provided the necessary tools for web development, there was a learning curve involved in understanding its concepts and applying them effectively.


https://github.com/divyechopra/Instahyre-Job-Analytics/assets/122443219/d516df5b-5701-4d54-8a32-30623148e4f7


## References

- Python Software Foundation. (2022). Python Language Reference, version 3.10. Retrieved from https://docs.python.org/3/reference/index.html

- Wikipedia contributors. (2023, April 19). BeautifulSoup. In Wikipedia, The Free Encyclopedia. Retrieved 15:44, April 22, 2023, from "https://en.wikipedia.org/wiki/Beautiful_Soup_(HTML_parser)"

- Wikipedia contributors. (2023, April 13). Flask (web framework). In Wikipedia, The Free Encyclopedia. Retrieved 15:48, April 22, 2023, from "https://en.wikipedia.org/wiki/Flask_(web_framework)"

- Pandas Development Team. (n.d.). pandas 1.4.5 documentation. Retrieved April 22, 2023, from "https://pandas.pydata.org/docs/"

- Scikit-learn developers. (n.d.). Clustering. Retrieved April 22, 2023, from "https://scikit-learn.org/stable/modules/clustering.html"

- FuzzyBuzzy. (n.d.). FuzzyBuzzy Documentation. Retrieved April 22, 2023, from "https://pypi.org/project/fuzzybuzzy/"

- Microsoft Corporation. (n.d.). Power BI. Retrieved April 22, 2023, from "https://powerbi.microsoft.com/en-us/"

- Selenium with Python: https://selenium-python.readthedocs.io/
