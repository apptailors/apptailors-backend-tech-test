# AppTailors Backend recruitment task


## Task 
Create web application with two endpoints:
  - endpoint `/meal/{name}/img` should return simple html page with meal name and displayed meal image 
  - endpoint `/meal/{name}/` should return JSON with 
  ```
  {
    "id": <identifier>,
    "name": "<meal name>",
    "instructions": "<meal preparation instruction>",
    "ingredientsNumber": <number>,
    "ytLink": "<youtube link>"
  }
  ```
  - hint: ingredientsNumber should be number of not empty fields `strIngredient{X}`
  - Get proper data from external API https://www.themealdb.com/api.php

## Business requirements
- handle simple edge cases e.g. for wrong meal name return proper HTTP status code 
- validate input parameters (do not allow numbers and special characters etc.)
- handle case when API will return multiple results
- prevent from making multiple times same request to external API, save result for later usage in map/dictionary or other simple data structure with quick access

## Technical requirements
- Node.js Express app with Typescript 
- provide Git history
- add sample unit tests e.g. for calculating number of ingredients
- pay attention to code quality, naming etc.
- provide instructions how to run app

## Optional
- use async/await syntax for external API calls
- instead of using map/dictionary for caching external API results use external library, in-memory database or external database 
- dockerize project
