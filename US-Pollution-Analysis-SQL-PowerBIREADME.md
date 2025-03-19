Here's a GitHub-worthy README document for your project, including all the instructions provided so far.  

### Suggested Repo Name:  
**`US-Pollution-Analysis-SQL-PowerBI`**  

---

## **U.S. Pollution Analysis Using SQL & Power BI**  

### **Overview**  
This project analyzes real-world air pollution data from the [American Lung Association](https://www.lung.org/research/sota/city-rankings/most-polluted-cities). The goal is to create a structured SQL database to store pollution data and generate insights using SQL queries and Power BI visualizations.  

### **Data Source**  
The data is sourced from the American Lung Association's "State of the Air" report, ranking cities based on:  
- **Ozone pollution**  
- **Year-round particle pollution**  
- **Short-term particle pollution**  

---

## **Database Creation in MS SQL Server**  
To store and analyze pollution data, we first create the `pollution_data` table in MS SQL Server.  

### **Step 1: Create Database**  
```sql
CREATE DATABASE PollutionDB;
USE PollutionDB;
```

### **Step 2: Create Table**  
```sql
CREATE TABLE pollution_data (
    id INT IDENTITY(1,1) PRIMARY KEY,
    city VARCHAR(100),
    state VARCHAR(100),
    ozone_pollution_rank INT,
    year_round_particle_pollution_rank INT,
    short_term_particle_pollution_rank INT
);
```

---

## **Inserting Data**  
Manually insert real data from the American Lung Association into the table. Example:  
```sql
INSERT INTO pollution_data (city, state, ozone_pollution_rank, year_round_particle_pollution_rank, short_term_particle_pollution_rank)
VALUES ('Los Angeles', 'California', 1, 5, 7);
```
(Repeat this step for all cities in the dataset.)  

---

## **Querying the Data**  

### **Display All Pollution Data**  
```sql
SELECT * FROM pollution_data;
```

### **Top 10 Polluted Cities by Ozone Pollution**  
```sql
SELECT TOP 10 * 
FROM pollution_data 
ORDER BY ozone_pollution_rank ASC;
```

### **Top 10 Polluted Cities by Year-Round Particle Pollution**  
```sql
SELECT TOP 10 * 
FROM pollution_data 
ORDER BY year_round_particle_pollution_rank ASC;
```

### **Top 10 Polluted Cities by Short-Term Particle Pollution**  
```sql
SELECT TOP 10 * 
FROM pollution_data 
ORDER BY short_term_particle_pollution_rank ASC;
```

---

## **Power BI Visualization**  

### **Step 1: Connect Power BI to SQL Server**  
1. Open **Power BI Desktop**.  
2. Click **Get Data** → Select **SQL Server**.  
3. Enter your **Server Name** and **Database Name (PollutionDB)**.  
4. Click **Load** to import data.  

### **Step 2: Create Visualizations**  
Using Power BI, generate the following charts:  

#### **1. Top 10 Polluted Cities by Ozone**  
- **X-axis:** City  
- **Y-axis:** Ozone Pollution Rank (Ascending)  

#### **2. Top 10 Polluted Cities by Year-Round Particle Pollution**  
- **X-axis:** City  
- **Y-axis:** Year-Round Particle Pollution Rank  

#### **3. Top 10 Polluted Cities by Short-Term Particle Pollution**  
- **X-axis:** City  
- **Y-axis:** Short-Term Particle Pollution Rank  

---

## **Future Enhancements**  
- Automate data extraction from the American Lung Association  
- Include additional pollution factors (e.g., CO2 levels, NO2 emissions)  
- Develop interactive Power BI dashboards  

---

## **Contributing**  
Feel free to fork this repository, submit pull requests, and suggest improvements!  

📌 **GitHub Repository:** [Insert your GitHub Repo URL here]  

🚀 **Let's use data to drive change!** 🌎💨  

---

The pollution charts have been generated successfully. You can download the image using the link below:

[Download Pollution Charts](sandbox:/mnt/data/pollution_charts.png)
