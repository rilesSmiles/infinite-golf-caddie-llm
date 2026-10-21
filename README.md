# Caddie: Infinite Golf chatbot backend

Backend for the Odin AI Chatbot Framer component. Free to run on OpenRouter.

## Files
- `api/chat.js`: the endpoint the Framer widget talks to (`/api/chat`)
- `knowledge.js`: everything Caddie knows. Edit this to update answers.

## Deploy (about 5 minutes)
1. Go to github.com, click **New repository**, name it `infinite-golf-chatbot`, and create it.
2. Click **uploading an existing file** and drag in everything from this folder (keep the `api` folder intact). Commit.
3. On vercel.com, click **Add New > Project**, import the repo, and hit **Deploy**.
4. Get a free key at openrouter.ai (profile > Keys > Create Key).
5. In Vercel: **Settings > Environment Variables**, add `OPENROUTER_API_KEY` with your key.
6. **Deployments**, then the three dots on the latest one, then **Redeploy**.
7. Visit `https://<your-project>.vercel.app/api/chat` in a browser. You should see `"keyConfigured": true`.
8. Make sure **Settings > Deployment Protection** has Vercel Authentication turned off for production, or the widget can't reach it.

## Connect Framer
In the Odin AI Chatbot component properties:
- **Backend URL**: `https://<your-project>.vercel.app/api/chat`
- **Assistant Name**: `Caddie`

## Free tier limits
OpenRouter free models allow 50 requests per day until you've bought $10 of credits (one time), which raises it to 1,000 per day. For a launch week, the $10 is worth it.

## Updating Caddie
Edit `knowledge.js` on GitHub (pencil icon) and commit. Vercel redeploys automatically.
