# Visited Countries App
This project allows users to mark the countries they have visited by inputting the country name, which gets loaded into a PostgreSQL database. The server fetches the data from the database and displays the visited countries on the web interface.

# Prerequisites
Before you begin, ensure you have the following installed:

Node.js
PostgreSQL
pgAdmin (optional, for database visualization)

# Getting Started
1. Clone the repository
2. npm install
3. Set up PostgreSQL database
4. 
   CREATE DATABASE world;
   Connect to the world database and create the necessary tables:
   Inside the world database you can import the countries.csv file so you get all the information for the countries table.
   You will also need another table called visited_countries where we will set the id and the country code of the visited countries.

   CREATE TABLE visited_countries (
    id SERIAL PRIMARY KEY,
    country_code VARCHAR(3)
   )

5. Configure database connection
Ensure your database connection details in your index.js file match your PostgreSQL setup:

        const db = new pg.Client({

          user: "postgres",
    
          host: "localhost",
    
          database: "world",
    
          password: "yourpassword",
    
          port: 5432,  
  
        });

Port 5432 is set by default, if you have another port selected for postgreSQL change it to your desired port.

Start the application on node using node index.js


# Usage
Mark a country as visited:
Enter the name of the country you have visited in the input field and submit. The country will be added to your list of visited countries.

# View visited countries:
The homepage displays all the countries you have marked as visited along with the total count.

![image](https://github.com/Joelft94/visited-countries/assets/107083554/e5ac98d1-c1b0-415f-8560-066c79fb4020)

