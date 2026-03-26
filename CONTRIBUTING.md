# Contributing to Elevate

Thank you for your interest in contributing! This document covers everything you need to get started.

---

## Code of Conduct

Be respectful and constructive. This project welcomes contributors of all backgrounds and experience levels.

---

## How to Contribute

### Reporting a Bug

1. Check [existing issues](../../issues) to avoid duplicates
2. Open a new issue and include:
   - A clear, descriptive title
   - Steps to reproduce
   - Expected vs actual behaviour
   - Browser and OS details

### Suggesting a Feature

Open an issue with the label `enhancement`. Describe the feature, why it would be useful, and any implementation ideas you have.

### Submitting a Pull Request

1. **Fork** the repository
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/elevate-resume-builder.git
   cd elevate-resume-builder
   ```
3. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```
4. **Make your changes** — see the Development Guidelines below
5. **Test** your changes in the browser (Chrome, Safari, and Firefox)
6. **Commit** with a clear message:
   ```bash
   git commit -m "Add: brief description of what you added"
   git commit -m "Fix: brief description of what you fixed"
   ```
7. **Push** to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
8. **Open a Pull Request** against `main` — fill in the PR template with a description and screenshots where relevant

---

## Development Guidelines

### Running Locally

No build step required. Serve the files with Python:

```bash
python3 -m http.server 3571
```

Then open [http://localhost:3571](http://localhost:3571).

### File Structure

The entire application lives in two HTML files:

| File | Contents |
|------|----------|
| `index.html` | All React components, CSS, and utility functions |
| `guide.html` | Static user guide page |

All React components are defined inside the `<script type="text/babel">` block in `index.html`. There is no build pipeline — changes are visible on browser refresh.

### Code Style

- **Indentation:** 2 spaces
- **Components:** Functional React components only (no class components)
- **State:** `React.useState` / `React.useEffect` via CDN globals
- **CSS:** CSS custom properties (`var(--name)`) for all colours and shared values — see the `:root` block at the top of the `<style>` tag
- **Naming:** camelCase for JS variables and functions, kebab-case for CSS class names
- **Strings:** Australian English spelling throughout — colour, organise, résumé, behaviour, etc.
- **Comments:** Only where logic is non-obvious

### Adding a New Step or Component

1. Define the component function inside the `<script type="text/babel">` block
2. Add it to the `App` function's render logic using the `step` state variable
3. Update the `Header` component's `steps` array if the step count changes
4. Document the new step in `guide.html`

### Colour Palette

Only use colours from the defined palette — do not introduce new hex values:

```css
--bg:     #EDF2FB   /* page background */
--s1:     #E2EAFC   /* card backgrounds */
--s2:     #D7E3FC   /* secondary elements */
--s3:     #CCDBFD   /* borders */
--a1:     #C1D3FE   /* tags, chips */
--a2:     #B6CCFE   /* hover states */
--accent: #ABC4FF   /* buttons, active states */
--ink:    #1E1B4B   /* headings */
--body:   #374151   /* body text */
--muted:  #6B7280   /* secondary text */
```

---

## What We're Looking For

Good first contributions:

- Additional Australian job boards
- More certifications in the `CERT_DB` array
- Improved ATS scoring algorithm
- Better keyword extraction logic
- Accessibility improvements (ARIA labels, keyboard navigation)
- Additional discovery questions in `genDiscoveryQs`
- Browser compatibility fixes

---

## Questions?

Open an issue tagged `question` and we'll get back to you.
