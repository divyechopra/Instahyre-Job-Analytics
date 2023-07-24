# Project Name : Instahyre Job Analytic

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

- *Company Table:*: 

Column Name         | Description
--------------------|-------------------------------------------------
Company ID          | Primary key for Company table
Name                | Name of the company posting the job listings
Founded             | Founded year of the company
Employees           | Total number of employees in the company


- *Details Table:*:

Column Name           | Description
----------------------|--------------------------------------------------
DetailID            | Unique identifier for each set of additional details
Skills              | Skills or qualifications required for the job
Involvement         | The nature of involvement in the job
Exp                 | Year of experience needed for the job
HR                  | Name of HR who posted the job

## Methodology

The following methodology was used to accomplish the project objectives:

1. *Data Scraping:* The job data was scraped from Instahyre using the Python library BeautifulSoup. The data was scraped based on specific search criteria, such as job titles, job locations, and company names.

2. *Data Transformation:* The scraped data was transformed into three tables, namely jobs, company, and details with the help of Power Query and Excel. The jobs table contained attributes such as job_id, company_id, location, designation, and details_id. The company table contained attributes such as company_id, name, industry, employees_count, and Instahyre_followers. The details table contained attributes such as details_id, involvement, level, total_applicants, and skills.

3. *Data Cleaning and Pre-processing:* The data cleaning process encompassed eliminating irrelevant data, addressing missing values, standardizing formats, removing duplicates, cleaning textual data, handling outliers, converting data types, checking for inconsistencies, normalizing categorical data, and validating data integrity.

4. *Dashboard Creation:* A dashboard was created using Power BI to provide an interactive visualization of the data. The dashboard included various charts and graphs to display the data in an easy-to-understand format. The charts included a skill distribution chart, a company class distribution chart, and a job location chart.

![Sample_User_interface](https://drive.google.com/uc?export=download&id=1PlrEg8wLSgjdHdEM70aSMQFMGwEZwTMg)

5. *Feature Extraction:* The NLTK library was used to gather the required skills from the job descriptions in the details table with the help of Natural Language Processing.

6. *Company Classification:* The companies were classified into four classes, namely Class1, Class2, Class3, and Class4, based on their employee count and Instahyre followers using K-Means clustering algorithm. A new column was added to the company table to represent the company class. Additionally we also evaluated it by Elbow Method and the optimum number of clusters are 4.

<p align="center">
  <img src="https://drive.google.com/uc?export=download&id=1jmAdodfremotelYI3mMF0U9-w1CT63Js" width="400">
</p>

<h5 align=center>
  Optimum number of cluster 
<h5>
   
<p align="center">
  <img src="https://drive.google.com/uc?export=download&id=1EQ-MHNLCRd2GrtK_GC1nVAeK_jD2veZk" width="400">
</p>
   
 <h5 align=center>
  3-D Scatter Plot of Clusters
 <h5>
  
 <p>&nbsp;</p>

7. *User Interface:* A search bar was created using the Flask web framework where users could search for skills. The FuzzyBuzzy library was used to correct user input errors in the search bar. Upon entering the skill, the most common experience level, industry, and company class where the skill is required, and the number of jobs available for the skill were displayed.

## Results

### 1. Key Insights from Dashboard

- Maximum No of Jobs are in Bengaluru.

- Top Hiring Industries are Information and Technology, Financial, and Education.
 
- Top 5 States which have the most jobs are Delhi, Maharashtra, Haryana, Karnataka, and Uttar Pradesh.

- Most of the Jobs are Full Time.

- Large Company which are having employees count of 1000+ having 52% volume of total Jobs

- When we are selecting Delhi we get to know that we have most of the jobs in Education Sector and then Information and Technology

- We also get to know that Education sector has 37.29% Internships.

- If we select Maharastra then we get to know that the  top industries are IT and Finance.


### 2. This is webpage that will take input from users and generate output according to searched skills.

<p>
  <img src="https://drive.google.com/uc?export=download&id=1fwhxw2c6r0E55K9SPt5cZ6wCjC8GnK5h" width="1200">
</p>


<!-- ![Sample_User_interface](https://drive.google.com/uc?export=download&id=1fwhxw2c6r0E55K9SPt5cZ6wCjC8GnK5h) -->

### 3. This is webpage that show all the listed jobs for the particular skills with some additional information.

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
