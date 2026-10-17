# BizGuard + AI assistant

## Run it
1. Install Node.js (nodejs.org), then in this folder run:  npm install
2. Copy .env.example to a new file named .env and paste your API key
   (get one at platform.openai.com > API keys)
3. npm start
4. Open http://localhost:3000 and use the chat button

Never commit .env to GitHub and never paste the key into index.html.
If the AI call fails, the chat falls back to built-in answers, so the demo never breaks.

## Using Claude (Anthropic) instead of GPT
npm install @anthropic-ai/sdk, put ANTHROPIC_API_KEY in .env, and in server.js replace the client and call with:

    const Anthropic = require('@anthropic-ai/sdk');
    const client = new Anthropic({ apiKey: process.env.ANTHROPIC_API_KEY });
    // inside the route, `system` is a separate field and messages must not include a system role:
    const r = await client.messages.create({
      model: 'claude-sonnet-5-5', max_tokens: 400,
      system: SYSTEM + '\nBusiness data (live): ' + String(context).slice(0, 4000),
      messages: [...history.slice(-6).map(h => ({ role: h[0]==='Owner'?'user':'assistant', content: String(h[1]) })), { role: 'user', content: question }],
    });
    res.json({ text: r.content[0].text });

## Putting it online for the competition
Deploy this folder to Render, Railway or Fly.io (free tiers exist). Add OPENAI_API_KEY as an
environment variable in their dashboard instead of using a .env file. Set a spending limit on your API account.
