# Personal Task Manager (Laravel Mini Project)

Project Code: WST21-PM-2026-SF
Student Name: Xavier Ammeer Q, Taghoy
Course & Year: BSIT 2
Database Used: SQLite

## Features
- Add Task
- View Tasks
- Edit Task
- Delete Task
- Update Status (Pending / Completed)

## Tech Stack
- Laravel (Routes → Controller → Model → Blade)
- SQLite database
- Bootstrap 5 for styling

## How It Works

- **Routes** (`routes/web.php`) — Route::resource wires up all CRUD routes
  (index, create, store, edit, update, destroy), plus an extra PATCH route
  for the one-click status toggle.
- **Controller** (`TaskController.php`) — handles validation and talks to
  the `Task` model for every CRUD action.
- **Model** (`Task.php`) — Eloquent model for the `tasks` table.
- **Database** — a migration defines the `tasks` table schema (task_name,
  description, status, due_date).
- **Blade Views** — `index` (task list with status toggle buttons),
  `create`, and `edit` forms, extending a shared Bootstrap layout.

## Screenshots

_Add screenshots of your running app here._