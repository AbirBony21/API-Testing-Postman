# API Testing using Postman

This repository contains some Postman collections for testing APIs.

## Prerequisites
- [Postman](https://www.postman.com/) installed on your system
- [Newman](https://www.npmjs.com/package/newman) installed for CLI execution

# M5V2 Prac1 - API Collection

This is a Postman collection for testing two different APIs: 
- Fake REST API for managing activities
- Restful Booker API for handling hotel bookings

## Importing the Collection
1. Open Postman.
2. Click on **Import**.
3. Select the `M5V2 Prac1.postman_collection.json` file and import it.

## Collection Variables
This collection uses collection variables for dynamic values:
- `URL`: Base URL for the Fake REST API.
- `activity`: Title for new activities.
- `auth_token`: Authentication token for the Restful Booker API.

## API Requests

### Activities API
- **Get Activities**: `GET {{URL}}/api/v1/Activities`
- **Add Activity**: `POST {{URL}}/api/v1/Activities`
- **Update Activity**: `PUT https://fakerestapi.azurewebsites.net/api/v1/Activities/29`
- **Delete Activity**: `DELETE https://fakerestapi.azurewebsites.net/api/v1/Activities/2`

### Restful Booker API
- **Authenticate**: `POST https://restful-booker.herokuapp.com/auth`
- **Get Booking IDs**: `GET https://restful-booker.herokuapp.com/booking`
- **Get Booking Details**: `GET https://restful-booker.herokuapp.com/booking/{id}`
- **Create Booking**: `POST https://restful-booker.herokuapp.com/booking`
- **Update Booking**: `PUT https://restful-booker.herokuapp.com/booking/1`
- **Partially Update Booking**: `PATCH https://restful-booker.herokuapp.com/booking/1`
- **Delete Booking**: `DELETE https://restful-booker.herokuapp.com/booking/1`
- **Health Check**: `GET https://restful-booker.herokuapp.com/ping`

## Authentication
For the Restful Booker API, an authentication token is required for modifying bookings.
1. Run the **Authenticate** request.
2. The token is automatically stored as `auth_token` and used in subsequent requests.

## Running the Collection
1. Set the required collection variables.
2. Execute individual requests or run the entire collection.

# M6V1 Prac1 - API Collection

This is a Postman collection for testing an API related to activities.

## Importing the Collection
1. Open Postman.
2. Click on **Import**.
3. Select the `M6V1_Prac1.postman_collection.json` file and import it.

## Collection Variables
This collection uses collection variables for dynamic values:
- `URL`: Base URL for the Fake REST API.
- `activity_name`: Title for new activities.
- `title_to_update`: Activity title to update.
- `id`: ID of an activity.
- `new_title`: Updated title for an activity.

## API Requests

### Activities API
- **Get Activities**: `GET {{URL}}/api/v1/Activities`
- **Add Activity (Valid Data)**: `POST {{URL}}/api/v1/Activities`
- **Update Activity**: `PUT https://fakerestapi.azurewebsites.net/api/v1/Activities/29`

## Automated Tests
- The collection includes Postman test scripts to validate responses:
  - **Status Code Validation**: Ensures the response returns the expected status code.
  - **Response Data Validation**: Compares actual API response data against expected values.
  - **Random Data Generation**: Generates dynamic activity names and IDs for testing.

## Running the Collection in Postman
1. Set the required collection variables.
2. Execute individual requests or run the entire collection.

## Running the Collection using Newman (CLI)
To run the collection via the command line using [Newman](https://www.npmjs.com/package/newman):

### Command:
```sh
newman run M6V1_Prac1.postman_collection.json


