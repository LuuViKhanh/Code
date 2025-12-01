# Flyora Backend

A Spring Boot backend application for the Flyora e-commerce platform specializing in bird-related products.

## Features

- User authentication and authorization with JWT
- Product management (birds, food, toys, furniture)
- Order processing and management
- Payment integration with PayOS
- Shipping integration with GHN (Giao Hàng Nhanh)
- Admin dashboard functionality
- Customer support and issue reporting
- News and blog management
- Real-time notifications

## Technology Stack

- **Framework**: Spring Boot 2.7.18
- **Database**: AWS DynamoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Payment**: PayOS
- **Shipping**: GHN API
- **Documentation**: OpenAPI/Swagger
- **Build Tool**: Maven
- **Java Version**: 17

## Setup

### Prerequisites

- Java 17 or higher
- Maven 3.6+
- AWS Account (for DynamoDB)

### Environment Variables

Copy `.env.example` to `.env` and configure the following variables:

```bash
# Database Configuration
DB_URL=your-database-url
DB_USERNAME=your-db-username
DB_PASSWORD=your-db-password

# JWT Configuration
JWT_SECRET=your-jwt-secret-key

# GHN Configuration
GHN_TOKEN=your-ghn-token
GHN_SHOP_ID=your-shop-id
GHN_DISTRICT_ID=your-district-id
GHN_WARD_CODE=your-ward-code

# PayOS Configuration
PAYOS_CLIENT_ID=your-payos-client-id
PAYOS_API_KEY=your-payos-api-key
PAYOS_CHECKSUM_KEY=your-payos-checksum-key
```

### Running the Application

1. Clone the repository
2. Configure environment variables
3. Run the application:

```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

### API Documentation

Once the application is running, you can access the API documentation at:
- Swagger UI: `http://localhost:8080/swagger-ui.html`

## Project Structure

- `src/main/java/org/example/flyora_backend/`
  - `controller/` - REST API controllers
  - `service/` - Business logic services
  - `repository/` - Data access layer
  - `dynamo/models/` - DynamoDB entity models
  - `DTOs/` - Data Transfer Objects
  - `configuration/` - Spring configuration classes
  - `Utils/` - Utility classes

## Security

This project uses environment variables for sensitive configuration. Never commit actual credentials to version control.

## License

This project is proprietary software.