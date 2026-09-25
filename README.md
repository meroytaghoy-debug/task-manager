<img width="1920" height="1008" alt="6e76044b-cb8f-4aa4-a3c4-7af90b5cca9f" src="https://github.com/user-attachments/assets/ccbaaa5a-16e8-4659-b3dc-9a44899d63a9" /># Personal Task Manager (Laravel Mini Project)

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
<img width="1920" height="1008" alt="6b52ee6e-c358-45ab-a0e6-70bec09d6752" src="https://github.com/user-attachments/assets/f974f339-1866-48e9-8e3c-ab69937d27cf" />
<img width="1920" height="1008" alt="7615b052-5149-4855-a46e-1d270b43d90c" src="https://github.com/user-attachments/assets/fa82c907-dd54-4a67-b8cb-9d0918235b75" />
<img width="1920" height="1008" alt="6e76044b-cb8f-4aa4-a3c4-7af90b5cca9f" src="https://github.com/user-attachments/assets/3cb2c5eb-fea0-4006-a40e-46be3000562d" />

<img width="1920" height="1008" alt="94bad37a-15a4-4ce2-a805-00ffd9b8990f" src="https://github.com/user-attachments/assets/9970e003-499f-47c6-8ce3-d32530cf2a19" />
<img width="1920" height="1008" alt="7615b052-5149-4855-a46e-1d270b43d90c" src="https://github.com/user-attachments/assets/57e8b324-d765-49d6-b5ed-73df4850ca04" />








