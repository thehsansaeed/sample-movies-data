# Sample-Movies-Data

Certainly! Below is a README.md template for your GitHub repository:

---

# Documentation for API 

Welcome to the Simple Movies API documentation. This API provides access to information about movies, allows users to submit orders for movies, and view existing orders.

## Base URL

The base URL for this API is: `https://simple-movies-api.glitch.me`

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

### Submit an Order

#### POST /orders

Allows you to submit a new order. Requires authentication.

Request body (JSON format):

- `movieId`: Integer - Required.
- `customerName`: String - Required.

### Get All Orders

#### GET /orders

Allows you to view all orders. Requires authentication.

### Get an Order

#### GET /orders/:orderId

Allows you to view an existing order. Requires authentication.

### Update an Order

#### PATCH /orders/:orderId

Update an existing order. Requires authentication.

Request body (JSON format):

- `customerName`: String

### Delete an Order

#### DELETE /orders/:orderId

Delete an existing order. Requires authentication.

## API Authentication

To submit or view an order, you need to register your API client.

### Register API Client

#### POST /api-clients/

Request body (JSON format):

- `clientName`: String
- `clientEmail`: String

The response will contain the access token. The access token is valid for 7 days.

---

Feel free to customize this README file further to include additional information about your API, such as usage examples, authentication methods, and any other relevant details. Ensure that the README provides clear instructions for users on how to interact with your Simple Movies API.
