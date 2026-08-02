# URL Shortener

A full-stack URL shortening service built with Go, Redis, and React.

## Tech Stack

- **Backend** — Go (Fiber framework) + Redis
- **Frontend** — React + TypeScript
- **Infrastructure** — Docker + Docker Compose

## Features

- Shorten long URLs into clean short links
- Custom short URL slugs
- Configurable expiry (default 24 hours)
- IP-based rate limiting (10 requests / 30 minutes)

## Getting Started

### Prerequisites

- Docker & Docker Compose
- Node.js v16+

### Run the Backend

```bash
cd Backend
docker-compose up --build
```

API runs at `http://localhost:3000`

### Run the Frontend

```bash
cd Frontend/url-shortener
npm install
npm start
```

App runs at `http://localhost:3001`

## API

### POST `/api/v1` — Shorten a URL

```json
{
  "url": "https://example.com/very-long-url",
  "short": "my-slug",
  "expiry": 24
}
```

### GET `/:slug` — Redirect to original URL
