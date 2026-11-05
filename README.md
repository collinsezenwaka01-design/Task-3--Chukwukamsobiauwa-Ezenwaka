# Task-3--Chukwukamsobiauwa-Ezenwaka

# My Project 3: Azure Data Warehouse

This project shows how I set up a secure private database in Microsoft Azure and connected to it safely using an SSH tunnel.

## 📊 The "Frustration & Confusion" Counter
Building things in the cloud is hard! Here is the honest count of how many times I got stuck or confused before making it work:

* **Realizing I needed to build a Network first:** 4 times 🛑
* **Getting confused about file paths and keys:** 6 times 🔑
* **Looking for where MySQL Workbench was installed:** 3 times 🔍
* **Total Times Frustrated & Confused:** **13 times** 🤯
* **Seeing the green checkmark when it finally worked:** **Amazing!** 🎉

---

## 🛠️ Tools Used
* **Cloud:** Microsoft Azure
* **Database:** Azure MySQL Database
* **Network:** Azure Virtual Network (VNet) & Private Endpoint
* **SQL Client:** MySQL Workbench

---

## 📜 My SQL Code

### 1. Creating the Table
This code builds the structure to hold the information safely:
```sql
CREATE DATABASE IF NOT EXISTS Warehouse;
USE Warehouse;

CREATE TABLE Interns (
    InternID INT PRIMARY KEY,
    FirstName VARCHAR(50) NOT NULL,
    LastName VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE NOT NULL
);
```

### 2. Adding the Data
This code adds the names into our table:
```sql
INSERT INTO Interns (InternID, FirstName, LastName, Email)
VALUES 
(1, 'Jane', 'Doe', 'jane@decodelabs.com'),
(2, 'John', 'Smith', 'john@decodelabs.com'),
(3, 'Connor', 'O''Leary', 'connor@decodelabs.com');
```

### 3. Checking the Results
To make sure everything worked perfectly, I ran this final command to see the data:
```sql
SELECT * FROM Interns;
```
