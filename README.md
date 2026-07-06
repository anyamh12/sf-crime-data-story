# Crime reports across San Francisco in 2025

Crime data can help communities, researchers, and city officials understand where public safety resources may be needed. However, crime statistics should always be interpreted carefully because reported crime is not the same as actual crime. Many incidents are never reported, and neighborhoods with more visitors or businesses may naturally have higher number of reports. 
  
This project examines police incident reports from 2025 in San Francisco to answer two questions:
1. Which neighborhoods had the highest number of reported incidents?
2. Did the number of reported incidents change throughout the year?

The analysis was completed using Google Sheets pivot tables and charts. 

## Original Source of Data
The dataset is published through the San Francisco Open Data Portal: Public Safety, which is maintained by the City and County of San Francisco. 

Dataset: San Francisco Police Department(SFPD): 2018-Present

### Why was this  data collected?
The San Francisco Police Department records incidents that officers respond to or document. The data is made publicly available to improve transparency and allow researchers, journalists, and residents to better understand crime trends throughout the city. 

### Is this source trustworthy?
Because the data comes directly from the San Francisco Police Department and is distributed through the city's official Open Data Portal, it is considered a reliable government source. However, like any dataset, it has limitations. It only includes crimes that were reported or recorded by police and may contain reporting delays or updates after publication. 

## Data Cleaning and Analysis
The original dataset contained 1,043,833 police reports covering the years 2018-2025. 
To focus the analysis:
* The file was too large, in order to create the dataset used, I filtered the dataset on the website to include only 2025 incidents in the CSV
* After importing the data into Google Sheets, data cleanup was used to trim whitespace
* Created pivot tables
* Removed blank cells 

## Findings

### Chart 1: Reported Incidents by Neighborhood (2025)

<img width="600" height="371" alt="Chart1-neighborhoods" src="https://github.com/user-attachments/assets/252973ba-7dfb-4e0b-8ccd-7ee033d22c9d" />


**Figure 1.** Number of reported police incidents by neighborhood in San Francisco during 2025. The Tenderloin, South of Market, and Mission neighborhoods reported the highest numbers of incidents. 

Several neighborhoods reported substantially more incidents than others. The Tenderloin (12,432 incidents) had the largest number of reported police incidents during 2025, followed closely by South of Market (SoMa) (11,916 incidents) and the Mission District (11,547 incidents). These neighborhoods contain dense residential areas, businesses, entertainment districts, public transportation hubs, and high number of visitors. Higher numbers of reported incidents do not necessarily mean these neighborhoods are the "most dangerous." They may reflect higher population density, more opportunities for reporting, and greater police presence. 

### Chart 2: Reported Incidents by Month

<img width="600" height="371" alt="Chart2-monthly" src="https://github.com/user-attachments/assets/f8e0798f-bf47-4622-b77f-650e70a3a27d" />

**Figure 2.** Monthly reported police incidents during 2025. Incident totals remained relatively consistent throughout the year.

Crime reports remained relatively stable across the year, with monthly totals varying only modestly. January recorded the largest number of reported incidents, while June and December had the fewest in this dataset. The consistency suggests that reported crime in San Francisco did not fluctuate dramatically from  month to month during 2025, although additional years would be needed to determine whether these patterns are typical. 

## Methods 

This project was completed using Google Sheets 
The analysis included:
* Filtering the dataset to 2025
* Created pivot tables
* In the 'Rows' section, *'the analysis neighborhood'* column was selected in descending order and sorted by COUNTA of Incident Reports
* In the 'Values' section, *'Incident Reports'* column was inputted and summarized by COUNTA
* the number of incidents by neighborhood
* Since the original dataset did not include an "Incident Month" header, it was created in the next open column, I used '=TEXT(C2,"MMM")' which input the months the crime was committed from the "Incident Date" Column.
* Inputted *'Incident Months'* in the 'Rows' section, ordered by descending and sorted by COUNTA of Incident Number
* In the 'Values' section, *'Incident Number'* was summarized by COUNTA

The charts summarize large amounts of information in a way that is easier to understand than reading thousands of individual records. 

## Limitations 

Although this dataset is extensive, several important limitations should be considered. 

* Google Sheets and Excel could not handle the large file for the amount of police reports, as it spanned over multiple years, leading to 2025 being the main focus. 
* It only includes crimes that were reported to or recorded by the San Francisco Police Department. 
* Some Crimes go unreported.
* Reports may later be updated or reclassified.
* Neighborhoods differ greatly in population size, tourism, and commercial activity making direct comparisons difficult. 
* Incident counts do not measure crime rates because they are not adjusted for the population.

Because of these limitations, the results should not be interpreted as ranking neighborhoods by overall safety. 

## Ethical Considerations

Crime statistics can unintentionally reinforce stereotypes about neighborhoods if presented without proper context. Areas with higher numbers of reported incidents often have larger populations, more visitors, or more businesses, all of which increase opportunities for police reports

Responsible reporting should avoid labeling communities as dangerous based solely on incident totals. A more complete story would include interviews with residents, police officials, criminologist, and a population-adjusted crime rate trend.

Presenting data responsibly helps ensure that readers understand both what the data shows and what it cannot show. 

## Conclusion 

This project explored police incident reports across San Francisco during 2025 using publicly available data from the San Francisco Police Department. The analysis found that the Tenderloin, South of Market, and Mission District neighborhoods recorded the highest numbers of reported incidents. Monthly totals remained relatively consistent throughout the year, with January reporting the most incidents. 

While these findings reveal where police reports were most frequently recorded, they do not measure the actual amount of crime occurring in each neighborhood or explain why differences exist. Population density, tourism, reporting, and police activity all influence the number of reported incidents. 

Future reporting could strengthen this analysis by comparing multiple years, examining specific crime categories, calculating crime rates per capita, and incorporating interviews with community members and public safety officials. By combining quantitative data with additional reporting, journalist can produce a more accurate and balanced understanding of public safety in San Francisco. 

## Google Sheets
https://docs.google.com/spreadsheets/d/1YbOJusujAC4s1IK707KJ6wSdVIFvqdo1qjo9JLYMBBc/edit?usp=sharing

## Data Source
San Francisco Police Department Incident Reports (2018–Present)
https://data.sfgov.org/Public-Safety/Police-Department-Incident-Reports-2018-to-Pres/wg3w-h783
