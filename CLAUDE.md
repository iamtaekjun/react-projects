# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a React application built with Vite, featuring:
- React 19.1.1 with modern hooks (useState, etc.)
- Vite as the build tool and development server
- ESLint for code linting with React-specific rules
- Standard React project structure with JSX components

## Development Commands

```bash
# Start development server with hot module replacement
npm run dev

# Build for production
npm run build

# Run ESLint to check code quality
npm run lint

# Preview production build locally
npm run preview
```

## Code Architecture

### Project Structure
- `src/main.jsx` - Application entry point, renders App component with React 18+ createRoot
- `src/App.jsx` - Main application component with basic counter functionality
- `src/App.css` - Component-specific styles for App
- `src/index.css` - Global styles with light/dark theme support
- `public/` - Static assets (Vite logo)
- `index.html` - HTML template with root div

### Styling Approach
- Uses CSS files imported directly into components
- Global styles in `index.css` include CSS custom properties for theming
- Supports both light and dark color schemes via `prefers-color-scheme`
- Component-specific styles in separate CSS files (e.g., `App.css`)

### ESLint Configuration
- Uses modern flat config format (`eslint.config.js`)
- Configured for React with hooks and refresh plugins
- Custom rule: `no-unused-vars` with pattern for uppercase constants
- Ignores `dist` directory for production builds

## Development Notes

- Uses Vite's fast refresh for instant updates during development
- Components use `.jsx` extension
- ESM modules throughout (type: "module" in package.json)
- No TypeScript currently configured (uses plain JavaScript)
- No testing framework currently set up