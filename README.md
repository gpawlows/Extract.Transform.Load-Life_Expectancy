## Project Title - Extract, Transform, Load - Life Expectancy 

Team Members - Parth Korat, Geoff Pawlowski, Ashutosh Sawant

## Project Description/Outline

Longer life; this is a universal goal that the world’s countries have been trying to achieve for its peoples’ since countries first came to be.  The good news is that the world has been wildly successful at extending life over the past two (2) centuries.  The more inconclusive news is that different countries have achieved varying results over time.  This is not unexpected as different countries develop at different rates.  Figure 1 is just one (1) example of how two countries can have very different life expectancy curves, relative to time.  However, with many datasets available to us at this time in history, we are hoping to take advantage of the stratification in life expectancy between countries and several other quantifiable variables.  We intend to extract this data, clean it and store it for potential analysis.  




![Life Expectancy](Images/LE.png)




## Datasets To Be Used





![Datasets](Images/Datasources.PNG)

Extract:  All datasets were extracted from the links sourced in this readme file as .csv files.  

Transform:  All .csv files were read into Jupyter Notebooks files and transformed into Pandas dataframes for cleaning.  The dataset from the UN needed additional cleaning within the .csv to convert text to columns. The years for the features had to be transformed via .replace(), so that the features and the outcome could be joined together. Later the extraneous countries had to be removed using a .notna() method so that the outcome feature had no null values. 

Data was graphed to visually inspected for outliers along with conducting anlytical box-plot outlier analysis.  There was a batch of data where decimal places were found to be moved 2 places in error after visual inspection and that was corrected.  



## Data Dictionary

id: Primary Key, Serial <br/>
country: Country identifier, VARCHAR <br/>
year: for life expectancy the year in the table represent the year of the data collection. <br/>
For any of the features the year in the table represents an average of multiple years of data, according to the following key <br/>
2019: Average of 2016-2019 data <br/>
2015: Average of 2011-2015 data <br/>
2010: Average of 2006-2010 data <br/>
2000: Average of 2000-1996 data <br/> 
expectancy: Years expected to live if survived birth, Int <br/>
birthattended: % of births attended by nurses or midwives, Decimal <br/>
gdpspend: % of Gross Domestic Product spent on all levels of education, Decimal <br/>
drinkingwater: % of households who have access to clean drinking water in their home, Decimal <br/>
handwash: % of households who have access to basic santization for handwashing in the home, Decimal <br/>
literacy: % of adults in country who are literate, Decimal <br/>
meddoctor: number of doctors per 10,0000 persons per country, # personnel/10,000 people <br/>
nursemidwives: number of nurses and midwives per 10,000 persons per countyr, # personnel/10,000 people <br/>
stuteacherration: number of students per teacher in the primary education systems (similar to class room size), #students/teacher <br/>

Database: PostgreSQL (ETLAssignment_dB)



