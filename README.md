# URL Shortener

A simple URL shortener service using Go, Redis, and Fiber.

## Features

- Shorten URLs with custom or random aliases.
- Redirect shortened URLs to their original destinations.
- Rate limiting to prevent abuse.
- Basic URL validation and security checks.

## Setup

### Prerequisites

- Docker
- Docker Compose

### Docker

Build and run the application:

docker-compose up --build

## Endpoints

### Shorten URL

- **POST** `/app/v1`
- **Body**: ```{
    "url": "https://example.com",
    "short": "customAlias", // optional
    "expiry": 24 // optional, in hours
  }```

 
### Resolve URL

- **GET** `/:short`
- Redirects to the original URL.
