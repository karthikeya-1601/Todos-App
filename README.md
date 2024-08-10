
This project is a simple to-do list application that allows users to add, delete, and mark tasks as completed. The tasks are stored locally using the browser's `localStorage`, ensuring that the list persists even after the page is refreshed.

## Features

- **Add Tasks:** Users can add a new task to the list.
- **Delete Tasks:** Users can remove tasks from the list.
- **Mark as Complete:** Users can mark tasks as completed, which toggles a visual indication (e.g., strikethrough).
- **Persistent Storage:** The to-do list is saved in `localStorage`, so it persists across page reloads.

## Technologies Used

- **HTML:** The structure of the application.
- **CSS:** Basic styling for the to-do list and buttons.
- **JavaScript:** The core functionality of the app, including adding, deleting, and managing tasks, as well as interacting with `localStorage`.

## Code Overview

### Main Components

1. **HTML Structure**
   - `todoItemsContainer`: The container where to-do items are appended.
   - `addTodoButton`: The button to add a new to-do item.
   - `saveTodoButton`: The button to save the current state of the to-do list.

2. **JavaScript Functions**
   - **`getTodoListFromLocalStorage()`**: Fetches the to-do list from `localStorage`. If no list is found, it returns an empty array.
   - **`onAddTodo()`**: Handles the addition of a new to-do item. It creates a new to-do object, appends it to the list, and updates the UI.
   - **`onTodoStatusChange(checkboxId, labelId, todoId)`**: Toggles the completion status of a to-do item.
   - **`onDeleteTodo(todoId)`**: Deletes a to-do item from the list and updates the UI.
   - **`createAndAppendTodo()`**: Dynamically creates and appends a to-do item to the DOM.

3. **Event Listeners**
   - The `addTodoButton` is tied to the `onAddTodo()` function, allowing users to add tasks.
   - The `saveTodoButton` is tied to saving the current state of the list to `localStorage`.

### Initial Load

Upon loading the app, the `getTodoListFromLocalStorage()` function is called to populate the to-do list from `localStorage`. Each item is rendered using the `createAndAppendTodo()` function.

## How to Use

1. **Add a Task:** Type a task into the input field and click "Add Todo".
2. **Mark as Complete:** Click the checkbox next to a task to mark it as complete.
3. **Delete a Task:** Click the trash icon next to a task to delete it.
4. **Save Tasks:** Click the "Save Todo" button to save the current state of the to-do list.

