# URL Shortener

A full-stack URL shortening application built using Spring Boot that converts long URLs into short, shareable links and redirects users to the original URL.

## Live Demo

[Try the Application](https://url-shortener-smpa.onrender.com)

## Features

- Shorten long URLs into compact links
- Redirect short URLs to their original destination
- Persistent URL storage using MySQL
- Server-side rendered UI using Thymeleaf
- Input validation and error handling
- RESTful backend architecture
- Cloud-hosted MySQL database
- Dockerized and deployed on Render

## Tech Stack

### Backend
- Java 21
- Spring Boot
- Spring MVC
- Spring Data JPA
- Hibernate

### Frontend
- Thymeleaf
- HTML
- CSS

### Database
- MySQL
- Aiven Cloud MySQL

### Deployment
- Docker
- Render

## How It Works

1. User submits a long URL.
2. The backend generates a unique short code.
3. The original URL and short code are stored in MySQL.
4. A shortened URL is returned to the user.
5. Visiting the shortened URL redirects the user to the original URL.

Example:

Long URL:

```text
https://example.com/some/very/long/url
```

Short URL:

```text
https://your-app.onrender.com/abc123
```

## Project Architecture

```text
Client
  |
  v
Spring MVC Controller
  |
  v
Service Layer
  |
  v
Spring Data JPA Repository
  |
  v
MySQL Database
```

## Database Entity

The URL mapping stores information such as:

```text
id
originalUrl
shortCode
createdAt
```

Adjust this section to match the actual fields in your entity.

## Running Locally

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY
cd URL-shortener-spring-demo-main
```

### 2. Configure environment variables

```text
DB_URL=jdbc:mysql://localhost:3306/urlshortener
DB_USERNAME=root
DB_PASSWORD=your_password
```

### 3. Run the application

Linux/macOS:

```bash
./gradlew bootRun
```

Windows:

```bash
gradlew.bat bootRun
```

The application will run locally on:

```text
http://localhost:8081
```

## Production Deployment

The application is containerized using Docker and deployed on Render.

Production architecture:

```text
User
  |
  v
Render
Spring Boot Application
  |
  v
Aiven Cloud
MySQL Database
```

Database credentials are configured using environment variables and are not stored in the source code.

## Author

Nandeshwar Reddy Challa
