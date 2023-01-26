# E Commerce Back End

## Description

This application is the back end of an e-commerce store. It uses an Express.js API with Sequelize to interact with the MySQL databases.

## Installation & Usage

To isntall the application follow the steps below:
* Clone the repository into your desired directory on your local machine.
* Install the npm packages by running the "npm install" command in the directory terminal.

Below are the steps to setup the database, seed the database, and run the server:
* First you will want to source the schema for the database
    * Navigate to the root directory folder of the application
    * Open the command line terminal
    * Type the command "mysql -u root -p"
    * Input your password if you have one
    * Once mysql is started you will need to source the schema
    * Type the command "source db/schema.sql"
    * Type "quit" to exit the mysql shell
* Next you will need to seed the data
* Type the command "npm run seed"
* The console should return that all models have been seeded
* Now to start the server
* Type the command "npm start" to start the server
* Once the server is running you can now open Insomnia and perform the different route calls

There are multiple routes that can be called to modify or view the data in the database. The user has the option to GET all of the products, categories, and tags. To GET a single product, category, or tag the endpoint with the associated ID can be used. To create a new product, category, or tag the user can use a POST route. A PUT route can be used to update information in the database by specifing the appropriate ID. Lastly, to DELETE any information in the database the user can do so by using a DELETE route with the appropriate ID.

## Technologies & Code Description
The following technologies were used for this application:
* JavaScript
* Node.js
* Express.js
* MySQL2
* Sequelize
* dotenv

The Models and their column requirements can be found in the "models" folder. Here the column requirements set the data that can be included within the table. The models are associated to one another. For one category there can be many products so this creates a One-To-Many association. Each product can have multiple tags and multiple tags can belong to multiple products. This creates a Many-To-Many association. This is done through the "ProductTag" model. These associations can be found in the "index.js" file within the "models" folder.

The files that hold the code to make the different GET, POST, PUT, and DELETE routes are found in the "routes" folder. The PUT and DELETE routes include the parameter of ID. This is so that the user can specify what data they want to update or delete.

## Video Walkthrough
Below is a video walkthrough showing how the application is sourced, seeded, and server started. Next the video will show the results of the GET, POST, PUT, and DELETE routes when tested in Insomnia.

https://drive.google.com/file/d/1KLa6efe7YKdtejouQJN6fDfe_zRiuJp7/view
