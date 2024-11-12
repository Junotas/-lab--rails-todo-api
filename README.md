
---

# Todo API

This is a simple API for managing tasks, built with Ruby on Rails.

## Requirements

- **Ruby Version**: 3.3.6
- **Rails Version**: 8.0.0
- **Database**: SQLite (default) or PostgreSQL

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/todo-api.git
cd todo-api
```

### 2. Install Dependencies

Run the following to install all required gems:

```bash
bundle install
```

### 3. Configure the Database

- **Database Creation**: This project uses SQLite by default, but you can modify `config/database.yml` to switch to PostgreSQL or another database.
- **Database Setup**: Run the following commands to create and initialize the database.

```bash
rails db:create
rails db:migrate
```

### 4. Start the Server

Start the Rails server:

```bash
rails server
```

The API will be available at [http://localhost:3000](http://localhost:3000).

## Usage

### Endpoints

- **Get all tasks**: `GET /tasks`
- **Create a new task**: `POST /tasks`
  - **Parameters**: `title` (string), `description` (text), `completed` (boolean)
- **Update a task**: `PUT /tasks/:id`
- **Delete a task**: `DELETE /tasks/:id`

### Example Requests

- **Create a Task**:
  ```bash
  curl -X POST http://localhost:3000/tasks -d "task[title]=Sample Task&task[description]=Sample description&task[completed]=false"
  ```

- **Get All Tasks**:
  ```bash
  curl http://localhost:3000/tasks
  ```

## Additional Notes

- This is an API-only Rails app, meaning it does not have a frontend.
- Tests have not been added yet.

---