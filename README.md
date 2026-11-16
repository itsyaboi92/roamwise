# Roamwise

AI-first road trip planner with state-specific questions, small-town home-base suggestions, and day-trip routing estimates.

## Deploy on Render

1. Create a **Web Service** from this repository's **main** branch.
2. Runtime: **Node**. Root directory: leave blank. Build command: `echo ready`. Start command: `node server.js`.
3. Create a free-tier GroqCloud key at https://console.groq.com/keys and set Render environment variable `GROQ_API_KEY` to that private key. Optional: `GROQ_MODEL=openai/gpt-oss-120b`. Do not add the key to GitHub.
4. Deploy and open your Render URL.

Requires Node.js 20+. GroqCloud offers a rate-limited free tier; no paid API is configured or used by this application. Rate limits can cause temporary errors. Never commit API keys.

## Caveats

This is a development prototype. AI-generated locations may be inaccurate. Road times use public Nominatim/OSRM demo services and are computed between **town centers**, not verified attraction entrances. Some routing checks can fail or be unavailable. Check attraction hours, costs, accessibility, road closures and availability independently. Memory is stored only in the same browser; no user accounts or cross-device sync. The AI does not yet optimize multi-stop routes, enforce a complete daily driving budget, or book accommodations.
