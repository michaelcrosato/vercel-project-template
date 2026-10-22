# Vercel project template

Start new projects from this template so Vercel never builds on every push.

What's included:

- `vercel.json` turns off automatic Git deployments. Pushing to GitHub builds nothing.
- `CLAUDE.md` tells every agent to deploy only when asked, and exactly how: through the
  Vercel connector, building the latest `main` to production.

The last deployment stays live at its normal URL until you ask for a new one.

## Starting a new project

1. On GitHub, click **Use this template** and create your new repo.
2. Import the repo into Vercel as usual. The import does one initial deployment.
3. In your first session in the new repo, the agent fills in the project names in
   `CLAUDE.md`. After that, just say "deploy" whenever you want a new build.
