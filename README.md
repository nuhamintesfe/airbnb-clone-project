# airbnb-clone-project

This project is a full-stack clone of Airbnb, built to demonstrate modern backend development practices, API security, database design, and CI/CD deployment. It is powered by Django, PostgreSQL, GraphQL, and Docker.

## Tech Stack
- Django
- PostgreSQL
- GraphQL
- Docker
- GitHub Actions
  
## Team Roles

### Backend Developer
Responsible for building RESTful APIs, managing server-side logic, and integrating with the database.

### Database Administrator
Designs and maintains the database schema, ensures data integrity and performance.

### DevOps Engineer
Sets up CI/CD pipelines, manages Docker containers and deployment strategies.

### Security Engineer
Implements security measures like authentication, encryption, and input validation.

### Project Manager
Coordinates the team, tracks progress, and ensures project milestones are met.

## Technology Stack

- **Django**: A high-level Python web framework used to build the backend and RESTful APIs.
- **PostgreSQL**: A powerful open-source relational database for storing structured data.
- **GraphQL**: Enables efficient and flexible API data queries and mutations.
- **Docker**: Containerizes the application for consistent development and deployment.
- **GitHub Actions**: Automates testing and deployment via CI/CD pipelines.

## Database Design

### Entities

- **User**
  - Fields: id, username, email, password, date_joined
  - Relationships: Can have multiple bookings, reviews, and listed properties

- **Property**
  - Fields: id, owner_id, title, location, price_per_night
  - Relationships: Belongs to a user, has many bookings and reviews

- **Booking**
  - Fields: id, user_id, property_id, check_in, check_out
  - Relationships: Belongs to a user and a property

- **Review**
  - Fields: id, user_id, property_id, rating, comment
  - Relationships: Belongs to a user and a property

- **Payment**
  - Fields: id, booking_id, amount, payment_status, date
  - Relationships: Linked to a booking

## Feature Breakdown

- **User Registration & Authentication**
  Allows users to sign up, log in, and manage their profiles securely.

- **Property Management**
  Hosts can list properties with photos, descriptions, and pricing.

- **Booking System**
  Users can check availability, book properties, and view their bookings.

- **Review System**
  Enables guests to rate and review properties after their stay.

- **Payment Integration**
  Supports secure online payments and payment history tracking.

## API Security

### Authentication
Only registered users can access specific endpoints using JWT tokens.

### Authorization
Permissions will be applied to prevent unauthorized access (e.g., only hosts can update their listings).

### Rate Limiting
Protects APIs from abuse by limiting the number of requests per user/IP.

### Input Validation
All incoming data is validated to prevent SQL injection and XSS.

### Data Encryption
Passwords and sensitive data are encrypted using industry standards.

**Why It’s Important**:
- Protects user data and transactions.
- Prevents unauthorized bookings or edits.
- Ensures secure payment processing.

## CI/CD Pipeline

**CI/CD (Continuous Integration and Continuous Deployment)** automates testing and deployment to reduce errors and speed up releases.

### Tools:
- **GitHub Actions**: Automates testing, linting, and deployment on every commit.
- **Docker**: Ensures consistency across development, staging, and production environments.

**Benefits**:
- Early bug detection
- Faster iteration and feedback
- Safer deployments with rollback support

