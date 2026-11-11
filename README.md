📝 Scribbly Notes — Realistic Handwritten Notebook Studio

Turn typed study notes into authentic, human-like handwritten notebook pages ready to print, review, or export — completely offline and privately on your machine.

🎯 Project Overview

Objective: Modern revision and study notes can be tedious to read when typed in uniform digital fonts. Rewriting notes by hand takes days. Scribbly Notes bridges this gap by transforming raw markdown/text into realistic handwritten notebook sheets with natural pen variations, diagrams, and math formulas without requiring cloud APIs, subscription keys, or internet access.

Methodology: Built as an offline-first Single Page Application (SPA). Uses client-side token parsing, a seeded pseudo-random number generator (PRNG) for microscopic word-level baseline offsets ($\pm 1.2\text{px}$) and rotation jitter ($\pm 1.35^\circ$), an decoupled Base64 image registry (mediaStore), and standard CSS @media print rules for vector PDF generation.

Expected Outcome: A multi-page notebook generator where typed notes flow cleanly across A4 sheets without split lines, supporting custom handwriting slant calibration, multi-color highlighters, pasted screenshots, math fractions, and selectable vector PDF output.

✨ Key Features

1. ✍️ 3 Handwriting Scripts & Paper Textures

Scripts: Casual Cursive, Architect/Neat Print, and Journal Flow.

Paper Types: Classic Ruled Notebook, Engineering Grid, Bullet Journal Dots, and Legal Yellow Pad with authentic margin lines and paper binder holes.

Inks: Gel Pen Blue, Royal Blue, Ballpoint Black, Vintage Sepia, Teacher Red, and Forest Green.

2. 🎲 Natural Human Variation Engine

Simulates real handwriting imperfections by calculating independent rotation angles, baseline vertical offsets, and ink pressure opacity per word.

Handwriting Slant Slider: Real-time calibration slider allowing users to adjust their personal handwriting slant from $-12^\circ$ (backhand) to $+22^\circ$ (forward cursive slant).

3. 🖼️ Clean Screenshot & Diagram Pasting (No Base64 Clutter)

Direct Clipboard Paste: Press Ctrl+V or Cmd+V inside the editor to paste any screenshot or diagram.

Smart Media Registry: The application converts images into an internal registry and inserts a short tag ([image: img_1a2b | Fig: Caption]), preventing massive Base64 strings from cluttering your notes.

Realistic Washi Tape: Rendered images include a Polaroid-style photo frame with subtle tilt and textured top tape.

4. 📐 Hand-Drawn Math & Freehand Sketchpad

Inline Fractions: Syntax [frac: numerator / denominator] creates handwritten stacked fractions with division bars.

Inline Radicals: Syntax [sqrt: expression] renders square root symbols with auto-extended radical bars.

Freehand Canvas Doodler: Click Draw Sketch to doodle circuit diagrams, graphs, or chemical structures and insert them directly into your notes.

5. 🖍️ Multi-Color Highlighters, Sticky Notes & Doodles

Pastel Highlighters: Highlight important terms with ==text== using Pastel Yellow, Pastel Green, Soft Pink, or Sky Blue.

3D Sticky Notes: Pin post-it notes to any page with [sticky: your note].

Margin Doodle Icons: Add ★ (Important) or 💡 (Insight) to the beginning of any line to render icons in the red margin column.

6. 📄 Clean Multi-Page A4 Flow & Export

Automatically calculates line heights and content weights, flowing long study summaries across Page 1, Page 2, Page 3+ without cut lines.

Export PDF: Triggers native browser vector print with selectable, copyable text.

Export PNG: Generates high-DPI image snapshots of individual notebook pages.
<img width="918" height="431" alt="image" src="https://github.com/user-attachments/assets/1d54ad64-47b7-4791-b61d-aed413138cae" />

🚀 Quick Syntax Reference

What you want

Type this in the editor

What appears on the notebook

Section Title

# Ohm's Law & Circuits

Large underlined handwritten header

Highlight

==crucial formula==

Pastel marker stroke across the word

Math Fraction

[frac: V / R]

Stacked vertical fraction $\frac{V}{R}$

Square Root

[sqrt: 2]

Handwritten root $\sqrt{2}$

Sticky Note

[sticky: Exam on Monday]

Yellow post-it pinned to the page

Paste Image
<img width="918" height="432" alt="image" src="https://github.com/user-attachments/assets/a7f60d29-f443-4d06-bf6f-72466582b11a" />

Press Ctrl+V with copied image

Mounted photo with washi tape

Important Star

★ Recall definition

Red star drawn in the margin

Checkbox

[box] Solve exercises

Square handwritten checkbox ☐

Arrow

-> or =>

Handwritten directional arrow ⟶

📋 Verification Checklist ("Done When")

[1] No split lines: Long 3+ page notes calculate line weights and paginate cleanly with no text cut in half across page boundaries.

[2] Wi-Fi Off / Offline integrity: All fonts, textures, scripts, and canvas functions are stored locally in the project; zero CDN dependencies.

[3] Legible & pleasant reading: Proper margins, ruled line heights ($32\text{px}$), realistic binder perforations, and natural spacing.

[4] Selectable text: Exporting via browser Print produces vector PDFs where all text can be selected, searched (Ctrl+F), and copied.

💻 How to Run Locally

Option A: Standalone HTML File (Zero-Setup)

Download or clone this repository.

Double-click index.html (or scribbly_notes.html) in your file explorer.

It opens instantly in Chrome, Edge, Firefox, or Safari — no npm install or local server required.

Option B: TypeScript + React Version

If running the componentized React project:

# 1. Install dependencies
npm install

# 2. Start local development server
npm run dev

# 3. Build optimized offline production bundle
npm run build


📂 Repository Structure

ScribblyNotes/
├── index.html                  # Standalone runnable offline single-page studio
├── ScribblyNotesApp.tsx        # TypeScript React single-file component version
├── README.md                   # Project documentation & guide
├── project_5_submission_guide.md # 5-step build lifecycle and rubric mapping
└── screenshots/                # Showcase preview images
    ├── 01-notebook-editor.png
    ├── 02-math-and-taped-images.png
    └── 03-vector-pdf-print.png


📜 Usage Policy

Rule: For personal study, revision summaries, and creative notebooks only. Never submit generated pages as handwritten schoolwork or official paper submissions.

📄 License

This project is open-source under the MIT License.
