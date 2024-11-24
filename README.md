# Movie API

A Spring Boot application that provides a RESTful API for managing movies and reviews. The application uses MongoDB as its database and includes endpoints to fetch movie data and add reviews.

## Features

- Retrieve a list of movies.
- Retrieve details of a single movie by its IMDb ID.
- Add reviews to movies.
- MongoDB integration for efficient data storage.

## Technologies Used

- Spring Boot
- Maven
- MongoDB
- Lombok
- REST API
- Java

## Endpoints

### Movies
- **GET /api/v1/movies**  
  Retrieve all movies.  
  **Response:** List of movies.

- **GET /api/v1/movies/{imdbId}**  
  Retrieve a single movie by IMDb ID.  
  **Path Parameter:** `imdbId`  
  **Response:** Movie details.

### Reviews
- **POST /api/v1/reviews**  
  Add a review to a movie.  
  **Request Body:**  
  ```json
  {
    "reviewBody": "Your review text",
    "imdbId": "Movie IMDb ID"
  }

  Prerequisites
Java 17 or later
Maven
MongoDB

Getting Started
Clone the repository:

bash
Copy code
git clone <repository-url>
cd movie-api
Configure MongoDB:
Ensure MongoDB is running locally or update the application.properties file to point to your MongoDB instance.

Example:

properties
Copy code
spring.data.mongodb.uri=mongodb://localhost:27017/moviesdb
Build and Run the Application:

bash
Copy code
mvn clean install
mvn spring-boot:run
Access the API:
The API will be available at http://localhost:8080.

Example Data
Sample Movie Object
json
Copy code
{
  "id": "64c2f8e43d2e3c6f4d678a0b",
  "imdbId": "tt1234567",
  "title": "Example Movie",
  "releaseDate": "2023-01-01",
  "trailerLink": "https://youtube.com/example",
  "poster": "https://imageurl.com/poster.jpg",
  "genres": ["Action", "Adventure"],
  "backdrops": ["https://imageurl.com/backdrop1.jpg"],
  "reviews": []
}
Libraries and Dependencies
Spring Boot Starter Web: For creating RESTful APIs.
Spring Boot Starter Data MongoDB: For MongoDB integration.
Lombok: For reducing boilerplate code.
Spring Boot DevTools: For development convenience.
Future Enhancements
Authentication and authorization.
Pagination for movie lists.
Advanced search functionality.
Dockerization for containerized deployment.
License
This project is open-source and available under the MIT License.

Author
Jorge Allan Paz Garza
