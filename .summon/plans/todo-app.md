---
status: pending
title: Build a Todo App with React + Vite + TypeScript + Tailwind
---

## Overview
Create a fully functional todo application with add, complete, edit, and delete functionality using React, TypeScript, and Tailwind CSS v4.

## Implementation Steps

### 1. Set up project structure and dependencies
- Create `/app/src/main.tsx` as the entry point
- Create `/app/src/App.tsx` as the root component
- Create `/app/index.html` with a root div for React mounting
- Create `/app/vite.config.ts` with Tailwind CSS v4 plugin
- Create `/app/tsconfig.json` with proper TypeScript configuration
- Create `/app/package.json` with React 19, Vite, TypeScript, and Tailwind CSS v4 dependencies
- **Expected outcome**: Project structure ready with all dependencies installed

### 2. Create global styles
- Create `/app/src/styles/global.css` starting with `@import "tailwindcss";`
- Import global styles in `/app/src/main.tsx` before rendering
- **Expected outcome**: Tailwind CSS is available throughout the app

### 3. Create types for todo data
- Create `/app/src/types/todo.ts` with a `Todo` interface containing `id`, `title`, `completed`, and `createdAt` properties
- **Expected outcome**: Type safety for todo data throughout the app

### 4. Create a custom hook for todo management
- Create `/app/src/hooks/useTodos.ts` with state management for todos
- Implement functions to: add a todo, delete a todo, toggle completion status, and update todo text
- Use `localStorage` to persist todos between page reloads
- **Expected outcome**: All todo logic is centralized and reusable

### 5. Create a TodoItem component
- Create `/app/src/components/TodoItem.tsx` to display individual todos
- Show todo text, a checkbox to mark complete/incomplete, an edit button, and a delete button
- Include an inline edit mode where users can modify the text
- **Expected outcome**: Each todo displays with all actions available

### 6. Create a TodoInput component
- Create `/app/src/components/TodoInput.tsx` with an input field and "Add" button
- Allow users to type a new todo and press Enter or click the button to add it
- Clear the input field after adding
- **Expected outcome**: Users can add new todos easily

### 7. Create a TodoList component
- Create `/app/src/components/TodoList.tsx` to display all todos
- Map through todos and render a `TodoItem` for each
- Show a message if there are no todos
- **Expected outcome**: All todos are displayed in a clean list

### 8. Build the main App component
- Create `/app/src/App.tsx` with the main layout
- Import and use the `useTodos` hook for state management
- Include `TodoInput` and `TodoList` components
- Add a header and simple styling with Tailwind
- Include stats showing total todos and completed todos
- **Expected outcome**: All components work together in a functional app

### 9. Add sorting and filtering options
- Add buttons or a select dropdown to filter todos (all, active, completed)
- Update the display based on selected filter
- **Expected outcome**: Users can view todos by status

### 10. Test and refine
- Verify all CRUD operations work (add, view, edit, delete, complete)
- Test localStorage persistence across page reloads
- Check responsive design on mobile and desktop
- **Expected outcome**: Fully functional todo app ready to use
