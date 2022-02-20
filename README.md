# BK-Retail
E-commerce website back-end using Sequelize and provided front-end

Screencastify walkthru link: chrome-extension://mmeijimgabbpbgpdklnllpncmdofkcpn/app.html#/files/42b65111-52ec-4926-y677-3b30278a5a74?autostopped

GitHub Repository link: https://github.com/bradkuhne/BK-Retail

## Description
  
 The BK Retail application allows a user to maintain product categories, products and product tags from the command line. To initialize this application files can be seeded by running db.sql, schema.sql and seeds.sql in sequential order.  To start the application enter npm start from the command prompt.  There is no front end to this application.

   
## License
  
 [![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)
  
 The Unlicense is a template for disclaiming copyright monopoly interest in software you've written; in other words, it is a template for dedicating your software to the public domain. It combines a copyright waiver patterned after the very successful public domain SQLite project with the no-warranty statement from the widely-used MIT/X11 license.
  
## Table of Contents
  
* [Installation](#Installation)
  
* [Usage](#Usage)
  
* [Contributions](#Contributions)
  
* [Tests](#Tests)
  
* [Questions](#Questions)
  
## Installation
  
 To install the BK Retail application you need to have Express, Sequelize and mysql2 installed.  After that, just start the application from the command prompt using NPM Start.  To initialize this application files can be seeded by running db.sql, schema.sql and seeds/index.js in sequential order.  To start the application enter npm start from the command prompt.  There is no front end to this application.
  
## Usage
  
 The BK-Retail application could be used by anyone who wants to manipulate simple joined tables.
  
## Contributions
  
 This project was solely developed by Brad Kuhne.
  
## Test Instructions
  
 This project was not developed with Express.  To test it, run index.js and compare results to expected results.
  
## Questions
  
 https://github.com/bradkuhne  Email: bjkuhne@aol.com


User Story
AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
Acceptance Criteria
GIVEN a functional Express.js API
WHEN I add my database name, MySQL username, and MySQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the MySQL database
WHEN I open API GET routes in Insomnia for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete data in my database
Mock-Up
The following animations show examples of the application's API routes being tested in Insomnia.

The first animation shows GET routes to return all categories, all products, and all tags being tested in Insomnia:

The second animation shows GET routes to return a single category, a single product, and a single tag being tested in Insomnia:

The final animation shows the POST, PUT, and DELETE routes for categories being tested in Insomnia:

Your walkthrough video should also show the POST, PUT, and DELETE routes for products and tags being tested in Insomnia.

You’ll need to use the MySQL2 (Links to an external site.) and Sequelize (Links to an external site.) packages to connect your Express.js API to a MySQL database and the dotenv package (Links to an external site.) to use environment variables to store sensitive data, like your MySQL username, password, and database name.

Use the schema.sql file in the db folder to create your database using MySQL shell commands. Use environment variables to store sensitive data, like your MySQL username, password, and database name.

Database Models
Your database should contain the following four models, including the requirements listed for each model:

Category

id

Integer

Doesn't allow null values

Set as primary key

Uses auto increment

category_name

String

Doesn't allow null values

Product

id

Integer

Doesn't allow null values

Set as primary key

Uses auto increment

product_name

String

Doesn't allow null values

price

Decimal

Doesn't allow null values

Validates that the value is a decimal

stock

Integer

Doesn't allow null values

Set a default value of 10

Validates that the value is numeric

category_id

Integer

References the category model's id

Tag

id

Integer

Doesn't allow null values

Set as primary key

Uses auto increment

tag_name

String

ProductTag

id

Integer

Doesn't allow null values

Set as primary key

Uses auto increment

product_id

Integer

References the product model's id

tag_id

Integer

References the tag model's id

Associations
You'll need to execute association methods on your Sequelize models to create the following relationships between them:

Product belongs to Category, as a category can have multiple products but a product can only belong to one category.

Category has many Product models.

Product belongs to many Tag models. Using the ProductTag through model, allow products to have multiple tags and tags to have many products.

Tag belongs to many Product models.

Make sure you set up foreign key relationships that match the column we created in the respective models.

Fill Out the API Routes to Perform RESTful CRUD Operations
Fill out the unfinished routes in product-routes.js, tag-routes.js, and category-routes.js to perform create, read, update, and delete operations using your Sequelize models.

NOTE
The functionality for creating the many-to-many relationship for products is already done for you.

HINT
Be sure to look at your module project's code for syntax help and use your model's column definitions to figure out what req.body will be for POST and PUT routes!

Seed the Database
After creating the models and routes, run npm run seed to seed data to your database so that you can test your routes.

Sync Sequelize to the Database on Server Start
Create the code needed in server.js to sync the Sequelize models to the MySQL database on server start.

Walkthrough Video: 37%
A walkthrough video that demonstrates the functionality of the e-commerce back end must be submitted, and a link to the video should be included in your README file.

The walkthrough video must show all of the technical acceptance criteria being met.

The walkthrough video must demonstrate how to create the schema from the MySQL shell.

The walkthrough video must demonstrate how to seed the database from the command line.

The walkthrough video must demonstrate how to start the application’s server.

The walkthrough video must demonstrate GET routes for all categories, all products, and all tags being tested in Insomnia.

The walkthrough video must demonstrate GET routes for a single category, a single product, and a single tag being tested in Insomnia.

The walkthrough video must demonstrate POST, PUT, and DELETE routes for categories, products, and tags being tested in Insomnia.

