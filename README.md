# Cloud AI — GitHub Pages

Upload `index.html` to a GitHub repository and enable GitHub Pages.

## Important
This is a static browser app. It does **not** make an API key secret. Never hard-code a real key in the HTML or commit it to GitHub.

The UI expects an OpenAI-compatible endpoint:
`POST <base>/chat/completions`

The provider must also permit browser CORS requests. A provider-specific Claude/Anthropic API may require an adapter/backend instead of direct browser calls.

Features:
- Cloud-style chat UI
- New chat / clear
- Local chat history
- Model dropdown
- API URL + API key settings on first open
- Text messaging
- Browser speech-to-text voice input
- Mobile responsive layout
- No API key embedded in source
