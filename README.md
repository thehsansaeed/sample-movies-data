# Simple Movies API Documentation

Welcome to the Simple Movies API documentation. This API allows you to access information about movies, reserve a movie, view existing reservations, and update or delete reservations.

## Base URL

The base URL for this API is: `https://raw.githubusercontent.com/thehsansaeed/sample-movies-data/main/movies.json`

## Endpoints

### Status

#### GET /status

Returns the status of the API.

### List of Movies

#### GET /movies

Returns a list of movies.

Optional query parameters:

- `genre`: Filter movies by genre.
- `limit`: Limit the number of movies returned (1-20).

### Get a Single Movie

#### GET /movies/:movieId

Retrieve detailed information about a movie.

### Reserve a Movie

#### POST /reservations

Allows you to reserve a movie. Requires authentication.

Request body (JSON format):

- `movieId`: Integer - Required.
- `customerName`: String - Required.

### Get All Reservations

#### GET /reservations

Allows you to view all reservations. Requires authentication.

### Get a Reservation

#### GET /reservations/:reservationId

Allows you to view an existing reservation. Requires authentication.

### Update a Reservation

#### PATCH /reservations/:reservationId

Update an existing reservation. Requires authentication.

Request body (JSON format):

- `customerName`: String

### Delete a Reservation

#### DELETE /reservations/:reservationId

Delete an existing reservation. Requires authentication.

## API Authentication

To reserve or view a movie, you need to register your API client.

### Register API Client

#### POST /api-clients/

Request body (JSON format):

- `clientName`: String
- `clientEmail`: String

The response will contain the access token. The access token is valid for 7 days.

## Possible Errors

- Status code 409: "API client already registered." Try changing the values for clientEmail and clientName to something else.
