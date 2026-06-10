# IGDTUWHub 🚀
> Centralized Academic, Career, and Productivity Hub for Students of Indira Gandhi Delhi Technical University for Women (IGDTUW)

[![Website Link](https://img.shields.io/badge/Live-Demo-brightgreen)](https://igdtuww.github.io/IGDTUWhub/)
[![Contributions-Welcome](https://img.shields.io/badge/Contributions-Welcome-blue.svg)](CONTRIBUTING.md)
[![Tech-Stack](https://img.shields.io/badge/Stack-HTML%20%7C%20CSS%20%7C%20JS-blueviolet)](style.css)

**IGDTUWHub** is a premium, client-side academic portal engineered specifically to streamline resources, boost study productivity, and map career paths for IGDTUW students. It combines course resources, grade management calculators, dynamic scheduling, and interactive break-time tools into a unified, responsive single-page experience.

---

## 🧭 Project Architecture & Directory Layout

The codebase is designed as a lightweight, lightning-fast client-side application using standard web technologies. The clean directory structure is organized as follows:

```
IGDTUWhub/
├── index.html           # Main HTML shell containing responsive nav layout & script mounts
├── style.css            # Custom CSS defining CSS Grid/Flexbox layouts, glassmorphic UI, animations
├── script.js            # Core JS application logic, state, and router handling dynamic content rendering
├── coming-soon.html     # Placeholder page for upcoming features
├── favicon.png          # IGDTUWHub browser tab favicon
├── README.md            # Comprehensive project documentation (This file)
├── CONTRIBUTING.md      # Detailed guidelines for local setup and contributing
└── music/               # Directory containing audio files for games and alerts
    ├── clap.wav         # Sound asset
    └── success.mp3      # Sound asset
```

---

## ⚡ Core Features & Component Breakdown

### 1. 📚 Course & Subject Resources
- **Branch Filtering:** CSE, CSE-AI, IT, ECE, ECE-AI, AIML, MAE, DMAM, MAC.
- **Hierarchical Navigation:** Navigate by Year (1st, 2nd, 3rd, 4th) and Semester (1st, 2nd, etc.) to fetch dedicated notes, syllabus, and Past Year Questions (PYQs).
- **Bookmarks & Saved Courses:** Bookmark favorite courses, which are persisted for instant access on subsequent visits.

### 2. 🧮 Academic Calculators
- **CGPA Calculator (Official IGDTUW Scale):**
  Calculate exact CGPA using course credits and marks based on the university's academic grading standard:
  | Marks (%) | Grade | Grade Point |
  | :--- | :--- | :--- |
  | **93 - 100** | A+ | **10** |
  | **85 - 92** | A | **9** |
  | **77 - 84** | B+ | **8** |
  | **69 - 76** | B | **7** |
  | **61 - 68** | C+ | **6** |
  | **53 - 60** | C | **5** |
  | **45 - 52** | D | **4** |
  | **Below 45** | F | **0** |
- **Advanced Target Calculator:**
  Estimate target SGPAs required over future semesters. Enter your target cumulative CGPA and select your graduation semester horizon to discover exactly what average SGPA you must maintain to reach your goal.

### 3. 📅 Interactive Event & Academic Calendar
- **Interactive Calendar Grid:** Dynamically view month-by-month calendars for 2023, 2024, 2025, and 2026.
- **Preloaded Academic Schedule:** Contains pre-loaded official university events, mid-semester/end-semester examination dates, orientations, fests (Innerve, Taarangana), fests dates, and holiday listings.
- **Custom Personal Events:** Add custom personal events to the calendar (with description and date) and easily manage/delete them as your schedule shifts.
- **Integrated PDF Calendar Viewer:** Embeds the university's academic schedule PDF reliably inside the interface via a viewer panel.

### 4. 📝 Quick Notes Saver & PDF Downloader
- **Autosave Notes:** Integrated text editor with immediate persistence to local browser memory.
- **Export to Document:** Convert text to PDF instantly with client-side compiling using `jsPDF` for local storage, print, or sharing.

### 5. 🗺️ Career & Skill Roadmaps
- **Career Guides:** Embedded guides for Frontend/Backend (Full Stack) Engineering, Android App Development, AR/VR engineering, Machine Learning, Data Science, and DSA/CP.
- **External PDF Guides:** Direct hooks into interactive structures hosted at `roadmap.sh`.

### 6. 🏛️ Societies & Extra-Curriculars Directory
- **Categorized Index:** Explore active campus groups across Technical (Lean In, TechNeeds, GDG, IEEE, AWS, AssetMerkle), Cultural (Taarangana, Tarannum, Hypnotics, Rahnuma), Media (Prekshya), and Sports (Synergy).
- **Interactive Search:** Filter societies instantly by typing keywords.

### 7. ⏱️ Study Productivity Tools (Pomodoro Timer)
- **Time Boxing:** Standard 25-minute focus session paired with a 5-minute restorative rest period.
- **State Management:** Sound cues notify users when a session starts or finishes.

### 8. 🎮 Interactive Mini Games
- **Relaxation Zone:** Features browser-playable casual games to refresh during study breaks, including:
  - **Memory Match:** Dynamic card flipping game.
  - **Tic-Tac-Toe:** Single or local multiplayer.
  - **Puzzle Slider:** Tile reordering.
  - **Classic Pong:** Realtime paddle bounce.
  - **Mini Coding Quiz:** Interactive terminal-based trivia challenges testing Python, C, and JS knowledge.

---

## 💾 Local Browser State Architecture

To deliver a login-free experience, IGDTUWHub leverages the browser's `localStorage` API. The application manages the following keys:

- `cgpa_Semester <N>`: Stores arrays of custom subjects, credits, and grades saved for semester calculation.
- `igdtuw_custom_events`: Stores custom student events mapped to date keys (`YYYY-MM-DD`).
- `igdtuw_saved_courses`: Stores the list of courses bookmarked by the user for resource shortcut.
- `igdtuw_notes`: Stores raw note content in the Quick Notes scratchpad.

---

## 🛠️ Tech Stack & Third-Party Integrations

- **Core Scripting & Frameworks:** Vanilla Javascript (ES6+ Module Design Pattern)
- **Styling UI:** CSS3 Flexbox/Grid, custom variables for color mapping, and responsive breakpoints.
- **Icons & Styling Support:** [FontAwesome v6](https://fontawesome.com/)
- **PDF Exporter:** [jsPDF v2.5.1](https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js)
- **Data Charts:** [Chart.js](https://cdn.jsdelivr.net/npm/chart.js)
- **Web Fonts:** [Google Fonts (Poppins & Outfit)](https://fonts.google.com/)

---

## 🚀 How to Run Locally

Since this app is a purely client-side static web application, running it locally requires no build compilers or database configurations.

### Option A: Direct Launch
1. Download or clone this repository.
2. Locate the `index.html` file inside the root folder.
3. Double-click `index.html` to open it immediately in any standard modern web browser.

### Option B: Local Web Server (Recommended)
To prevent CORS or module-path restrictions when working with advanced local file loading, run a quick HTTP server:
- **Python 3:**
  ```bash
  python -m http.server 8000
  ```
- **NodeJS (via npx):**
  ```bash
  npx serve
  ```
Open `http://localhost:8000` or the indicated port in your web browser.

---

## 🤝 Contribution Guidelines

We highly encourage students of IGDTUW to contribute fests updates, notes, course guides, PYQs, and feature patches to keep this hub fresh and helpful!

Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for details on cloning, submitting pull requests, and standard style guidelines.

---

## ✨ Authors & Collaborators

Designed and built with 💜 by the original developers:

- **Manvi Sinha** ([LinkedIn](https://www.linkedin.com/in/manviiiisinhhh/) / [Instagram](https://www.instagram.com/manvisinhha/)) - Frontend & UI/UX Design
- **Arni Goyal** ([LinkedIn](https://www.linkedin.com/in/arni-goyal-b2639b321/) / [Instagram](https://www.instagram.com/arni_1408/)) - Backend Logics & Integrations
- **Divya Yadav** ([LinkedIn](https://www.linkedin.com/in/divya-yadav-3b7592322/) / [Instagram](https://www.instagram.com/divy.ayadav482/)) - Features & Data Curation

*This project is community-supported and open-source.*
