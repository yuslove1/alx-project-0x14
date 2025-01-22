# API Explorer: Mastering RESTful Connections - MovieApp (Next.js, TypeScript, Tailwind CSS)

This project builds a MovieApp using Next.js, TypeScript, and Tailwind CSS, interacting with the [Movies Database API](https://moviesdatabase.p.rapidapi.com) via RapidAPI. It explores practical API interaction, data fetching, response handling, and authentication.

## Getting Started

1. **Clone the Repository:** `git clone https://github.com/yuslove1/alx-project-0x14.git`
2. **Navigate to Project Directory:** `cd alx-movie-app`
3. **Install Dependencies:** `npm install`
4. **Set Up Environment Variables:** Create a `.env.local` file in the root directory and add your MoviesDatabase API key: `MOVIE_API_KEY=RAPID_API_KEY`
5. **Run the Development Server:** `npm run dev`

## API Documentation and Usage

This project uses the [Movies Database API](https://moviesdatabase.p.rapidapi.com) via RapidAPI. Key aspects of the API are documented below.

## API Overview

The MoviesDatabase API provides access to a vast collection of movie data, including details like titles, descriptions, cast information, ratings, and more. It allows developers to integrate movie-related information into their applications.

## API Version

v1

## Available Endpoints

GET Search by imdb id

GET /titles/search/akas/{aka}

GET/titles/search/keyword/{keyword}

GET /titles/search/title/{title}


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

The [Movies Database API](https://moviesdatabase.p.rapidapi.com) may have usage limits, such as rate limiting.  Refer to the official documentation for specific details.  Best practices include caching frequently accessed data and implementing error handling to ensure application resilience.