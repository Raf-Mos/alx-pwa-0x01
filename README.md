# alx-project-0x14

## API Overview

The MoviesDatabase API is a comprehensive movie database service that provides access to a vast collection of movie information. This RESTful API allows developers to retrieve detailed movie data including titles, release years, genres, cast information, ratings, and poster images. The API is designed to support movie discovery applications by offering powerful filtering and search capabilities, making it easy to build engaging movie browsing experiences.

## Version

API Version: 1.0

## Available Endpoints

- **GET /titles** - Retrieve a list of movies with optional filtering parameters
  - Supports pagination through page parameter
  - Filter by year, genre, and other criteria
  - Returns movie titles with basic information

- **GET /titles/{id}** - Get detailed information about a specific movie
  - Returns comprehensive movie details including cast, crew, and ratings

- **GET /titles/search/{query}** - Search for movies by title
  - Full-text search across movie titles
  - Returns matching results with relevance scoring

## Request and Response Format

### Typical Request Structure
```
GET /titles?year=2023&page=1&limit=12&sort=year.decr&genre=Action
Headers:
  x-rapidapi-host: moviesdatabase.p.rapidapi.com
  x-rapidapi-key: YOUR_API_KEY
```

### Response Object Structure
```json
{
  "page": 1,
  "next": "/titles?page=2",
  "entries": 12,
  "results": [
    {
      "id": "tt1234567",
      "titleText": {
        "text": "Movie Title"
      },
      "primaryImage": {
        "url": "https://example.com/poster.jpg"
      },
      "releaseYear": {
        "year": 2023
      },
      "genres": {
        "genres": [
          {
            "text": "Action"
          }
        ]
      }
    }
  ]
}
```

## Authentication

The MoviesDatabase API uses RapidAPI key-based authentication:

- **Header Required**: `x-rapidapi-key`
- **Host Header**: `x-rapidapi-host: moviesdatabase.p.rapidapi.com`
- **API Key**: Obtained from RapidAPI platform after subscription
- **Storage**: Store API key in environment variables (never in client-side code)

### Example Authentication Headers
```
x-rapidapi-host: moviesdatabase.p.rapidapi.com
x-rapidapi-key: your-rapidapi-key-here
```

## Error Handling

### Common Error Responses

- **401 Unauthorized**: Invalid or missing API key
- **403 Forbidden**: API key lacks required permissions
- **429 Too Many Requests**: Rate limit exceeded
- **500 Internal Server Error**: Server-side issues

### Error Response Format
```json
{
  "message": "Invalid API key. Go to https://docs.rapidapi.com/docs/keys for more info.",
  "error": "Unauthorized"
}
```

### Recommended Error Handling
- Implement try-catch blocks for all API calls
- Check response status codes before processing data
- Provide user-friendly error messages
- Implement retry logic for temporary failures

## Usage Limits and Best Practices

### Rate Limits
- Free tier: Limited requests per month
- Paid tiers: Higher limits based on subscription plan
- Monitor usage through RapidAPI dashboard

### Best Practices
- **Pagination**: Use limit parameter to control response size (recommended: 12-20 items)
- **Caching**: Implement client-side caching to reduce API calls
- **Error Boundaries**: Use React error boundaries for graceful failure handling
- **Environment Variables**: Store API keys securely using .env.local
- **Server-side Calls**: Make API requests from Next.js API routes to protect keys
- **Efficient Filtering**: Use specific genre and year filters to get relevant results
- **Image Optimization**: Use Next.js Image component for poster optimization

### Optimization Tips
- Batch requests when possible
- Implement debouncing for search functionality
- Use background loading for better user experience
- Cache frequently accessed data locally
