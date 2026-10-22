## Deploying to Vercel

Vercel does NOT auto-deploy from GitHub, on purpose. Pushing to GitHub never deploys.

Why: every Vercel build costs build minutes, and every deployment is stored and billed
daily. I only look at a tiny fraction of builds, so building on every push wasted money
on deployments nobody saw. The last deployment stays live until I ask for a new one.

Rules:
- Never deploy unless I explicitly ask in this session.
- Never re-enable automatic deployments or change "deploymentEnabled" in vercel.json.
- Never use the pause button, deploy hooks, or the Vercel CLI to deploy.

First-time setup: if the values below still contain `<...>` placeholders, fill them in
before the first deploy. Use the Vercel connector to find the project linked to this
repo (team: michaelcrosato-1122's projects), and this repo's GitHub owner and name.
Commit the filled-in values to main. If no Vercel project exists for this repo yet,
create one only when I ask, then fill in the values.

How to deploy (the only method):
Call the Vercel connector's create_deployment with:
- team: michaelcrosato-1122's projects
- project: <PROJECT_NAME>
- gitSource: type "github", org "<GITHUB_OWNER>", repo "<REPO_NAME>", ref "main"
- target: "production"
Then wait for the build to finish and report the result and the live URL.
