# API Testing using Postman

This repository contains some Postman collections for testing APIs.

## Prerequisites
- [Postman](https://www.postman.com/) installed on your system

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

