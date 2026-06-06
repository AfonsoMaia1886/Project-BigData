# Big Data Management and Modelling - Airbnb Database Analysis

This Big Data consulting project analyzes an Airbnb database to optimize business intelligence queries. We leveraged Docker to deploy a local MongoDB instance, using Python and aggregation pipelines to efficiently process, clean, and extract insights on pricing and hosts from complex housing data.

## 📂 Project Structure

- **`BDMM_23.ipynb`**: The main Python notebook (Jupyter Notebook) used to solve the various components of the project. It includes establishing connections to the MongoDB database (using the `pymongo` library), importing and reshaping data, building *aggregation pipelines*, and optimizing queries.
- **`BDMM_HW_Database.agz`**: The archive / backup file (BSON mongodump) containing the raw database. This file must be imported into your MongoDB instance to restore the `listingsAndReviews_HW2` collection.
- **`BDMM_PartD_20250464.pdf`**: The individual report/document for **Part D: Host Performance Expert**, prepared by team member Afonso Maia (20250464).

## 🚀 Setup and Execution

1. **Prerequisites**:
   - [Docker](https://www.docker.com/) installed and running.
   - [Studio3T](https://studio3t.com/) installed for database management.
   - Python environment with Jupyter Notebook and libraries such as `pymongo` and `pandas` installed.

2. **Start MongoDB via Docker**:
   In the terminal (Command Prompt or PowerShell), start a new MongoDB container using the default credentials:
   ```bash
   docker run --name mongodbHW -d -e MONGO_INITDB_ROOT_USERNAME=AzureDiamond -e MONGO_INITDB_ROOT_PASSWORD=hunter2 -p 27017:27017 mongo
   ```

3. **Import Data to MongoDB**:
   - Open **Studio3T** and create a new connection with the following URI: `mongodb://AzureDiamond:hunter2@localhost:27017`
   - Test the connection and Connect.
   - Click **Import**, select the **BSON mongodump archive** format, and point to the `BDMM_HW_Database.agz` file.
   - Click Run to load the database.

4. **Run the Analysis**:
   - Open the `BDMM_23.ipynb` notebook and run the cells. The initial code will automatically connect to MongoDB and start auditing the imported database.

## 👥 Team Members

This project was divided by analytical specializations. The members of Group 23 and their roles are:
- **Part C:** Rodrigo Gonçalves (20250529) - *Comfort Analytics Expert*
- **Part D:** Afonso Maia (20250464) - *Host Performance Expert*
- **Part E:** Francisco Graça (20250471) - *Property Features Expert*
