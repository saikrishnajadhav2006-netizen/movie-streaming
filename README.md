# Aniplex — Movie Discovery & Web Technology Lab

A responsive anime/movie discovery website built as a practical lab project. The interface is branded **Aniplex** and includes a home page, demo login, student registration, searchable catalogue, XML/DTD data, and Fetch API demonstrations.

> **Coursework scope:** Weeks 1–10 are integrated into this website. Weeks 11–15 (TypeScript and Angular) should live in a separate repository and are intentionally not bundled into this project.

## Run locally

Fetch API requires HTTP rather than opening `index.html` directly via `file://`.

**VS Code:** install/use Live Server, right-click `index.html`, choose **Open with Live Server**.

**Python alternative:**
```bash
python -m http.server 5500
```
Then open `http://localhost:5500`.

## Pages and features

- **Home:** featured collection and project introduction.
- **Sign in:** browser-only demonstration login.
- **Register:** client-side validation for name, email, password length, and matching passwords.
- **Explore:** 100 Indian films across Telugu, Tamil, Malayalam, Kannada, Hindi, Bengali, Marathi, Punjabi, Assamese, and Odia cinema; search, language and genre filters.
- **Movie details:** select a film to view its cast and open a JustWatch India availability search or YouTube trailer search. Aniplex does not host copyrighted video.
- **Posters:** poster thumbnails are looked up from Wikipedia page images at runtime; unavailable images use a designed fallback. Internet access is required.
- **Lab Experiments:** Week 1–10 experiment log plus buttons for text, JSON, XML, and POST demonstrations.

## Experiment index

| Week | Experiment title | Implementation |
|---|---|---|
| 1 | Home & Login Pages | Semantic HTML, navigation, static page views |
| 2 | Student Registration Form | HTML form fields and browser constraints |
| 3 | CSS Styling | External CSS in `styles.css`; inline/internal CSS explained in the experiment notes |
| 4 | JavaScript Form Validation | DOM events, email checks, password matching, localStorage demo |
| 5 | Movie Catalogue | Movie data, card rendering, search, genre filter |
| 6 | XML Book Data & DTD | `books.xml` and `books.dtd` |
| 7 | Review & Skill Test 1 | Manual test checklist below |
| 8 | Fetch API — Load Text | Fetches `sample.txt` asynchronously |
| 9 | Fetch API — Parse JSON/XML | Fetches `movies.json`; parses `books.xml` using DOMParser |
| 10 | Fetch API — POST Data | Sends JSON to JSONPlaceholder using POST |

## Week 7 manual test checklist

- [ ] Home, Explore, Lab Experiments, Sign in, and Register navigation works.
- [ ] Registration rejects blank name/email, invalid email, short passwords, and password mismatch.
- [ ] Valid demo registration can sign in in the same browser.
- [ ] Catalogue search and genre filter update results.
- [ ] Load text, Parse JSON, and Parse XML buttons display parsed data.
- [ ] POST button reports the API response or a clear network error.
- [ ] Layout remains usable on narrow/mobile screens.
- [ ] Validate the XML with a DTD-capable XML validator.

## Important limitations

- This is a **front-end learning prototype**, not a real streaming service. This is a discovery catalogue, not a licensed streaming service. Availability links search JustWatch India; trailer links search YouTube. Actual playback is provided only by rights-holding services.
- Login and registration use browser `localStorage` for demonstration only. The demo stores the password in plain text, so **never use real credentials**. A production application needs a backend, password hashing, HTTPS, secure sessions, and a database.
- Week 10 uses the public JSONPlaceholder testing API and requires internet access.
- Some browsers restrict XML external DTD resolution. Use a dedicated XML validator to validate `books.xml` against `books.dtd`.

## Suggested structure

```text
movie-streaming/
├── index.html
├── styles.css
├── app.js
├── movies.json
├── sample.txt
├── books.xml
├── books.dtd
└── README.md
```
