# Goal Tracker CLI App

A simple command-line interface (CLI) application to manage and track your personal goals. Built with Node.js and Inquirer.js, this app allows you to create, manage, and track the completion of your goals with an interactive terminal interface.

## Features

- 🎯 Create new goals
- 📋 List all goals with interactive selection
- ✅ Mark goals as completed
- 📊 View completed goals
- 🔓 View pending (open) goals
- 🗑️ Delete goals
- 💾 Automatic data persistence to JSON file

## Prerequisites

- Node.js (version 18 or higher)
- npm (Node package manager)

## Installation

1. Clone or download this repository to your local machine
2. Navigate to the project directory:
   ```bash
   cd /path/to/iniciante - app
   ```
3. Install the required dependencies:
   ```bash
   npm install
   ```

## Usage

To run the application, execute the following command in your terminal:

```bash
node index.js
```

The app will start with a welcome message and present you with a menu of options.

## Menu Options

The application provides the following menu options:

### 1. Cadastrar meta (Register goal)

- Allows you to add a new goal to your list
- Simply type your goal when prompted
- Goals are automatically saved to the JSON file

### 2. Listar metas (List goals)

- Displays all your registered goals
- Use arrow keys to navigate between goals
- Press space to mark/unmark goals as completed
- Press Enter to confirm your selections

### 3. Metas realizadas (Completed goals)

- Shows a list of goals you've marked as completed
- Displays the count of completed goals

### 4. Metas abertas (Open goals)

- Shows a list of goals that are still pending
- Displays the count of open goals

### 5. Deletar metas (Delete goals)

- Allows you to select and remove goals from your list
- Select the goals you want to delete using space and Enter

### 6. Sair (Exit)

- Exits the application
- All changes are automatically saved before exiting

## File Structure

- `index.js` - Main application file containing all the logic and UI
- `metas.json` - Data file that stores your goals and their completion status
- `package.json` - Contains project dependencies (inquirer)
- `aula.md` - Course notes about programming concepts
- `todo.md` - List of implemented features
- `README.md` - This documentation file

## How It Works

The application uses Node.js's built-in file system module to persist data between sessions. When you start the app:

1. It attempts to load existing goals from `metas.json`
2. If the file doesn't exist, it initializes an empty list
3. All changes are automatically saved to the JSON file
4. The inquirer library provides an interactive command-line interface

## Data Persistence

All your goals are stored in the `metas.json` file in the following format:

```json
[
  {
    "value": "Goal description",
    "checked": true/false
  }
]
```

The `checked` property indicates whether the goal has been completed (true) or is still pending (false).

## Troubleshooting

- If the app fails to start, ensure you have Node.js installed and run `npm install` to install dependencies
- If goals are not saving, check that you have write permissions to the project directory
- Make sure the `metas.json` file has the correct format if edited manually

## About

This application was created as part of a learning exercise to understand:

- Node.js fundamentals
- Asynchronous programming with async/await
- File system operations
- Interactive CLI interfaces
- Data persistence with JSON
