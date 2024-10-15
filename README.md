# Azure-Data-Ingestion-Pipeline

This Repo demonstrates a data pipeline that ingests data from a CSV file, and stores it to Azure SQL Database.

## Steps to Implement this Repo

1. **Set Up Azure Account**
   - Sign up for a free Azure account if you don't already have one.

2. **Create Azure Resources**
   - **Azure Storage Account**: To store the CSV file.
   - **Azure Data Factory**: To create the data pipeline.
   - **Azure SQL Database**: To store the transformed data.

3. **Prepare the Data**
   - Create a sample CSV file named `sample_data.csv` with the following content:
     ```csv
     Id,Name,Age
     1,John Doe,30
     2,Jane Smith,25
     3,Emily Davis,40
     ```

4. **Upload the CSV File**
   - Upload `sample_data.csv` to your Azure Storage Account.

5. **Create a Data Pipeline in Azure Data Factory**
   - Create a new pipeline in Azure Data Factory:
     - **Linked Service**: Connect to your Azure Storage Account.
     - **Linked Service**: Connect to your Azure SQL Database.
     - Add a **Copy Data** activity to copy data from the CSV file to the SQL Database.

6. **Create the Azure SQL Database Table**
   - In your Azure SQL Database, define a table with the following SQL:
     ```sql
     CREATE TABLE Users (
         Id INT PRIMARY KEY,
         Name NVARCHAR(100),
         Age INT
     );
     ```

7. **Run the Pipeline**
   - Trigger the pipeline to ingest and transform the data from the CSV file into the SQL Database.
   - Additional schedule triggers can also be added to automate the pipeline execution

