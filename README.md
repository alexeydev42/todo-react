# To Do List

A React task manager for creating, organizing and tracking everyday tasks.

The application includes search, statistics, persistent storage, theme switching and a layered component structure. It was developed as part of my React practice, with the implementation focused on state management, component composition and reusable application logic.

[Live demo](https://alexeydev42.github.io/todo-react/) · [Repository](https://github.com/alexeydev42/todo-react)

## Features

- add new tasks;
- mark tasks as completed;
- delete individual tasks or clear the entire list;
- search tasks by title;
- view task statistics;
- jump to the first incomplete task;
- switch between light and dark themes;
- UI animations when tasks are added or removed;
- persistent task data in the deployed version.

## Tech stack

- React 19
- JavaScript
- SCSS Modules
- Vite
- Context API
- `useReducer`
- custom hooks
- JSON Server
- Local Storage
- ESLint
- GitHub Pages

## Application structure

The project is organized into several layers:

```text
src/
├── app/
├── entities/
├── features/
├── pages/
├── shared/
└── widgets/
```

The structure is inspired by Feature-Sliced Design.

Task data and related logic are placed in `entities`, user actions are separated into `features`, reusable UI and API code are kept in `shared`, and the main application interface is assembled in `widgets`.

## State management

Task state is managed with `useReducer`, while Context provides task data and actions to the components that need them.

The project also contains custom hooks for:

- task operations;
- persistent storage;
- scrolling to the first incomplete task;
- reusable task-related behavior.

Memoization and stable callbacks are used where appropriate to avoid unnecessary recalculations and keep component responsibilities separated.

## Data storage

The project supports two data sources.

During local development it can work with a JSON Server backend.

The production build used for GitHub Pages switches to a static/local implementation, so the deployed application remains usable without a separate backend.

## Run locally

Clone the repository and install dependencies:

```bash
git clone https://github.com/alexeydev42/todo-react.git
cd todo-react
npm install
```

Start JSON Server:

```bash
npm run server
```

Then, in another terminal, start the application:

```bash
npm run dev
```

## Build

```bash
npm run build
```

## Deployment

The project is deployed with GitHub Pages:

https://alexeydev42.github.io/todo-react/
