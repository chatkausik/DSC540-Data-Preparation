### Covid 19 Data Analysis and Comparison
![image](https://user-images.githubusercontent.com/13950516/162676269-ab24f4ed-7089-44de-bc64-64c2ae6b0710.png)


### <img src="https://user-images.githubusercontent.com/13950516/162672483-4d953e53-2d6b-49d6-81ba-e7daa4a54351.png" width="40" height="40" /> &nbsp; Problem Statement:
The novel coronavirus, also known as SARS-CoV-2, is a contagious respiratory virus that first reported in Wuhan, China. On 2/11/2020, the World Health Organization designated the name COVID-19 for the disease caused by the novel coronavirus. This new strain of virus has strike fear in many countries as cities are quarantined and hospitals are overcrowded. 
This project aims at exploring COVID-19 through data analysis and visualization.


### <img src="https://user-images.githubusercontent.com/13950516/162672846-869bf047-63a7-489f-9b33-4f4a3beab1b2.png" width="40" height="40" /> &nbsp; Dataset
For this project , I have selected data from the following sources:

1.	**CSV** – The Covid 19 data is scrapped from John Hopkins University github repo : https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series , this has 

  - Daily time series summary tables, including confirmed, deaths and recovered. All data is read in from the daily case report. The time series tables are subject to be updated if inaccuracies are identified in our historical data.
  
  - Two time series tables are for the US confirmed cases and deaths, reported at the county level.
  
  - Three time series tables are for the global confirmed cases, recovered cases and deaths. Australia, Canada and China are reported at the province/state level.
  
  - Data is updated at a daily basis.

2.	**API** – I have used the api : https://services.arcgis.com/lQySeXwbBg53XWDi/arcgis/rest/services/Map/FeatureServer/0/query?where=1%3D1&outFields=*&outSR=4326&f=json <br/> <br/> which will provide the demographic info (Age, employment, sex, ethnicity etc ) for US at a County level for all the corona virus cases, this  information is vital to understand the rate of spread across communities in United States. I will use this data to deep dive into corona cases in US and generate some interesting facts.

3.	**Web** – I am scrapping data from https://www.worldometers.info / website for more insights at a world level like population, density, area and other factors.

 
The datasets 1 and 2 are related by county and country code, whereas the dataset 1 and 3 are related by Country code, this will help me join the 3 datasets into one and perform any slicing dicing for visualization.


### <img src="https://user-images.githubusercontent.com/13950516/162673345-5ea37d71-b9e4-47b7-aa6e-c43921d7b2d0.png" width="40" height="40" />&nbsp; Approach:

1. Data Gathering from Different Sources – While I had previous experience working with CSV for data gathering, I learned doing Web Scrapping using BeautifulSoup for processing HTML data. However there were a few challenges as the Web has grown organically out of many sources. It combines a ton of different technologies, styles, and personalities, and it continues to grow to this day.
<br/> <br/> Also, I learned to fetch data from Web API using requests library, Request returns а Response, a powerful object for inspecting the results of the  request. Using Response, I examined the headers and contents of the response, get a dictionary with data from JSON in the response, and also determined how successful our access to the server was by the response code from it. 

2. Data Cleaning and Transformation  - Learned how to filter, sort, merge, join two dataframes in Pandas.

3. Data Visualization  - Learned a lot of visualization libraries like matplotlib, seaborn and plotly.

4. Importing data in Sql table from Python – Mostly in my previous projects I never created any Db, added any table and queried, In this project I got a chance and learned sqllite3 to create database, I have also learned to use sqlalchemy library to create a database table and read into a dataframe.


### <img src="https://user-images.githubusercontent.com/13950516/162673481-c1ce4edf-5240-43be-ae07-e7ef061be0c6.png" width="40" height="40" />&nbsp; 

Ethical considerations:

Data can be used to drive decisions and make an impact at scale. Yet, this powerful resource comes with challenges. How can organizations/individuals ethically collect, store, and use data? What rights must be upheld? The field of data ethics explores these questions and offers five guiding principles for business professionals who handle data.

Data ethics encompasses the moral obligations of gathering, protecting, and using personally identifiable information and how it affects individuals. “Data ethics asks, ‘Is this the right thing to do?’ and ‘Can we do better?’” While we may not be the person responsible for implementing tracking code, managing a database, or writing and training a machine-learning algorithm, understanding data ethics can allow you to catch any instances of unethical data collection, storage, or use. By doing so, you can protect your customers' safety and save your organization from legal issues.

Conclusion:

In this project I touched on a lot of the technicalities of data wrangling also I understood the practical importance, Any analyses a business performs will ultimately be constrained by the data that informs them. If data is incomplete, unreliable, or faulty, then analyses will be too—diminishing the value of any insights gleaned. <br/>
Data wrangling seeks to remove that risk by ensuring data is in a reliable state before it’s analyzed and leveraged. This makes it a critical part of the analytical process. when done manually data wrangling can be time-consuming. This can be reduced by defining some policies around data—for example, requiring that data include certain information or be in a specific format before it’s uploaded to a database.


