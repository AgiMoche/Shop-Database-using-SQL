Shop Database using sql (200)
For raw project instructions see: http://syllabus.africacode.net/sql/shop-project/

## Project Setup

### 1. "src" Folder:
This folder contains the four SQL script files required for the project:
1. **create-database.sql**
- Contains the SQL script that creates the database used for the project
2. **create-tables.sql**
- Contains the SQL script that creates the tables used in the database
3. **populate-table.sql**
- Contains the SQL script that fills the tables with the relevant data
4. **queries.sql**
- Contains the answers to the questions that required the database to be queried
  
### 2. Key links:
In the _creates-table.sql_, there are two tables that have key links to other tables in the database
1. The _payments_ table:
- The "customer_id" column is linked to the "id" column of the _customers_ table
2. The _orders_ table:
- The "product_id" column is linked to the "id" column of the _products_ table
- The "payment_id" column is linked to the "id" column of the _payments_ table
- The "fulfilled_by_employee_id" column is linked to the "id" column of the _employees_ table

### 3. Table information:
1. **Customers table**:
- This table contains the biographical information of the customers in the shop database with each category in its own column. The biographical information is
their first and last name, gender, address, phone number, email, city, and country. Additionally, it has an ID column which is a column with unique identifiers.
2. **Employees table**:
- This table contains information of the employees in the shop database with each category in its own column. The information is their first and last name, email
and job title. Additionally, it has an ID column which is a column with unique identifiers.
3. **Orders table**:
This table contains the information of orders made in the shop database with each category in its own column. The following information is in the table:
- The "id" column which is the column with unique identifiers
- The "product_id" column which is linked to the "product_id" column of the Products table
- The "payment_id" column which is linked to the "payment_id" column of the Payments table
- The "fulfilled_by_employee_id" column which is linked to the "employee_id" column of the Employee table
- The "date_required" column
- The "date_shipped" column which contains the date for when the order was shipped
- The "status" column which indicates the shipping status of the product
4. **Payments table**:
This table contains the information of payments made in the shop database with each category in its own column. The following information is in the table:
- The "id" column which is the column with unique identifiers
- The "customer_id" column which is linked to the "customer_id" column of the Customers table
- The "payment_date" column which contains the date for when payment was made 
- The "amount" column which contains the amount for the payment made in South African Rands
5. **Products table**:
This table contains the information of products offered in the shop database with each category in its own column. The following information is in the table:
- The "id" column which is the column with unique identifiers
- The "product_name" column which contains the name of the product being offered
- The "description" column which contains a description of the corresponding product being offered
- The "buy_price" column which contains the price at which the product being offered is being sold

### 4. Running project:
1. Launch Docker
2. Once Docker is launched, open the Command Prompt or Windows Terminal
3. Clone the GitHub repository containing the Shop Database SQL folders using the following command:
```
git clone https://github.com/Umuzi-org/Oageng-Moche-200-sql-
```
4. Navigate to the folder where the project repository was cloned using the Command Prompt or Windows Terminal
5. Navigate to the repository path using the following command:
```
cd Oageng-Moche-200-sql-
```
6. Use the following command to run the YAML file associated with the Shop Database SQL folders:
```
docker-compose up
```
7. Once the command is done running, all the relevant tables and queries will be displayed in the Command Prompt or Windows Terminal

### 5. Completing the operations:
1. Once the operations have been completed, go to Docker and stop/shut down the operation 
2. When the operation has been stopped/shut down, remove the containers and networks associated with the project by running the following command in the Command Prompt or Windows Terminal:
```
docker-compose down
```
