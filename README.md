
# Products API

This project is a backend implementation of a Products API using ASP.NET Web API with .NET 8. The project follows the Earth Layer Architecture and Repository Pattern for a clean and maintainable codebase.

## Project Structure

The project is structured in various layers to promote separation of concerns and scalability:
1. **Products.Api**: The presentation layer that handles HTTP requests and responses.
2. **Products.Domain**: The domain layer that contains domain entities and repository interfaces.
3. **Products.Infrastructure**: The infrastructure layer that contains data access logic and implementations of repository interfaces.

## Earth Layer Architecture

The Earth Layer Architecture separates the project into distinct layers, each responsible for a specific part of the application. This helps in maintaining a clean and scalable codebase.

## Features

- **CRUD Operations**: Implemented Create, Read, Update, and Delete operations for products.
- **Repository Pattern**: Used to abstract the data access layer from the business logic layer.
- **Email Service**: Configured using MailKit to send emails.

## Getting Started

### Prerequisites

- .NET 8 SDK
- SQL Server
- SMTP server credentials for sending emails

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/Joshasha/Products.git
    cd Products
    ```
2. Restore dependencies:
    ```sh
    dotnet restore
    ```
3. Update the configuration in `appsettings.json`:
    ```json
    {
     "EmailSettings": {
      "Host": "smtp.gmail.com",
      "Port": 465,
      "Username": "example@gmail.com",
      "Password": "Your PassWord"
    },
    ```

### Running the Application

1. Build the project:
    ```sh
    dotnet build
    ```
2. Run the project:
    ```sh
    dotnet run --project Products.Api
    ```

### Swagger

Swagger is configured for API documentation. To access the Swagger UI, run the application and navigate to:
    ```sh
    https://localhost:4718/swagger/index.html
    ```

## Usage

### API Endpoints

- **Get all products**: `GET /api/products`
- **Get a product by ID**: `GET /api/products/{id}`
- **Create a new product**: `POST /api/products`
- **Update a product**: `PUT /api/products/{id}`
- **Delete a product**: `DELETE /api/products/{id}`

