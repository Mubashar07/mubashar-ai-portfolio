# Mubashar Ayub — AI Automation & Software Engineering Portfolio

A responsive, sci-fi inspired personal portfolio built with Vue 3 and Vite. It includes animated AI visuals, an interactive agent selector, services, workflow steps, projects, skills, about and contact sections.

## Run locally

1. Install Node.js (LTS): https://nodejs.org/
2. Extract this ZIP and open the project folder in VS Code.
3. Open a terminal in the project folder and run:

   ```bash
   npm install
   npm run dev
   ```

4. Open the local URL shown in the terminal (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
npm run preview
```

The production site is generated in `dist/`.

## Deploy to GitHub Pages

1. Create a new GitHub repository and upload the project files (do not upload `node_modules`).
2. In the repository, open **Settings → Pages** and choose **GitHub Actions** as the build/deployment source.
3. Add `.github/workflows/deploy.yml` (included in this project) if it is not already present.
4. Push to the `main` branch. GitHub Actions will build the Vue app and publish the `dist` folder.

## Personalize before publishing

Search in `src/App.vue` for these placeholders and replace them with your real details:

- `hello@example.com` — email address
- `https://wa.me/000000000000` — WhatsApp link in international format, digits only
- LinkedIn and GitHub links in the footer
- Project descriptions, stacks and links — use real projects and verified outcomes only
- The About section's experience and stats, if you want to make those claims more specific

The design uses a locally bundled hero image and CSS-generated sci-fi visuals, so the main artwork does not depend on an external image host. Google Fonts are loaded online; system fallbacks are included.
