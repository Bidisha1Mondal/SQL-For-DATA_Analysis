#MySQL Project for Data Analysis:
###Data Link:-

[SQL project.xlsx](https://github.com/user-attachments/files/19608393/SQL.project.xlsx)

###MySQL Code:-

USE college;
-- READ DATA --

SELECT * FROM mysql;

-- Total Cars:To get a count of total records --

SELECT count(*) FROM mysql;

-- The manager asked the employee how many cars will be available in 2023? --

SELECT count(*) from mysql 
WHERE year = 2023;


-- The manager asked the employee how many cars will be available in 2020,2021,2022? --

SELECT count(*) from mysql 
WHERE year IN (2020,2021,2022)
GROUP BY year;

-- Client asked me to print the total of all cars by year.I don't see all the details. --

SELECT year,count(*) from mysql
GROUP BY year; 

-- Client asked to car dealer agent how many diesel cars will there be in 2020? --

SELECT count(*) FROM mysql
WHERE year = 2020 and fuel="Diesel";

-- Client requested a car dealer agent how many petrol cars will there be in 2020? --

-- The manager told the employee to give a print all the fuel cars(petrol,diesel and CNG) come by all year. --

SELECT year,count(*) from mysql
WHERE fuel="Petrol"
GROUP BY year; 

SELECT year,count(*) from mysql
WHERE fuel="Diesel"
GROUP BY year;

SELECT year,count(*) from mysql
WHERE fuel="CNG"
GROUP BY year;

-- The manager there were more than 100 cars in a given year,which year had more than 100 cars? --

SELECT year,count(*) from mysql
GROUP BY year
HAVING count(*)>100;

-- The manager said to the employee all cars count details between 2015 and 2023 we need complete list --

SELECT count(*) FROM mysql 
WHERE year BETWEEN 2015 and 2023;

-- The manager said to the employee all cars details between 2015 and 2023 we need complete list --

SELECT * FROM mysql 
WHERE year BETWEEN 2015 and 2023;

