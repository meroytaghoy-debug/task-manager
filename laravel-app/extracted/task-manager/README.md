# Personal Task Manager (Laravel Mini Project)

Project Code: WST21-PM-2026-SF
Student Name: Xavier Ammeer Q. Taghoy
Course & Year: BSIT 2
Database Used: MySQL

## Features
- Add Task
- View Tasks
- Edit Task
- Delete Task
- Update Status (Pending / Completed)

## Tech Stack
- Laravel (Routes → Controller → Model → Blade)
- MySQL database
- Bootstrap 5 for styling

## Project Structure

This repo contains only the application-specific files layered on top of a
standard Laravel installation:

```
app/Models/Task.php
app/Http/Controllers/TaskController.php
database/migrations/2024_01_01_000000_create_tasks_table.php
routes/web.php
resources/views/layouts/app.blade.php
resources/views/tasks/index.blade.php
resources/views/tasks/create.blade.php
resources/views/tasks/edit.blade.php
```

## Setup Instructions

1. **Create a fresh Laravel project** (skip this if you already have one):
   ```bash
   composer create-project laravel/laravel task-manager
   cd task-manager
   ```

2. **Copy the files from this repo** into the matching folders of your
   Laravel project, overwriting `routes/web.php`.

3. **Configure your `.env` file** for MySQL:
   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=task_manager
   DB_USERNAME=root
   DB_PASSWORD=
   ```
   Create the `task_manager` database in MySQL (e.g. via phpMyAdmin or the
   `mysql` CLI) before running migrations.

4. **Generate your app key** (first time only):
   ```bash
   php artisan key:generate
   ```

5. **Run the migration** to create the `tasks` table:
   ```bash
   php artisan migrate
   ```

6. **Start the development server**:
   ```bash
   php artisan serve
   ```

7. Open **http://127.0.0.1:8000** in your browser. The root URL redirects
   straight to the task list at `/tasks`.

## How It Works

- **Routes** (`routes/web.php`) — `Route::resource('tasks', TaskController::class)`
  wires up all CRUD routes (index, create, store, edit, update, destroy) in
  one line, plus an extra `PATCH /tasks/{task}/status` route for the one-click
  status toggle.
- **Controller** (`TaskController.php`) — handles validation and talks to the
  `Task` model for every CRUD action.
- **Model** (`Task.php`) — Eloquent model for the `tasks` table, with
  `task_name`, `description`, `status`, and `due_date` as mass-assignable
  fields.
- **Database** — a single `tasks` migration defines the schema described in
  the project brief.
- **Blade Views** — `index` (task list with a "Mark as Pending/Completed"
  button per row), `create`, and `edit` forms, all extending a shared
  `layouts/app.blade.php` with Bootstrap styling.

## Screenshots

_Add screenshots of your running app here before submitting._
