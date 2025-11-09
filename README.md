<!--
	Improved README for a learning-focused Next.js + TypeScript project.
	Keep this high-level, include quick start, project map, learning goals and exercises.
-->

# next.js_learning — Learn Next.js + TypeScript

This repository is a small learning project for exploring Next.js (App Router) with TypeScript. It was created from the standard Next.js starter and trimmed to highlight the parts most useful when learning how Next.js + TypeScript apps are structured and developed.

The project intentionally keeps things simple so you can focus on the framework concepts, TypeScript ergonomics, and the developer experience.

## Goals

- Provide a minimal, hands-on Next.js + TypeScript example using the App Router (`app/`).
- Demonstrate common patterns: pages/routes, layouts, global styles, and a basic example page in `printforge/`.
- Offer exercises and suggestions to practice and extend the app.

## Tech stack

- Next.js (App Router)
- TypeScript
- PostCSS (see `postcss.config.mjs`)
- Vercel for easy deployment (optional)

## Quick start

1. Install dependencies:

```bash
# npm
npm install

# or yarn
yarn

# or pnpm
pnpm install
```

2. Start the development server:

```bash
npm run dev
# or `yarn dev` / `pnpm dev`
```

3. Open http://localhost:3000 in your browser. Changes to files under `app/` will hot-reload.

Common useful scripts (from `package.json`):

- `dev` — run the app in development mode
- `build` — create an optimized production build
- `start` — run the production server after `build`
- `lint` — run the linter (if configured)

## Project layout (key files)

Top-level files/folders you will frequently interact with:

- `app/` — Next.js App Router directory (routes, layouts, pages). The entry page is `app/page.tsx`.
- `app/layout.tsx` — root layout used across routes.
- `app/globals.css` — global CSS imports and base styles.
- `app/printforge/page.tsx` — example route included with this learning project.
- `public/` — static assets (images, icons).
- `next.config.ts` — Next.js configuration.
- `tsconfig.json` — TypeScript configuration.
- `postcss.config.mjs` — PostCSS setup.

Explore `app/` to see how routes and layouts are composed. If you add a new folder under `app/` with a `page.tsx`, it automatically becomes a new route.

## Learning exercises (suggested)

Work through these to learn important Next.js + TypeScript concepts:

1. Edit `app/page.tsx` to change the homepage content. Observe HMR (hot module replacement).
2. Add a new nested route: create `app/examples/hello/page.tsx` and visit `/examples/hello`.
3. Convert a component to use TypeScript types and props. Add a small interface and prop validation.
4. Create a dynamic route (e.g., `app/posts/[id]/page.tsx`) and read the route param using the App Router conventions.
5. Add a simple API route (if you prefer the Pages Router for APIs, create `pages/api/` or use Next.js server functions).
6. Add a CSS module or Tailwind/CSS-in-JS to practice styling approaches.

Each exercise helps materialize how Next.js handles routing, server rendering, and client components.

## Tips & notes

- This project uses the App Router (`app/`) — it differs from the Pages Router (`pages/`) in routing conventions and data fetching. See the Next.js docs for details.
- TypeScript is enabled by `tsconfig.json`. When adding new files, use `.tsx` for React components.
- If you run into type errors, run `npm run build` to see stricter errors that may not appear during `dev`.

## Troubleshooting

- If the dev server doesn't start, ensure dependencies are installed and your Node.js version meets Next.js requirements.
- If CSS or fonts don't load, check `app/layout.tsx` and `globals.css` for import paths.
- For build-time errors, run `npm run build` and inspect the console for the first failing file — the stack usually points to the exact file and line.

## Deploying

Deploying to Vercel is straightforward — connect the repository and Vercel will detect Next.js and set up build settings automatically. See https://vercel.com/new.

## Next steps (recommended)

- Try converting one or two pages to use server components and client components to see the difference in behavior.
- Add a small form and validate it with TypeScript types and runtime checks.
- Add tests (Jest + React Testing Library or Playwright) to practice testing pages/components.

---

If you'd like, I can:

- add a short CONTRIBUTING or DEVELOPMENT note with exact `npm` scripts from your `package.json`,
- create a small example component with TypeScript props, or
- add a few tests and CI workflow examples.

Tell me which of these you'd like next and I'll apply the change.
