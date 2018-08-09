# EvolentContactAssigment

Contactpedia
Contactpedia stores and manages the contact information of the clients with an provision to add modify or delete the contact information.

Getting Started
Run Contacts.sql script file in SQL server to create initial database and ContactInformation table.
Unzip contactpedia.zip folder and follow below steps:

Copy the project and open 2 different instances of the application in visual studio 2017. ContactpediaService app and ContactpediaApp should be run separately to run a local version of it.

For deployment:
Right click the project to deploy, click "Publish..." and select "Folder".
Browse the folder location to store the published files and click "Publish", it will build the application and publish the files to the mentioned location.
Go to Server (IIS,Linux or Mac), create a directory and paste the published files. 
Set authorization and other settings and start the server. 
This will make the application live thus accessible from browser or other apps having access to call the application.


Prerequisites

Visual Studio 2017 or above for running the code
ref: https://docs.microsoft.com/en-us/visualstudio/install/install-visual-studio

Sql Server 2015 or above for database connection
ref: https://docs.microsoft.com/en-us/sql/database-engine/install-windows/install-sql-server-from-the-installation-wizard-setup

IIS for windows, linux or mac server to deploy the application
ref: https://msdn.microsoft.com/en-us/library/ms181052(v=vs.80).aspx

Any Browser to run the application. 
ref: https://support.google.com/chrome/answer/95346?co=GENIE.Platform%3DDesktop&hl=en-GB

Postman for running the api independently
ref: https://www.sap.com/india/developer/tutorials/api-tools-postman-install.html

Running the tests
Set up a dummy database based on the entities (will attach a database file later), set the database connection string in the appsettings.json file and run the unit test.

Application Structure

Below are the project details and their respective folder structure with details about what are the contents in the folders

ContactpediaApp
A web application project made using asp.net core mvc for accessing the ContactpediaService to get the data and display them in the UI

Folders
Controller: Contains the controller which renders the views and calls the service to get the data.
Helper: contains helper file for making http requests
Models: contains viewmodels for mapping the ui fields to the objects thus sending to service for saving and fetching data
Views: contains ui screens for rendering the data received from service

Frameworks: Asp.net Core MVC, RestSharp for HttpCommunication

ContactpediaService
A service application made using asp.net core webApi for building http services to fetch and save contact information

Folders
Controller: Contains the controller which renders the views and calls the service to get the data.
Models: contains entities for mapping the input data to the entities thus saving and fetching data using the repositories
Repositories: contains repositories to make database interaction to fetch or save data into database
Validators: contains custom validators for validating data received as an input to the service

Frameworks and technologies: Asp.net Core WebAPI using dependency injection, asp.net core entityFramework, Repository Pattern

ContactpediaServiceUnitTests
A unit test project to test the api services made using ms unit test project with Moq framework for mocking

Frameworks: MS Unit Test, Moq for mocking

Authors
Kanhaiya Kumawat - Initial work 


