# To-Do List Application

This is a simple To-Do List application built with HTML, CSS, and JavaScript. The app allows users to add, delete, and mark tasks as completed. It also stores the to-do list in the browser's local storage, so the list is saved even after the page is refreshed.

## Features

- **Add To-Do**: Users can add new tasks to the list by typing in the input field and clicking the "Add" button.
- **Mark as Completed**: Users can mark a task as completed by clicking the checkbox next to the task. The task text is then visually marked with a strikethrough.
- **Delete To-Do**: Users can delete a task by clicking the trash icon next to the task.
- **Persistent Storage**: The to-do list is saved in the browser's local storage, so the list remains even if the user closes the browser or refreshes the page.

## Code Overview

### HTML

The basic structure of the application is created using HTML. The main elements include:

- An input field for users to type their tasks.
- "Add" and "Save" buttons for adding tasks and saving the list to local storage.

### CSS

Styling is handled by an external CSS file (not included in this code snippet). It includes styles for:

- The layout and appearance of the to-do list.
- Visual indicators for completed tasks (e.g., strikethrough for text).
- A responsive design that adapts to different screen sizes.

### JavaScript

The main functionality of the app is implemented in JavaScript. Key components include:

#### 1. Getting To-Do List from Local Storage

```javascript
function getTodoListFromLocalStorage() {
    let stringifiedTodoList = localStorage.getItem("todoList");
    let parsedTodoList = JSON.parse(stringifiedTodoList);
    return parsedTodoList === null ? [] : parsedTodoList;
}
