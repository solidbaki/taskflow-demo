# TaskFlow — React + TypeScript demo

A focused portfolio project demonstrating practical frontend patterns from the role description.

## Stack
- React + TypeScript strict mode
- Redux Toolkit Query for query/mutation state and cache invalidation
- `tailwind-variants` for typed component variants
- Zod for form validation
- Tailwind CSS + Vite

## Features
- Search tasks and filter by status
- Create tasks with Zod validation
- Mark tasks completed or reopen them
- Reusable Button and status badge variants
- Responsive dashboard with loading, error, and empty states

## Run locally
Requires Node.js 18+.

```bash
npm install
npm run dev
npm run build
```

## Architecture notes
- `src/taskTypes.ts` defines task status types and the creation schema.
- `src/tasksApi.ts` keeps data access and mutations outside UI components. It uses in-memory mock data, so data resets on refresh.
- `src/components/button.tsx` demonstrates typed `intent` and `size` variants with `tailwind-variants`.
- RTK Query tags invalidate the task list after mutations.
- `src/App.tsx` handles presentation and composes query/mutation hooks.

## Suggested code file for review
Use `src/components/button.tsx` to discuss `tailwind-variants`, typed props, and reusable UI patterns. Also be prepared to explain `src/tasksApi.ts`.

## Scope
This is a frontend demo, not a production service. It uses local mock data rather than a persistent API. A production version would connect the query functions to HTTP endpoints and add automated tests and server-side validation.
