# feedback.uft1.com
<img width="1142" height="722" alt="image" src="https://github.com/user-attachments/assets/ace2e866-72bf-48db-91f1-0b7a2721c198" />

Static feedback page that submits to Web3Forms.

## Usage
- General feedback: `https://feedback.uft1.com/`
- Context-specific feedback: `https://feedback.uft1.com/?context=sunflower-land-digging-assistant`

The page shows a neutral general-feedback state with no query string. When a `context` slug is present, the page switches into a dedicated context-specific mode and derives the visitor-facing label from that slug.

## Files
- `index.html`: page + Web3Forms form
- `about/index.html`: about page served at `/about/`
- `styles.css`: styling

Example slugs:
- `chat-widget`
- `portfolio`
- `sunflower-land-digging-assistant`

The page derives the visible label from the `context` slug automatically.
`sunflower-land-digging-assistant` becomes `Sunflower Land digging assistant`.

## Deploy
Host as a static site at `feedback.uft1.com` (any static hosting works):
- Put `index.html` and `styles.css` at the site root.
- Ensure `index.html` is served as the default document.

## Form handling
Submissions POST to `https://api.web3forms.com/submit` using the embedded `access_key`.

## Context rules
- Use a single `context` query parameter for the slug.
- Example slugs: `chat-widget`, `portfolio`, `sunflower-land-digging-assistant`.
- The UI converts the slug to a readable label automatically.
