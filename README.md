# AI Code Review Platform

A fullstack web application that leverages Google Gemini AI to provide automated, high-quality code reviews. The platform consists of a React frontend and an Express backend, enabling users to submit code snippets and receive detailed, AI-generated feedback and suggestions for improvement.

---

## Features

- **AI-Powered Code Review:**
  - Uses Google Gemini AI to analyze and review code for quality, best practices, performance, security, and maintainability.
- **Modern UI:**
  - React-based interface with a code editor and syntax highlighting.
- **Instant Feedback:**
  - Submit code and receive structured, actionable feedback in seconds.
- **REST API:**
  - Simple POST endpoint for code review requests.

---

## Tech Stack

- **Frontend:** React, Vite, PrismJS, React Simple Code Editor, React Markdown
- **Backend:** Node.js, Express, Google Generative AI SDK, dotenv, CORS

---

## Project Structure

```
code-review/
  ├── BackEnd/      # Express backend (API, AI integration)
  └── Frontend/     # React frontend (UI, code editor)
```

---

## Getting Started

### Prerequisites
- Node.js (v18+ recommended)
- npm or yarn
- Google Gemini API key (for backend)

### 1. Clone the Repository
```bash
git clone <repo-url>
cd code-review
```

### 2. Setup Backend
```bash
cd BackEnd
npm install
```

Create a `.env` file in `BackEnd/` with the following:
```
GOOGLE_GEMINI_KEY=your_google_gemini_api_key
```

Start the backend server:
```bash
node server.js
```
The backend runs on **http://localhost:3000** by default.

### 3. Setup Frontend
```bash
cd ../Frontend
npm install
npm run dev
```
The frontend runs on **http://localhost:5173** by default (Vite).

---

## Usage

1. Open the frontend in your browser: [http://localhost:5173](http://localhost:5173)
2. Enter or paste your code snippet in the editor.
3. Click the **Review** button.
4. View the AI-generated review and suggestions on the right panel.

---

## API Reference

### POST `/ai/get-review`
- **Request Body:**
  - `code` (string): The code snippet to review.
- **Response:**
  - AI-generated review and suggestions (string/markdown).

---

## Environment Variables

### Backend (`BackEnd/.env`)
- `GOOGLE_GEMINI_KEY` – Your Google Gemini API key (required)

### Frontend
- No environment variables required by default.

---

## Customization & Extending
- You can modify the backend to support additional AI models or review criteria.
- Frontend can be extended with more languages, themes, or collaborative features.

---

## License

This project is licensed under the ISC License.

---

## Acknowledgements
- [Google Generative AI](https://ai.google.dev/)
- [React](https://react.dev/)
- [Vite](https://vitejs.dev/)
- [PrismJS](https://prismjs.com/) 