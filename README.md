# World Cup Database 🏆

This repository contains my solution for the World Cup Database project, a core requirement for the freeCodeCamp Relational Database Certification. The goal was to build a database from scratch and automate data processing using Bash and SQL.

## 🛠 Project Components
Based on the project requirements, I have implemented:
- **worldcup.sql**: A complete PostgreSQL database dump including schemas for teams and games tables.
- **insert_data.sh**: A Bash script that automates the migration of data from games.csv into the PostgreSQL database. It handles duplicate entries and links team IDs correctly.
- **queries.sh**: A script containing advanced SQL queries (JOINs, Aggregate functions) to provide statistical analysis of World Cup history.

## 📋 Database Structure
The database consists of two mainteams1. **teams**: Stores unique names of all participating cogames2. **games**: Stores match details, linking to the teams table via winner_id and opponent_id foreign keys.

## 🚀 How to Run the Project

### 1. Rebuild the Database
First, restore the database structure using the SQL dump:
```bash
psql -U postgres < worldcup.sql
```
### 2.Import Data from CSV
​Run the insertion script to populate the tables (it uses TRUNCATE to ensure a clean start):
chmod +x insert_data.sh
 ```bash
 ./insert_data.sh
```

### 3.Run Statistical Queries
​Execute the query script to see the results of the analysis:
 ```bash
chmod +x queries.sh
```
 ```bash
./queries.sh
```

## 📊 Key Statistics Generated
The queries.sh script answers questions such as:
- Total and average goals scored by winning teams.
- List of unique winning teams in the entire dataset.
- Champions of each year.
- Teams that played in specific rounds (e.g., Eighth-Final 2014).

---
*Completed as part of the freeCodeCamp Relational Database Curriculum.*
