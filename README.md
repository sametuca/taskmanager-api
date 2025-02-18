# TaskManager API

## Project Description

TaskManager API is a RESTful API that allows users to manage their tasks efficiently. This API supports creating, listing, updating, and deleting tasks.

## Features

- Create tasks
- List tasks
- Update tasks
- Delete tasks

## Prerequisites

- .NET 8.0 (or compatible version)
- SQL Server (or other supported databases)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/sametuca/taskmanager-api.git
   cd taskmanager-api
   ```

2. **Set up the database:**

   Ensure your database connection is correctly configured in `appsettings.json`.

3. **Apply database migrations:**

   ```bash
   dotnet ef database update
   ```

4. **Run the application:**

   ```bash
   dotnet run
   ```

## API Endpoints

### Task Endpoints

| Method   | Endpoint          | Description          |
|----------|-------------------|----------------------|
| `GET`    | `/api/tasks`      | Get all tasks       |
| `GET`    | `/api/tasks/{id}` | Get task by ID      |
| `POST`   | `/api/tasks`      | Create a new task   |
| `PUT`    | `/api/tasks/{id}` | Update a task       |
| `DELETE` | `/api/tasks/{id}` | Delete a task       |

## Example Request

### Create a Task

```bash
POST /api/tasks
```

Request Body:

```json
{
  "title": "Sample Task",
  "description": "This is a sample task",
  "dueDate": "2023-12-31",
  "status": "Pending"
}
```

## Running Tests

To run the unit tests:

```bash
dotnet test
```

## Contribution

Contributions are welcome! Feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
