# Roamwise

AI-first road trip planner with state-specific questions, small-town home-base suggestions, and day-trip routing estimates.

## Deploy on Render

1. Create a **Web Service** from this repository's **main** branch.
2. Runtime: **Node**. Root directory: leave blank. Build command: `echo ready`. Start command: `node server.js`.
3. Create a Gemini API key at https://aistudio.google.com/apikey and set Render environment variable `GEMINI_API_KEY` to that private key. Optional: `GEMINI_MODEL=gemini-2.5-flash-lite`. Select a project/model eligible for Gemini's free tier. Do not add the key to GitHub.
4. Deploy and open your Render URL.

Requires Node.js 20+. Gemini offers rate-limited free-tier usage for eligible projects/models; this application does not fall back to a paid provider. Provider billing and free-tier eligibility depend on the Google project. Rate limits can cause temporary errors. Never commit API keys.

## Caveats

This is a development prototype. AI-generated locations may be inaccurate. Road times use public Nominatim/OSRM demo services and are computed between **town centers**, not verified attraction entrances. Some routing checks can fail or be unavailable. Check attraction hours, costs, accessibility, road closures and availability independently. Memory is stored only in the same browser; no user accounts or cross-device sync. The AI does not yet optimize multi-stop routes, enforce a complete daily driving budget, or book accommodations.
