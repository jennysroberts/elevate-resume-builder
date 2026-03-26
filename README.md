# Elevate — Resume Builder

A professional, ATS-optimised résumé builder designed for the Australian job market. Built as a zero-dependency, browser-based web app — no install, no account, no data sent anywhere.

![Elevate Screenshot](https://img.shields.io/badge/version-1.0.0-ABC4FF?style=flat-square) ![License](https://img.shields.io/badge/license-MIT-B6CCFE?style=flat-square) ![Platform](https://img.shields.io/badge/platform-macOS%20%2F%20Web-C1D3FE?style=flat-square)

---

## Features

- **LinkedIn Import** — Export your LinkedIn profile as PDF and paste the text, or enter your history manually
- **ATS Optimisation** — Extracts up to 24 keywords from any job description and scores your résumé against them in real time
- **Three Smart Prompts** — Guided Research, Template, and Discovery prompts that mirror what professional résumé writers do
- **Experience Discovery** — Conversational interview that surfaces achievements and side projects you may have overlooked
- **Live Resume Builder** — Split-view editor with a formatted document preview that updates as you type
- **ATS Score Gauge** — Animated score (0–97) broken down by keywords, action verbs, metrics, and completeness
- **Australian English** — Colour, organise, programme, analyse — correctly throughout
- **Australian Job Boards** — One-click search on SEEK, Indeed AU, LinkedIn, Jora, CareerOne, and Adzuna with your role pre-filled
- **Certification Recommendations** — Role-matched online certifications ranked by income impact
- **Print to PDF** — One-click export of a clean, A4-formatted résumé document
- **Zero Dependencies** — No npm, no build step, no server required. Runs from a single HTML file

---

## Getting Started

### Option 1 — Open directly (quickest)

```bash
open index.html
```

### Option 2 — Serve locally (recommended for full functionality)

```bash
python3 -m http.server 3571
```

Then open [http://localhost:3571](http://localhost:3571) in your browser.

### Option 3 — Deploy to any static host

Upload `index.html` and `guide.html` to GitHub Pages, Netlify, Vercel, or any web server. No build step required.

---

## Usage

The app guides you through five steps:

| Step | Screen | What you do |
|------|--------|-------------|
| 1 | **Profile** | Import from LinkedIn or enter your work history, education, and skills |
| 2 | **Job Target** | Paste the job description for ATS keyword extraction |
| 3 | **Customise** | Three prompts — research keywords, choose a template, discover hidden experience |
| 4 | **Builder** | Edit your résumé with a live preview and ATS score |
| 5 | **Search** | Launch targeted job searches and explore relevant certifications |

Full walkthrough: open [`guide.html`](guide.html) or click **📖 How to Use** in the app.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| UI Framework | React 18 (via CDN) |
| Transpiler | Babel Standalone (via CDN) |
| Styling | Pure CSS — custom properties, Flexbox, Grid |
| Typography | [Manrope](https://fonts.google.com/specimen/Manrope) (Google Fonts) |
| Runtime | Browser only — no Node.js, no bundler |
| Storage | In-memory only — no data leaves the device |

---

## Project Structure

```
elevate-resume-builder/
├── index.html    # Complete application — all components, styles, and logic
├── guide.html    # Step-by-step user guide
├── README.md     # This file
└── LICENSE       # MIT
```

---

## Colour Palette

| Name | Hex | Usage |
|------|-----|-------|
| Alice Blue | `#EDF2FB` | Page background |
| Lavender | `#E2EAFC` | Card backgrounds |
| Lavender | `#D7E3FC` | Secondary elements |
| Lavender | `#CCDBFD` | Borders, dividers |
| Periwinkle | `#C1D3FE` | Tags, chips |
| Periwinkle | `#B6CCFE` | Hover states |
| Baby Blue Ice | `#ABC4FF` | Primary buttons, accents |

---

## Browser Support

Works in all modern browsers (Chrome, Safari, Firefox, Edge). Optimised for macOS but fully functional on Windows and Linux.

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

[MIT](LICENSE) — free to use, modify, and distribute.
