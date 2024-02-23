# Go-CRM-BackendCRM Backend using Golang # Simple CRM Lead Management System

The Simple CRM Lead Management System is a Go application that provides a RESTful API for managing leads. It utilizes the Fiber web framework and the GORM ORM library to handle HTTP requests and interact with a SQLite database.

## Features

- Retrieve all leads
- Retrieve a specific lead by ID
- Create a new lead
- Delete an existing lead

## Prerequisites

Before running the application, make sure you have the following installed:

- Go programming language (version 1.16+)
- SQLite database engine

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/A7medAbdien/Go-CRM-Backend.git
   ```

2. Navigate to the project directory:

   ```bash
   Go-CRM-Backend
   ```

3. Build the application:

   ```bash
   go build main.go
   ```

4. Run the application:

   ```bash
   go run main.go
   ```

5. The application will be available at `http://localhost:3000`.

## API Endpoints

The following API endpoints are available:

- `GET /api/v1/lead`: Retrieve all leads.
- `GET /api/v1/lead/:id`: Retrieve a specific lead by ID.
- `POST /api/v1/lead`: Create a new lead.
- `DELETE /api/v1/lead/:id`: Delete an existing lead.

## Usage

You can interact with the API endpoints using an HTTP client, such as cURL or Postman. Here are some examples:

- Retrieve all leads:

  ```bash
  curl http://localhost:3000/api/v1/lead
  ```

- Retrieve a specific lead by ID:

  ```bash
  curl http://localhost:3000/api/v1/lead/1
  ```

- Create a new lead:

  ```bash
  curl -X POST -H "Content-Type: application/json" -d '{"name":"John Doe","company":"ACME Inc","email":"john@example.com","phone":123456789}' http://localhost:3000/api/v1/lead
  ```

- Delete an existing lead:

  ```bash
  curl -X DELETE http://localhost:3000/api/v1/lead/1
  ```

## Database

The application uses an SQLite database to store lead information. The database file `leads.db` will be created in the project directory when you run the application. The database schema will be automatically migrated upon starting the application.

## Conclusion

The Simple CRM Lead Management System provides a simple and efficient way to manage leads through a RESTful API. You can use the provided API endpoints to retrieve, create, and delete leads in the SQLite database. Feel free to customize the application according to your specific requirements and extend its functionality as needed.