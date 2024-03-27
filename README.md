# Rocket Web Application

This Rocket web application provides a RESTful API for managing Rustaceans, a playful reference to users familiar with the Rust programming language. It uses Rocket for the web framework, Diesel as the ORM for database interactions, and Serde for serialization and deserialization of Rust structs.

## Features

- **CRUD Operations**: Create, read, update, and delete Rustaceans.
- **Asynchronous Support**: Leveraging Rocket's async capabilities for efficient database operations.
- **Secure**: Basic authentication for protected routes.
- **JSON Support**: Uses Serde for handling JSON request/response bodies.

## Getting Started

These instructions will get your copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

- Rust (latest stable version)
- Cargo (comes with Rust)
- Diesel CLI
- SQLite (or adjust the Diesel and Rocket configuration for your DBMS)

### Installation

1. **Clone the repository:**

```bash
git clone https://yourproject/repository.git
cd repository
```

2. **Setup the database:**

Make sure you have Diesel CLI installed. If not, install it with:

```bash
cargo install diesel_cli --no-default-features --features sqlite
```

Then, run:

```bash
diesel setup
diesel migration run
```

3. **Build and run the project:**

```bash
cargo run
```

The server will start running on `localhost:8000`.

## Usage

### Create a Rustacean

- **Endpoint**: `POST /rustaceans`
- **Body**:

```json
{
    "name": "Jane Doe",
    "email": "jane.doe@example.com"
}
```

### Get All Rustaceans

- **Endpoint**: `GET /rustaceans`

### Update a Rustacean

- **Endpoint**: `PUT /rustaceans/{id}`
- **Body**:

```json
{
    "name": "Jane Doe Updated",
    "email": "janeupdated@example.com"
}
```
