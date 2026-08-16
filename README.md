# Cloud AI — GitHub Pages

This is a single-file, Cloud-style Claude-compatible chat UI.

## Included
- First-open API URL + API key screen
- Save & Test connection
- Claude model picker
- `claude-opus-5-thinking`
- `claude-opus-4-8-thinking`
- Custom model ID
- New chat / clear
- Local chat history
- Text chat
- Image attachments
- PDF attachments
- Text/code/JSON/CSV/etc. attachments
- Browser speech-to-text
- Mobile responsive UI

## API format expected

The page expects an Anthropic Messages-compatible gateway:

`POST <BASE_URL>/v1/messages`

Headers:
- `x-api-key: YOUR_KEY`
- `anthropic-version: 2023-06-01`

If the Base URL already ends in `/v1`, the page uses `/messages` directly.

For example, entering:

`https://tabitoken.com`

causes the page to call:

`https://tabitoken.com/v1/messages`

The exact endpoint must be supported by your gateway.

## GitHub Pages
Upload `index.html` to the root of your repository, then enable GitHub Pages from Settings → Pages → Deploy from branch → `main` → `/ (root)`.

## Important
The API key is entered at runtime and kept in `sessionStorage`; it is NOT written into `index.html`.

This is still a browser app. Your API gateway must allow CORS requests from your GitHub Pages origin. If the gateway blocks CORS, a static-only GitHub Pages app cannot bypass that restriction; a backend/proxy is required.

Do not put a real API key in the repository.
