# Roomwise - CS651 Website Project

Roomwise is a room-planning frontend adapted from Sean Farmer's Launchpad starter. The original Git history and attribution are retained. The current implementation demonstrates the Project 1 frontend requirements with sample data; real authentication, photo analysis, and backend services are deferred.

## Frontend and local preview

The application remains in `CS651_Part1_Launchpad/` so existing paths keep working:

```sh
cd CS651_Part1_Launchpad
npm ci
npm run build
npm start
```

Open <http://localhost:3000>. See the [frontend README](CS651_Part1_Launchpad/README.md) for the planner walkthrough, component structure, and asset attribution.

| Folder | Purpose |
| --- | --- |
| `public/` | Home, About, Contact, minimal React host pages, shared CSS, and images |
| `src/` | React App, Sign In, shared components, and Bootstrap JavaScript entry points |
| `dist/` | Generated browser-ready site, including bundled React and Bootstrap |

Edit `public/` and `src/`, then rebuild `dist/`. Run npm commands inside the frontend folder; the repository root is not an npm application. Do not run `generate-pages.py` over the adapted pages, as it contains the original starter content.

## Reusing the build for Parts 2 and 3

The existing structure supports both hosting methods without rebuilding the frontend architecture. Use the **contents** of `CS651_Part1_Launchpad/dist/` as the web root, so `index.html`, `app.html`, `login.html`, `assets/`, and `images/` keep their relative paths.

- **Part 2:** Add a `DockerContainer/` folder containing the Apache Docker build and deployment instructions. Apache will serve the compiled `dist/` content; Node is needed during compilation, not as the production web server.
- **Part 3:** Upload the compiled `dist/` contents to the S3 website root. App navigation uses URL fragments (`app.html#editor`, `app.html#saved`), so it does not need server-side route rewrites. S3 hosts the built site, not JSX or Node programs.

The course assignment requires separate Part 2 and Part 3 GitHub submission repositories and wikis. Each must include the frontend source and supporting files as well as real deployment evidence. This development repository supplies the shared frontend; its folder structure alone does not complete either deployment.

Required wiki pages are `Docker Creation`, `YouTube Link`, and `Special Issues` for Part 2 (including the Special Issues PDF), and `S3 Bucket Setup` and `YouTube Link` for Part 3. Deployment URLs, AWS screenshots, videos, costs, and cloud configuration remain pending. No AWS infrastructure is included in this frontend change.

Assignment: <https://borg.csueastbay.edu/~grewe/CS651/Projects/Project1New.html>
