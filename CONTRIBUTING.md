# Contributing to IGDTUWHub 👩‍💻✨

We are absolutely thrilled that you are looking to contribute to **IGDTUWHub**! This platform is designed by students, for students, and it grows stronger with every update, resource, or fix provided by the community.

Please take a moment to review this guide to understand the development workflow and how to get your contributions successfully merged.

---

## 🗺️ Table of Contents
1. [Code of Conduct](#code-of-conduct)
2. [How Can I Contribute?](#how-can-i-contribute)
   - [Adding / Updating Academic Resources (Notes & PYQs)](#adding--updating-academic-resources-notes--pyqs)
   - [Adding / Editing Societies](#adding--editing-societies)
   - [Fixing Bugs or Requesting Features](#fixing-bugs-or-requesting-features)
3. [Local Development Setup](#local-development-setup)
4. [Coding Conventions & Style Guide](#coding-conventions--style-guide)
5. [Pull Request Checklist](#pull-request-checklist)

---

## 💜 Code of Conduct

To foster an inclusive, safe, and supportive environment for all student contributors, please maintain respectful and encouraging communication in issues, PR discussions, and comments.

---

## 💡 How Can I Contribute?

### Adding / Updating Academic Resources (Notes & PYQs)
The academic resources (course titles and subjects) are declared dynamically in `script.js` within the `branches` constant configuration object.

To update courses:
1. Open `script.js` and locate the `branches` object.
2. Locate the target branch key (e.g., `cse-ai`, `it`, `aiml`).
3. Under the appropriate year and semester array, append the exact title of the subject:
   ```javascript
   "1st Semester": [
     "Probability and Statistics",
     "Environmental Sciences",
     // Add your subject title here
   ]
   ```
4. If you have links to digital notes, Google Drive resources, or PYQs PDFs, trace the load handler inside `script.js` or submit them in an issue so we can attach them to the academic link configurations.

### Adding / Editing Societies
The searchable societies directory is driven by the `societiesData` array in `script.js`.

To add your society or club:
1. Locate `societiesData` array in `script.js`.
2. Add a new object following this schema:
   ```javascript
   {
     name: "Society Name",
     category: "Technical" | "Cultural" | "Media" | "Literary" | "Sports",
     type: "Society Focus area (e.g., Web3, Drama, Coding)",
     desc: "A short, engaging paragraph describing the society.",
     link: "https://www.instagram.com/your_handle/",
     image: "Direct URL to your society logo (Cloudinary, Imgur, etc.)"
   }
   ```
3. Test your society in the search filter on the site.

### Fixing Bugs or Requesting Features
- If you find a bug (e.g., incorrect calculations, UI overflows, broken calendar dates), feel free to open an issue or directly create a pull request with the fix!
- For new features (e.g., adding a CGPA trend tracker chart, new games, dark/light theme options), please open an issue first to discuss the implementation plan.

---

## 🛠️ Local Development Setup

To work on your changes locally:

1. **Fork the repository** on GitHub.
2. **Clone your fork** to your local machine:
   ```bash
   git clone https://github.com/your-username/IGDTUWhub.git
   ```
3. Make your edits inside `index.html`, `style.css`, or `script.js`.
4. Run a local web server to check your changes:
   - Python: `python -m http.server 8000`
   - Node: `npx serve`
5. Open your browser and navigate to `http://localhost:8000` (or the indicated port) to test the website dynamically.

---

## 🎨 Coding Conventions & Style Guide

- **HTML:** Use clean, descriptive semantic HTML elements (e.g., `<section>`, `<header>`, `<main>`, `<footer>`). Ensure all new form elements have unique IDs.
- **CSS Style Rules:**
  - Avoid inline styles.
  - Rely on CSS variables defined in `:root` for color styling.
  - Maintain a clean CSS hierarchy. Make sure media queries are placed logically at the bottom of the file for responsiveness.
- **JavaScript (JS):**
  - Keep variable declarations close to their first usage.
  - Prefer modern ES6 features (e.g. `const`/`let`, arrow functions, `for...of`, template literals).
  - Use standard spacing: 2 spaces for indentation.
  - Run syntax checks locally via Node before committing:
    ```bash
    node --check script.js
    ```

---

## 📝 Pull Request Checklist

Before submitting your pull request, ensure your branch checks off all these items:
- [ ] Code compiles and runs fine locally without any browser console errors.
- [ ] No temporary debugging scripts or files are left in the commit.
- [ ] The README file has been updated if any new library integrations were added.
- [ ] Your commit messages are clear, concise, and descriptive (e.g., `feat: added AI Club to societies directory` or `fix: corrected grade points calculation in getGpaPoint`).
