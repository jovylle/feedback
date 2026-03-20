# feedback.uft1.com
<img width="1142" height="722" alt="image" src="https://github.com/user-attachments/assets/ace2e866-72bf-48db-91f1-0b7a2721c198" />

Static feedback page that submits to Web3Forms.

## Files
- `index.html`: page + Web3Forms form
- `styles.css`: styling

## Deploy
Host as a static site at `feedback.uft1.com` (any static hosting works):
- Put `index.html` and `styles.css` at the site root.
- Ensure `index.html` is served as the default document.

## Form handling
Submissions POST to `https://api.web3forms.com/submit` using the embedded `access_key`.

