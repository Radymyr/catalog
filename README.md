# Nice Gadgets Catalog

A responsive single-page product catalog built with React + TypeScript.

The app includes category browsing, product details, favorites, cart management, theme/language switching, and URL-driven filtering/sorting/pagination.

## Live Demo

https://radymyr.github.io/catalog/

## Main Features

- Product catalog by categories: phones, tablets, accessories
- Product details page with gallery, color/capacity variant navigation, and specifications
- Favorites and cart with quantity management
- Search by product name (debounced)
- Sorting (newest, alphabetically, cheapest)
- Pagination and items-per-page controls
- Theme switcher (`dark` / `light`) with persistence in `localStorage`
- Language switcher (`en` / `ua`) with UI dictionary support
- Responsive layout with mobile menu and sliders (Swiper)
- Not-found and empty-state screens

## Tech Stack

- React 18
- TypeScript
- React Router (`HashRouter`)
- SCSS Modules + global SCSS
- Swiper
- Bulma + Font Awesome
- Vite

## Project Structure

```text
src/
  components/        # Reusable UI components
  pages/             # Route pages (Home, Catalog, ProductDetails, Favorites, Cart)
  providers/         # Global providers (state + app settings)
  hooks/             # URL/state hooks (pagination, sorting, per-page)
  utils/             # Data access and helper functions
  types/             # Shared TypeScript types
public/
  api/               # Local JSON product data
  img/, fonts/       # Static assets
```

## Getting Started

### Prerequisites

- Node.js 20+
- npm 9+

### Installation

```bash
npm install
```

### Run in Development

```bash
npm start
```

### Build for Production

```bash
npm run build
```

## Available Scripts

- `npm start` - run dev server
- `npm run build` - build production bundle
- `npm run lint` - run style format, Prettier, ESLint, and Stylelint
- `npm run lint-js` - run JS/TS linting
- `npm run lint-css` - run style linting
- `npm run style-format` - auto-fix SCSS styles with Stylelint
- `npm run format` - format TS/TSX files with Prettier
- `npm run deploy` - deploy to GitHub Pages (via `mate-scripts`)

## Data and State

- Catalog data is loaded from local JSON files in `public/api`.
- Cart and favorites are persisted in `localStorage` (`cartIds`, `favoritesIds`).
- Theme and language preferences are persisted in `localStorage` (`app_theme`, `app_language`).
- Sorting/pagination/search state is reflected in URL query params.

## Deployment Notes

For GitHub Pages deployment:

1. Update `homepage` in `package.json` from `"."` to your repository page URL/path.
2. Build and deploy:

```bash
npm run deploy
```

## License

This project is distributed under the terms of the [MIT License](LICENSE).
