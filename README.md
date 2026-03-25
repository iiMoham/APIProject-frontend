# Frontend — Personality Predictor UI

A static HTML/JS single-page app that sends user input to the Personality Predictor backend API and displays the result.

## Configuration (Required Before Deployment)

Open `index.html` and update the **one line** at the top of the `<script>` block:

```js
// Change this to your deployed backend URL:
const API_URL = "http://127.0.0.1:8000/predict";
//              ^^^ replace with https://api.your-domain.com/predict
```

## Running Locally

You can open `index.html` directly in a browser **or** serve it with a simple HTTP server:

```bash
# Python (built-in)
python -m http.server 3000
# Then open http://localhost:3000
```

## Deployment Options

Because this is a plain static HTML file, it can be deployed for free on any static host:

| Platform       | Command / Steps                                      |
|----------------|------------------------------------------------------|
| **Netlify**    | Drop the `frontend/` folder into the Netlify dashboard |
| **GitHub Pages** | Push `frontend/` to a repo and enable Pages        |
| **Nginx**      | Copy `index.html` to `/var/www/html/`               |
| **Vercel**     | `vercel --cwd frontend/`                            |
| **AWS S3**     | Upload `index.html` to a public S3 bucket           |

## Notes

- No build step required — pure HTML, Tailwind CDN, and vanilla JS.
- Make sure the backend server has CORS configured to allow requests from this frontend's origin.
