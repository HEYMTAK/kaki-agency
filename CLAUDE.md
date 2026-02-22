# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm install        # Install dependencies
npm run dev        # Start dev server (http://localhost:5173)
npm run build      # Type-check and build for production (output: dist/)
npm run preview    # Preview the production build locally
npm run lint       # Run ESLint
```

## Architecture

This is a **React + Vite + TypeScript** agency showcase site.

- `index.html` — entry point, Vite injects the React app here
- `src/main.tsx` — mounts `<App />` into `#root`
- `src/App.tsx` — root component, top-level routing and layout go here
- `src/App.css` / `src/index.css` — global styles

TypeScript is split across three configs:
- `tsconfig.json` — references the two below
- `tsconfig.app.json` — for `src/` (browser target)
- `tsconfig.node.json` — for `vite.config.ts` (Node target)

## Stack

- **Vite** for bundling and HMR
- **React 19** with TypeScript strict mode
- **ESLint** with `@eslint/js` + `typescript-eslint` + `eslint-plugin-react-hooks`
