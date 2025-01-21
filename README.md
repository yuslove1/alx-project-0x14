# API Explorer: Mastering RESTful Connections - MovieApp

This project aims to solidify understanding of RESTful APIs by building a MovieApp that interacts with the MoviesDatabase API.  It covers various aspects of API interaction, from exploring documentation to building a functional application.

## Getting Started

1. **Clone the Repository:** `git clone https://github.com/yuslove1/alx-project-0x14.git`
2. **Navigate to Project Directory:** `cd alx-movie-app`
3. **Install Dependencies:** `npm install` (or `yarn install`, depending on your package manager)
4. **Set Up Environment Variables:** Create a `.env` file in the root directory and add your MoviesDatabase API key: `REACT_APP_API_KEY=YOUR_API_KEY` (adapt as needed for your specific setup).
5. **Run the Development Server:** `npm start` (or the appropriate command for your framework)

## API Documentation and Usage

This project uses the MoviesDatabase API ([link to the API documentation](https://developer.themoviedb.org/reference/intro/getting-started)).  Key aspects of the API are documented below.

## API Overview

The MoviesDatabase API provides access to a vast collection of movie data, including details like titles, descriptions, cast information, ratings, and more. It allows developers to integrate movie-related information into their applications.

## API Version

v3

## Available Endpoints

* `/search/movie`: Searches for movies based on keywords.
* `/movie/{movie_id}`: Retrieves details about a specific movie.
* `/movie/popular`:  Fetches a list of popular movies.
* `/genre/movie/list`: Retrieves a list of movie genres.



## Request and Response Format

**Request Example (Search Movie):**

```typescript

GET /search/movie?api_key=YOUR_API_KEY&query=Inception

```

**Response Example (Search Movie - Simplified):**

```json
{
  "page": 1,
  "results": [
    {
      "id": 27205,
      "title": "Inception",
      "overview": "A thief who steals corporate secrets through the use of dream-sharing technology is given the inverse task of planting an idea into the mind of a CEO.",
      // ... other properties
    },
    // ... other results
  ],
}

```

## Authentication

Requests to the MoviesDatabase API require an API key.  This key should be included as a query parameter named `api_key` in all requests.  **Important:**  Store your API key securely, preferably as an environment variable, and do not expose it in your code.

## Error Handling

The API returns standard HTTP status codes to indicate success or failure.  Common error codes include:

* `401 Unauthorized`:  Invalid or missing API key.
* `404 Not Found`: The requested resource was not found.
* `429 Too Many Requests`: Rate limit exceeded.

The application should handle these errors gracefully, providing informative messages to the user.

## Usage Limits and Best Practices

The MoviesDatabase API may have usage limits, such as rate limiting.  Refer to the official documentation for specific details.  Best practices include caching frequently accessed data and implementing error handling to ensure application resilience.