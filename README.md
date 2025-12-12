# React TanStack Start + ShadCN UI + Bulletproof React Boilerplate

This repository is a fully structured starter template for building modern React applications using **TanStack Start**, **ShadCN UI**, and **Bulletproof React architecture**. The boilerplate is designed for scalability, maintainability, and clean separation of concerns.

---

## Table of Contents
1. [Project Structure](#project-structure)
2. [Installation](#installation)
3. [Available Scripts](#available-scripts)
4. [Features](#features)
5. [Routing](#routing)
6. [Folder Breakdown](#folder-breakdown)
7. [ShadCN UI Integration](#shadcn-ui-integration)
8. [Hooks & API Management](#hooks--api-management)
9. [Utilities](#utilities)
10. [Types](#types)
11. [Best Practices](#best-practices)
12. [Deployment](#deployment)

---

## Project Structure
```
src/
  components/
    custom-ui/          # Custom reusable UI components
    ui/                 # ShadCN UI components
  data/                 # Static/mock data for testing
  features/
    auth/
      api/              # Auth related API calls
      components/       # Auth specific components (login, signup)
      hooks/            # Auth related hooks
      types.ts          # Types for auth
  hooks/                # Global custom hooks
  lib/
    utils.ts            # Reusable utility functions
  navigation/
    paths.ts            # Route paths/constants
  routes/
    (protected)/       # Protected routes that require auth
    (public)/          # Publicly accessible routes
    __root.tsx          # Global root layout (providers, wrappers)
    index.tsx           # Main entry page
  types/                # Global TypeScript types
  utils/                # General purpose utility functions
```

---

## Installation
```bash
# Clone the repo
git clone <repo_url>

# Install dependencies
npm install

# Start the development server
npm run dev
```

---

## Available Scripts
| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with HMR |
| `npm run build` | Create production build (Vite) |
| `npm run preview` | Preview production build locally |

---

## Features
- **TanStack Start** for full-stack React with server components support
- **ShadCN UI** for modern, reusable UI components
- **Bulletproof React Architecture** with feature-based folder organization
- **TypeScript** for type safety
- **File-based routing** with route grouping (`(public)`, `(protected)`)
- **Server-side loaders** for SSR routes
- **Custom hooks** for data fetching and state management

---

## Routing
- **File-based routing**: All routes live under `src/routes/`
- **Route Groups**: `(public)` and `(protected)` for grouping without affecting URL
- **Root layout**: `__root.tsx` contains global providers, header/footer, and `<Outlet />`
- **Nested Layouts**: `_layout.tsx` files inside a route folder provide layout for all child routes
- **Dynamic Routes**: Use `$param` in file names, e.g., `src/routes/users/$userId.tsx`

---

## Folder Breakdown
### `components/`
- `ui/` → ShadCN-based UI components (Button, Input, Card, etc.)
- `custom-ui/` → custom reusable components not part of ShadCN

### `features/`
- **Feature-first architecture**: Each module (auth, users, etc.) has its own folder containing API calls, components, hooks, and types
- Example: `features/auth` includes login/signup forms, auth hooks, and API functions

### `hooks/`
- Global hooks used across features, e.g., `useToast`, `useModal`

### `lib/`
- Utility functions shared across the project

### `navigation/`
- Centralized route paths and constants for maintainability

### `routes/`
- **(public)** → Pages accessible without authentication
- **(protected)** → Pages requiring authentication
- `__root.tsx` → Global layout wrapper with providers
- `index.tsx` → Home page entry point

### `types/`
- Shared TypeScript interfaces and types for consistency across the project

### `utils/`
- Helper functions and generic utilities

---

## ShadCN UI Integration
- Installed and initialized ShadCN UI
- Customization of components can be done inside `src/components/ui/`
- Example: `Button.tsx` uses utility `cn` for class merging and Tailwind styling

---

## Hooks & API Management
- Each feature can have its own `hooks` and `api` folder
- Hooks are React Query ready (if needed) for server-side data fetching or local state management
- Example: `features/auth/hooks/useAuth.ts`

---

## Utilities
- `src/lib/utils.ts` → generic utility functions (e.g., `cn` for class names)
- `src/utils/` → app-specific utilities
- `src/navigation/paths.ts` → centralized route constants

---

## Types
- `features/auth/types.ts` → Auth module specific types
- `types/` → global types used across features

---

## Best Practices
- **Feature-based folder structure**: keeps related files together
- **Server-side loaders**: fetch data on the server when possible
- **Reusable components and hooks**: avoid duplication
- **Centralized navigation paths**: easier route maintenance
- **ShadCN UI for consistency**: maintain design consistency across app

---

## Deployment
- Run `npm run build` to create a production build
- Use `npm run preview` to test production build locally
- Deploy `dist/` to a Node.js server or supported hosting

---

This boilerplate is a strong starting point for scalable React applications using TanStack Start, ShadCN UI, and a bulletproof architecture for maintainable, organized, and clean code.
