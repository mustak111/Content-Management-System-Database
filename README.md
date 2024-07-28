# Content-Management-System-Database
Welcome to our GitHub repository for the Content Management System (CMS) Database and Binary Converter! This project provides a comprehensive database schema for building a content management system and includes a binary converter to store files in the database.

# CMS Database Schema:
The database schema comprises several tables that facilitate the organization and management of content, users, organizations, billing plans, subscriptions, and payments. Here are the tables with their respective columns

1. `Organizations` : Stores information about different organizations, including their unique `OrganizationID` and `OrganizationName`.

2. `Users` : Contains user data such as `UserID`, `OrganizationID`, `UserName`, `Password`, `Email`, `Role`, and `LastLogin`. The `OrganizationID` serves as a foreign key reference to the `Organizations` table.

3. `Content` : Manages content data with details like `ContentID`, `OrganizationID`, `Title`, `Description`, `Body`, `CreationDate`, and `UserID`. The `OrganizationID` and `UserID` fields are foreign key references to the `Organizations` and `Users` tables, respectively.

4. `Categories` : Keeps track of content categories using `CategoryID` and `CategoryName`.

5. `ContentCategories` : Forms a many-to-many relationship between content and categories using `ContentID` and `CategoryID`. It serves as a bridge table to associate content with multiple categories.

6. `ContentData` : Stores binary data related to content using `DataID`, `FileName`, `DataFile`, `FilePath`, `Extension`, `FileSize`, `ContentType`, `ContentID`, and `CategoryID`. The `ContentID` and `CategoryID` fields are foreign key references to the `Content` and `Categories` tables, respectively.

7. `BillingPlans` : Holds information about various billing plans with `PlanID`, `PlanName`, `Description`, `Features`, and `MonthlyPrice`.

8. `Subscription` : Manages subscriptions using `SubscriptionID`, `OrganizationID`, `UserID`, `PlanID`, `StartDate`, and `EndDate`. The `OrganizationID`, `UserID`, and `PlanID` fields are foreign key references to the `Organizations`, `Users`, and `BillingPlans` tables, respectively.

9. `Payments` : Tracks payment information with `PaymentID`, `SubscriptionID`, `PaymentDate`, and `Amount`. The `SubscriptionID` field is a foreign key reference to the `Subscription` table.

# Data Storing

GitHub Repo Description: Universal File Storage Database for Content Management System

Welcome to our GitHub repository for the Universal File Storage Database designed to support all types of files in binary format along with their path and file size. This database is specifically tailored for use in a Content Management System (CMS) and aims to provide a robust and versatile solution for file storage.

Database Schema:

The database schema is designed to accommodate files of any type, allowing users to store files in binary format and keep track of their original path and file size. Here are the tables with their respective columns:

* `DataID` : A unique identifier for each file stored in binary format.

* `FileName` : The name of the file being stored.

* `DataFile` : The actual binary representation of the file.

* `FilePath` : The original path of the file before being stored in binary format.

* `Extension` : The file extension, which helps identify the file type.

* `FileSize` : The size of the file in bytes.
  
* `ContentType` : Optional, can be used to specify the content type (e.g., `Document`, `Image`,` Audio`, `Video`, etc.).

# Binary Converter:
  The git submodule Binary File Converter and Database Storage  is  the binary converter of the files and retrive the data from the database.
  The binary converter is a tool that can be used to store the binary data for content in the `ContentData` table. The binary converter takes a file as input and converts it into a binary string. The binary string is then stored in the `ContentData` table.
  https://github.com/VALASALARAKESH/Binary-File-Converter-and-Database-Storage.git

# Usage:

1. Database Setup: Create the database using the SQL script provided in the repository (CREATE DATABASE Content_Management_System;). This script will set up the necessary structure for the Universal File Storage.

2. File Storage: Integrate the Universal File Storage Database with your Content Management System. When users upload files through the CMS, the binary converter can be used to convert and store the files in the ContentData table. Make sure to store the original file path and file size in the respective columns to preserve essential metadata.

3. Retrieval and Usage: Once files are stored in binary format, you can retrieve and use them as needed within your CMS. Retrieve the binary data from the DataFile column in the ContentData table, and use it to serve files to users or display content as required.

   * This Universal File Storage Database provides a flexible and scalable solution for storing files in binary format within a Content Management System. Whether it's documents, images, videos, or any other file type, this database can handle it all. Feel free to explore, customize, and enhance this repository to fit the specific requirements of your project.

# Contributing

Contributions are welcome. Please submit pull requests for any changes or improvements you would like to make. I hope this helps!
  
