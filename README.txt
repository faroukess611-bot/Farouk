# FAROUK STUDIO — AI Chat deployment

This package connects the website chat widget to the OpenAI Responses API through a Vercel serverless function. The API key is kept on the server, not in the browser.

## Deploy from a phone

1. Create an OpenAI API key at https://platform.openai.com/api-keys. API usage may require billing/credits; a ChatGPT subscription does not automatically include API credits.
2. Create/sign in to https://vercel.com.
3. Upload this package to a GitHub repository (or import it into Vercel). Keep `index.html`, `api/chat.js`, and `vercel.json` at the project root / matching folders.
4. In Vercel, open the project → Settings → Environment Variables.
5. Add `OPENAI_API_KEY` with your secret API key. Optionally add `OPENAI_MODEL` if your API account uses a different available model.
6. Redeploy the project after saving the environment variable.
7. Open the deployed site and test the chat widget.

## Security
- Never paste the API key into `index.html`, chat messages, or public source control.
- This starter does not include user authentication or rate limiting. Before promoting the site widely, add rate limiting/abuse protection to avoid unexpected API charges.
- If deployment fails, inspect Vercel Function Logs and check the API key, API billing, and model access.

## Files
- `index.html` — site and chat widget
- `api/chat.js` — secure server-side API proxy
- `vercel.json` — Vercel function configuration
