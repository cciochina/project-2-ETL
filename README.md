# project-2-ETL
## Project Report:

**Project Proposal**
For this project we had to find some sources of data and use our knowlege with pandas, sql and python libraries to do some cleaning and reconstruct tables to contain only the information we need.
My idea was to find information about Formula1 racing, I wanted to find the best drivers and car manufactures for every year since the begining of race wich was 1950 up to 2017.
I had a lot of information and because multiple drivers had a multiple races, I had to combine all the points together for each driver and also I had to group this information for each year.
At the end I was able to look at every year and see who obtain the podium for each year.

> **_Extract_**:

I chose my original data sources from www.kaggle.com.
Some of the data was `sqlite` and some was `csv` format. You can find all  the data in Resources folder.


> **_Transform_**:

I did my transformation in two parts:
1. Using the sqlite data resources. 
  - Create an engine to import the data from the sqlite data base
  - Select the tables which I was intersted in.
  - Convert the tables in DataFrame format.
  - I merged them.
  - I looked at the best three drivers who had the most points for each year:
      - Group by year and driver ID, and take the the surname, forname and nationality,
      - take the sum of drivers points of that year,
      - then after sorting them, take the first 3 places    
2. Using the csv data resources:
  - I used the same methods to transform the data as I did with sqite above using the csv files
  - Here I looked at constructors instead of drivers

> **_Load_**: 

 - At the end I place everything in one single table that containd the drivers who obtain the podium for the each year and the total points that they got for that year.
 - I also created a similar table about the cars manufactures.
 - I connected jypiter notebook with pgAdmin and created the SQL data base.
 - I aslo checked if the data base was created and it worked well.
