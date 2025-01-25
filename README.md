# Task Tracker

## Table of contents
- [Description](#description)
- [Installation](#installation)
- [Features](#features)
  - [Create task](#create-task)
  - [Update task](#update-task)
  - [Delete task](#delete-task)
  - [Show tasks](#show-tasks)


## Description

A simple task tracker application built with php based as an exercise from https://roadmap.sh/projects/task-tracker. This application is built with php and it uses a json file to store the tasks.


## Installation

Run the next command in root folder in order to make it executable.
```bash
$ chmod +x task-tracker
```

Now you can execute command like this:
```bash
$ ./task-tracker
```


## Features

The tracker must be able to create, update, delete and show tasks. To see full available commands you can run "task-tracker help" and it will show you the available commands.
```bash
$ ./task-tracker help

Usage: task-manager <command>
Available commands:
  list                                            - List all tasks
  list    <'done'|'pending'|'in-progress'>        - List tasks based in status
  add     <task-description>                      - Add a new task
  remove  <task-id>                               - Remove a task
  update  <task-id> <new-description>             - Remove a task
```

## Create task

In order to create a task
```bash
$ ./task-tracker add "Lorem ipsum dolor"

Task added succesfully (ID: 1)
```


## Update task

In order to update a task description you shoul run the command "task-tracker update \<task-id> \<new-description>".

```bash
$ ./task-tracker update 1 "Lorem ipsum dolor sit amet"

Task updated succesfully (ID: 1)
```


## Delete task

In order to delete a task you should run the command "task-tracker delete \<task-id>".

```bash
$ ./task-tracker delete 1

Task deleted succesfully (ID: 1)
```

## Show tasks
In order to show a list of tasks you should run the command "task-tracker list". This will output the list of tasks with their id, description, status and last uptate date.

```bash
$ ./task-tracker list

List of all tasks: 
1 - Command to add task (pending) - (2025-01-24 23:54:17.689552)
2 - Command to update task (done) - (2025-01-24 23:54:51.607128)
3 - Command to remove task (in-progress) - (2025-01-25 00:33:56.007356)
4 - Command to list all tasks (in-progress) - (2025-01-25 00:33:58.035494)
5 - Command to list tasks with given status (in-progress) - (2025-01-25 00:33:59.787877)
```


And also you can add a parameter to filter the list of tasks with the status.
```bash
$ ./task-tracker list pending

List of tasks with status pending:
1 - Command to add task (pending) - (2025-01-24 23:54:17.689552)
````
```bash
$ ./task-tracker list in-progress

List of tasks with status in-progress:
3 - Command to remove task (in-progress) - (2025-01-25 00:33:56.007356)
4 - Command to list all tasks (in-progress) - (2025-01-25 00:33:58.035494)
5 - Command to list tasks with given status (in-progress) - (2025-01-25 00:33:59.787877)
```
```bash
$ ./task-tracker list done

Output
List of tasks with status done: 
2 - Command to update task (done) - (2025-01-24 23:54:51.607128)
```
