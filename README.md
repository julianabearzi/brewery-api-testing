# Brewery API Testing

A test report done for a Brewery API.

# Tasks

## 1. Description

Find bugs or quality concerns when testing the Brewery API.
With Docker a container was started to run the API. This allowed access to the documentation in Swagger used to perform the tests manually.

GET requests:

- List breweries ("/breweries")
- Get a single brewery ("/breweries/{id}")
- Search breweries based on search term ("/breweries/search")

## Bugs found

The following bugs were found:

#### GET /breweries

1. Breweries list returns Internal Server Error (ID: B001)

#### GET /breweries/{id}

1. Response 404 after consecutive requests (ID: B002)

#### GET /breweries/search

1. API returns Internal Server Error after using param with more than 5 characters or with less than 5 characters (ID: B003)

#### GET /breweries?{query}

1. API returns Internal Server Error when request is string of name, state or type. (ID: B004)

#### Please see the bug report for more details.

[Click here to read the bug report](https://docs.google.com/spreadsheets/d/1m4hFgY1UP7_rxVc6IEatumfFzdSyizrE/edit#gid=911234466)

## 2. Description

Do some tests using any framework you are comfortable with, or you're keen to try.

I made a [Postman Collection](https://www.postman.com/)

### Dependencies & Preconditions

- Postman is necessary
- Server must be up and running

### How to run the Collection

1. Download the 'API Brewery.postman_collection.json' file from this repository.
2. Open Postman and choose any Workspace.
3. Import the Collection.
4. Click on the three dots menu that appear at the right of the Collection's name when you hover over it.
5. Select the option 'Run collection'.
6. Click on 'Run API Brewery'.

### Comments

- The Docker container initiates properly but when starting making requests to the API I noticed that I was always getting a 500 Server Error. Several attempts were made with no data received from the API.
  I made the reports based on the limited scenarios I could test, won't hesitate on doing a test run again if any issues were encountered with the Docker container.
