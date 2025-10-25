Collaborative Task Manager – Java & JavaScript Implementations
Overview

This project implements a Collaborative Task Management System in both Java and JavaScript (Node.js).
It is a command-line interface (CLI) application that allows multiple users to:

- Create and assign tasks

- Track task completion

- Categorize and prioritize work

- View tasks by user or category

The goal of the project is to demonstrate object-oriented design, modular programming, and data persistence in two different programming languages.

Core Features

- Create users
- Create tasks (title, description, category, priority)
- Assign tasks to users
- Mark tasks as complete
- List all tasks
- Filter tasks by user or category
- Help command to list available commands

Java Implementation

Files

- TaskManager.java
- Task.java
- User.java
- MainApp.java
- StorageManager.java

How It Works

Task.java: Represents a single task with ID, title, description, category, priority, assigned user, and completion status.

User.java: Represents a user who can be assigned tasks.

TaskManager.java: Core logic — manages users, tasks, and provides methods for creating, assigning, and listing.

MainApp.java: The CLI interface that handles command parsing and user input.

Running the Java Version

Open a terminal in the project directory.

Compile all Java files:

javac *.java


Run the main program:

java Main


Use the following commands:

- create-user <username>
- create-task <title>|<description>|<category>|<priority>
- list
- list-user <username>
- list-category <category>
- assign <taskId> <username>
- complete <taskId>
- help
- exit

JavaScript Implementation (Node.js)

Files
- app.mjs
- TaskManager.js
- storage.js
- package.json

How It Works

TaskManager.js: Contains the TaskManager class handling all business logic (users, tasks, assignment, listing).

storage.js: Manages persistence using JSON file storage (simulates a small local database).

app.mjs: CLI entry point that uses Node.js inquirer to interact with the user.

package.json: Configures dependencies and start scripts.

Setup Instructions

Ensure Node.js
 is installed.

Initialize the project:

npm init -y


Install dependencies:

npm install inquirer


Ensure your package.json contains:

{
 
  "name": "collab-todo",
 
  "version": "1.0.0",
 
  "type": "module",
 
  "scripts": {
  
    "start": "node app.mjs"
 
  },
  
  "dependencies": {
 
    "inquirer": "^9.2.7"
 
  }

}


Start the program:

npm start

Commands (for both versions)

Command	                                                        → Description

- create-user <username>	Creates a new user
- create-task <title>|<description>|<category>|<priority>	       → Creates a new task
- list	                                                          → Lists all tasks
- list-user <username>	                                          → Lists all tasks assigned to a specific user
- list-category <category>	                                      → Lists tasks in a given category
- assign <taskId> <username>	                                    → Assigns a task to a user
- complete <taskId>	                                             → Marks a task as completed
- help	                                                          → Shows available commands
- exit	                                                          → Exits the application
