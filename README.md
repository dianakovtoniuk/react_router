# React Router Demo

A small React + TypeScript app showing client-side routing with React Router: a shared layout, nested routes, dynamic route params and an error page.

## Features

- Root layout with a persistent navigation bar and an `Outlet` for page content
- Routes for the home page, the products list and a product details page
- Dynamic route `/products/:productId` read with `useParams`
- Active link highlighting with `NavLink`
- Programmatic navigation with `useNavigate`
- Relative links (`relative="path"`) for going back one level
- Custom error page for unknown routes via `errorElement`

## Tech Stack

- React 19
- TypeScript
- React Router (`react-router-dom`)
- Create React App (`react-scripts`)
- CSS Modules

## Routes

| Path | Page |
| --- | --- |
| `/` | Home |
| `/products` | Products list |
| `/products/:productId` | Product details |
| any other path | Error page |

## Project Structure

```
src/
├── App.tsx                    # router configuration
├── index.tsx                  # app entry point
├── components/
│   └── MainNavigation.tsx     # header navigation with active link styles
└── pages/
    ├── Root.tsx               # shared layout
    ├── Home.tsx               # home page
    ├── Products.tsx           # products list
    ├── ProductDetail.tsx      # product details page
    └── Error.tsx              # error page
```

## Getting Started

1. Clone the repository

```bash
   git clone https://github.com/KovtoniukDiana/<repo-name>.git
   cd <repo-name>
```

2. Install dependencies

```bash
   npm install --legacy-peer-deps
```

3. Start the dev server

```bash
   npm start
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

> `--legacy-peer-deps` is needed because `react-scripts@5` has not been updated for React 19 peer dependencies.

## Scripts

| Command | Description |
| --- | --- |
| `npm start` | Run the app in development mode |
| `npm run build` | Create a production build |
| `npm test` | Run tests |
