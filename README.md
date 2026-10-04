# Gift Genie 🧞

Gift Genie is an AI-powered web application that generates personalized gift recommendations. Users provide details about the recipient—such as their interests, hobbies, occasions, and budget—and the application returns curated suggestions formatted cleanly in real time.

---

## Features

- **AI-Driven Suggestions:** Sends natural language prompts to a backend endpoint (`/api/gift`) to generate relevant gift recommendations.
- **Markdown Parsing:** Uses `marked` to convert Markdown-formatted text responses from the AI into structured HTML.
- **XSS Protection:** Integrates `DOMPurify` to sanitize parsed HTML before injecting it into the DOM, preventing Cross-Site Scripting vulnerabilities.
- **Interactive UI & Feedback:** Features dynamic state handling, including an animated magic lamp loading indicator while suggestions are generated.

---

## Tech Stack

- **Frontend:** Vanilla JavaScript (ES6+), HTML5, CSS3
- **Backend:** Node.js (`server.js`)
- **Build Tool:** Vite
- **Libraries:**
  - [`marked`](https://marked.js.org/) (Markdown parser)
  - [`DOMPurify`](https://github.com/cure53/DOMPurify) (HTML sanitization)

---

## Project Structure

```text
├── assets/
│   ├── genie.svg
│   └── lamp.svg
├── index.html        # Main markup and input interface
├── index.js          # Client-side form handling, API request, and DOM rendering
├── server.js         # Backend server handling AI API routes
├── style.css         # Styling and loading animations
├── utils.js          # Helper and utility functions
├── vite.config.js    # Vite configuration
└── package.json      # Project dependencies and npm scripts
