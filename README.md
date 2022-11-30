## Introduction
***PawPaw*** is a start-up pet store where you can adopt **stray animals**. These animals survived the streets of East European countries (Azerbaijan, Georgia, and Turkey*) and are waiting for their new **foster families**. **Our store** is a window for pets, where you can choose them by different categories.

## Overview
Our **API Guide** describes the workflow of **getting**, **creating**, and **deleting** a pet from our database with the API. 

## API Features
The API list provides features in these categories:

> Listing the pets in the shelters by their status (available, pending, sold)

> Adding a specific pet to the database

> Getting full data on the specific pet

> Deleting all information about the specific pet

## Adding a pet to the database (POST)

Every pet is an object in the **JSON** format with various values such as ID, category, name, photos, tags, and status. You can post an animal to the database using the post method and https://petstore.swagger.io/v2/swagger.json/pet endpoint.

EXAMPLE:

```json
{
  "id": 0,
  "category": {
    "id": 0,
    "name": "string"
  },
  "name": "doggie",
  "photoUrls": [
    "string"
  ],
  "tags": [
    {
      "id": 0,
      "name": "string"
    }
  ],
  "status": "available"
}
```


## Getting information on a specific pet (GET)

You can access all data on any single pet by adding the ID at the end of the endpoint https://petstore.swagger.io/v2/swagger.json/pet/{petId}


## Deleting a pet from the database (DELETE)

You can also delete a single animal from the database, adding the ID at the end of the endpoint https://petstore.swagger.io/v2/swagger.json/pet/{petId}


Sample values for a single pet:

| KEY         | VALUE       |
| :---        |    ----:   | 
| id          | 123456789       |
| category   | id: 1, name: "dog"        | 
| name   | "Jackie"        | 
| photoUrls   | "https://www.cesarsway.com/wp-content/uploads/2015/06/stray-dog-cesars-way.jpg"        | 
| tags   |   id: 1, name: "speckled"      | 
| status   |   "pending"      | 



## Finding the pets by their status

Our pets have three availability statuses (available, pending, and sold), and you can reach them using "https://petstore.swagger.io/v2/swagger.json/pet/findByStatus" endpoint.

You can fetch the data of specific categories accordingly:

```
fetch('https://petstore.swagger.io/v2/swagger.json/pet/findByStatus')
  .then((response) => response.json())
  .then((data) => console.log(data));
```






---
**These countries are given examples because the high stray animals' population is verified.*
