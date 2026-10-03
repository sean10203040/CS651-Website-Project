# CS651 Project 1 — Part 1

Author: Sean Farmer
Theme: Launchpad, a general workspace frontend.

## Open on Windows
1. Extract this entire ZIP.
2. Install Node.js LTS if it is not already installed.
3. Open the extracted folder in VS Code (or your preferred editor).
4. Open a terminal/PowerShell in that folder.
5. Run `npm install`.
6. Run `npm run build`.
7. Run `npm start`.
8. Open http://localhost:3000 in your browser. Keep the terminal open. Press Ctrl+C to stop.

A prebuilt `dist` folder is included. With Node installed, `npm start` can serve it without rebuilding. Do not open React JSX files directly in the browser. The public HTML pages reference the compiled assets in dist.

## What to edit
- `public/index.html`: traditional Home page.
- `public/about.html`: traditional About page.
- `public/contact.html`: traditional Contact page. Replace the class contact wording with your preferred contact method if desired.
- `public/styles.css`: shared CSS, spacing, borders, padding, responsive rules.
- `public/images/workspace.svg`: original local workflow graphic on every page.
- `src/components.jsx`: reusable React components.
- `src/workspace.jsx`: React App page and state.
- `src/login.jsx`: React login/create-account forms and state.
- `src/static.js`: Bootstrap JavaScript for the static pages' responsive navbar.
- `public/app.html` and `public/login.html`: minimal React host pages.

Run `npm run build` after edits. `generate-pages.py` was used to create the initial static HTML; you do not need to run it. Re-running it overwrites those HTML files.

## Assignment requirements
| Requirement | Implementation |
|---|---|
| Home, About, Contact | Separate traditional HTML pages |
| App as a React SPA | app.html mounts workspace.jsx |
| Three reusable components, excluding App | Navigation, Footer, PageHeading, StatCard, WorkspaceCard, FilterBar, FormField |
| Component composition | App composes Navigation, StatCard, WorkspaceCard, FilterBar, Footer, etc. |
| State management | useState tracks card saves, category, view, checklist, login, and account fields |
| SPA navigation | Explore and Saved hash navigation; browser back/forward supported |
| Bootstrap responsiveness | Bootstrap grid, navbar-expand-md, collapse plugin, responsive columns |
| Two GUI interactions | Bootstrap mobile menu; React save/filter/checklist interactions |
| Graphics on every page | Local SVG workflow image; React renders image on App and Login |
| CSS box model | Shared stylesheet uses margin, border, padding, width, and responsive grid |
| React-only visible Login UI | login.html contains only the root div and script; components render all visible UI |
| Create-account behavior | Name, email, login, password form appears on right on desktop; stacks below on mobile; Enter removes it and fills original login/password |

## Try it
1. Resize to a narrow mobile width. Open/close the hamburger navigation.
2. Open App. Save a card. The counter increases; visit Saved.
3. Filter categories; toggle a saved card off; try an empty category.
4. Check the getting-started items. The count and progress bar update.
5. Open Login. Click Create account. Fill all four fields with sample details.
6. Click Enter. The account form disappears; login/password populate the original form.
7. Submit Sign in to see the demo response.

## Scope
Part 1 only: no database, backend, real authentication, or account creation. Passwords stay in React memory, are never submitted, and are not written to browser storage. Refresh resets the demo state. Do not use real passwords. Actual App purpose can be determined during the Project 2 proposal.

Bootstrap 5.3.3, React 18.3.1, and esbuild are pinned in package.json with a lockfile. All visual assets and browser dependencies are bundled locally. No CDN is required when viewing the build.

Hosting this preview is not completion of the assignment's AWS/deployment portion. That portion is outside this Part 1 deliverable.
