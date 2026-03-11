# 🤖 AI Study Buddy – Multi-Class Edition

A **completely free**, browser-based AI-powered study app for CBSE students of **any class**.  
No server. No installation. Just open `index.html` and start learning!

> Questions are loaded from CSV files you upload. A 2368-question Class 7 starter pack is built in — one click to load it. Works for any class: just upload your own CSV.

---

## ✨ Features at a Glance

| Feature | Description |
|---|---|
| 🎓 Class Selector | Active class shown in nav; subtitle and filters adapt automatically |
| 💬 AI Tutor | Ask anything — Claude, ChatGPT, or Gemini; system prompt adapts to your class |
| 📝 Practice Quiz | Subject + chapter MCQ quiz with topic / difficulty / type filters; 5–30 questions |
| ☀️ Daily Practice | 20 random questions from your active class; filter by subject |
| 🎓 Mock Exam | 5 MCQ + 3 Short Answer + 2 Long Answer; estimated grade output |
| 📋 Term Exam | 50-mark paper — 20 MCQ + 5 Short + 3 Long + 1 Essay; 90-min timer; PDF download |
| 🏅 Annual Exam | 80-mark paper — 30 MCQ + 6 Short + 4 Long + 2 Essay; 180-min timer; PDF download |
| 📊 Progress Tracker | Score, accuracy %, streak, subject bars, 10 achievements |
| 📂 MCQ Question Bank | Upload CSV files with MCQ questions; unlimited banks, deletable anytime |
| ✍️ Exam Question Bank | Upload short / long / essay questions for Mock, Term & Annual exams |

---

## 🚀 Quick Start (2 minutes)

1. Download this folder — keep all files together:
   ```
   index.html
   style.css
   script.js
   README.md
   class7_questions.csv    ← 2368 Class 7 MCQ questions
   ```
2. Open `index.html` in your browser (double-click)
3. Go to **📂 Question Bank** → click **📦 Load Sample Bank (2368 questions)**
4. Optionally click **📦 Load Sample Exam Questions (Class 7)** to load short/long/essay exam questions
5. Select Class 7 from the nav dropdown → start practising!

> The hero subtitle on the home screen updates automatically to show your active class once questions are loaded.

---

## 🌐 Free Hosting

### GitHub Pages
1. Free account at [github.com](https://github.com) → New Repository → `study-buddy`
2. Upload `index.html`, `style.css`, `script.js`
3. Settings → Pages → Deploy from branch → main → / (root)
4. Live at `https://YOUR-USERNAME.github.io/study-buddy`

### Vercel / Netlify
Drag the project folder onto [vercel.com](https://vercel.com) or [netlify.com](https://netlify.com) — live in under a minute, free forever.

> ⚠️ Banks are saved in browser `localStorage`. After deploying, re-load banks from the Question Bank Manager page.

---

## 📂 MCQ Question Bank

All MCQ questions come from uploaded CSV files. The app has no hardcoded questions.

### Getting questions

| Option | How |
|---|---|
| **Load Sample Bank** | 📂 Question Bank → **📦 Load Sample Bank (2368 questions)** — loads instantly, no upload |
| **Download Sample CSV** | Same page → **⬇️ Download Sample CSV** — get the file to edit and re-upload |
| **Upload your own** | Drag & drop any CSV with the schema below |

### MCQ CSV Schema

**Required:** `question`, `option_a`, `option_b`, `option_c`, `option_d`, `correct_answer` (A/B/C/D)

**Optional (recommended):** `question_id`, `class`, `subject`, `chapter`, `topic`, `difficulty` (Easy/Medium/Hard), `question_type`, `explanation`, `learning_objective`, `ncert_reference`

```csv
question_id,class,subject,chapter,topic,difficulty,question_type,question,option_a,option_b,option_c,option_d,correct_answer,explanation,learning_objective,ncert_reference
Q001,8,Science,Cell Structure,Cell Organelles,Easy,MCQ,Powerhouse of the cell?,Nucleus,Mitochondria,Ribosome,Chloroplast,B,Mitochondria produce ATP,Understand cell organelles,NCERT Class 8 Ch 8
```

The `class` column drives the Class Selector — upload a CSV with `class=8` and a Class 8 card appears automatically.

---

## ✍️ Exam Question Bank (Short / Long / Essay)

Mock, Term and Annual exams include Short Answer, Long Answer and Essay sections. These are **open-ended questions without answers** — students write their own responses.

### How it works

- By default the app uses **built-in Class 7 defaults** (15 short + 8 long + 7 essay questions)
- Once you upload or load a bank, the app uses **those questions instead** for the active class
- Falls back to defaults only if no uploaded bank has questions for that type and class

### Getting exam questions

| Option | How |
|---|---|
| **Load Sample** | 📂 Question Bank → scroll to **✍️ Exam Question Bank** → **📦 Load Sample Exam Questions (Class 7)** |
| **Download Template** | Same section → **⬇️ Download Exam CSV Template** |
| **Upload your own** | Drag & drop a CSV with `type` and `question` columns |

### Exam CSV Schema

**Required:** `type` (short / long / essay), `question`

**Optional:** `subject`, `class`, `chapter`, `marks`

```csv
type,question,subject,class,chapter,marks
short,Define photosynthesis and write its word equation.,Science,7,Nutrition in Plants,2
long,Explain how plants prepare food through photosynthesis.,Science,7,Nutrition in Plants,5
essay,Write an essay on the importance of trees and forests.,English,7,,
```

The `class` field filters questions to the active class. If omitted, questions appear for all classes.

### Multiple exam banks

Upload separate banks per class or subject — all are merged and filtered by active class at exam time.

---

## 🎓 Class Selector

- Every class that has MCQ questions in any uploaded bank appears as a card
- Click a card to scope the entire app to that class
- The nav badge updates: `🎓 Class 7 ▾`
- The **home page subtitle** updates: "Your AI-powered study partner for **Class 7**"
- Switch class any time via the nav dropdown — progress is preserved

---

## 🤖 AI Tutor

| Provider | Model | Free Tier | Key URL |
|---|---|---|---|
| 🟣 Claude | claude-sonnet-4-20250514 | Limited free | [console.anthropic.com](https://console.anthropic.com) |
| 🟢 ChatGPT | gpt-4o-mini | Limited free | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| 🔵 Gemini | gemini-2.0-flash | **1,500 req/day free** | [aistudio.google.com](https://aistudio.google.com/app/apikey) |

Add a key: **💬 AI Tutor** → setup panel → select provider → paste key → Save 🔑

No key? The app uses a built-in offline knowledge base for major CBSE topics.

---

## 📝 Practice Quiz

1. Select subject tab → select chapter → optionally filter Topic / Difficulty / Type
2. Live badge: `✅ 89 questions 🟢 40 Easy 🟡 32 Medium 🔴 17 Hard`
3. Choose 5–30 questions → Start

**Smart padding** — if a chapter has fewer questions than requested, the app pads from the same subject.  
**Answer Review** — after completing, expand 📋 View Answers for full ✅/❌ breakdown with explanations.

---

## 📋 Term Exam & 🏅 Annual Exam

| | Term (50M) | Annual (80M) |
|---|---|---|
| Section A — MCQ | 20 × 1 = 20 | 30 × 1 = 30 |
| Section B — Short Answer | 5 × 2 = 10 | 6 × 2 = 12 |
| Section C — Long Answer | 3 × 5 = 15 | 4 × 5 = 20 |
| Section D — Essay | 1 × 5 = 5 | 2 × 9 = 18 |
| Timer | 90 minutes | 180 minutes |

Short, Long and Essay questions come from the **Exam Question Bank** (uploaded or sample). MCQs come from the **MCQ Question Bank**.

PDF download available after submission.

---

## 🔄 Question Rotation (Anti-Repeat System)

Queue-based rotation per 5-dimension scope key: `subject :: chapter :: topic :: difficulty :: type`

- Every filter combination has its own independent queue
- Questions rotate through the entire pool before any repeats
- Multiple CSV banks get unique IDs — no collisions, no ghost questions after deletion

---

## 📁 File Structure

```
AI-Study-Buddy/
├── index.html              ← App layout and all page sections
├── style.css               ← All styles, colours, animations
├── script.js               ← All logic
├── class7_questions.csv    ← 2368 Class 7 MCQ starter questions
└── README.md               ← This file
```

### Key script.js sections

| Section | Contents |
|---|---|
| 0 | Class state — `getActiveClass()`, dropdown UI, `updateClassUI()` |
| 1 | Chapter definitions |
| 2 | `QUESTION_BANK = []` — empty; all MCQs come from CSV uploads |
| 3 | AI Tutor offline knowledge base |
| 4 | Mock exam MCQ questions |
| 4b | **Exam Question Bank** — `DEFAULT_SHORT/LONG/ESSAY_QUESTIONS`, `getExamQuestions()`, `loadAllExamBanks()`, `loadSampleExamBank()`, `parseExamCSV()`, `renderExamBanksList()`, `downloadSampleExamCsv()` |
| 5 | Progress tracking |
| 6 | Navigation (`showPage()`), dynamic hero subtitle |
| 7 | AI Tutor — multi-provider API, `getSystemPrompt()` |
| 8 | MCQ bank helpers — `getAllQuestions()`, `getActiveQuestions()` |
| 9 | Quiz setup — subject tabs, chapter grid, filters |
| 10 | Quiz rendering — `renderQuestion()`, answer shuffling |
| 11 | Daily practice |
| 12 | Mock exam |
| 12b | Term & Annual exam engine — `EXAM_CONFIG`, `startExam()`, timer, PDF |
| 13 | Progress tracker & achievements |
| 14 | MCQ CSV upload, parse, save, manage — `loadSampleBank()`, `downloadSampleCsv()` |
| 15 | ID assignment — `assignCsvIds()` |
| 16 | Rotation engine — `makeScopeKey()`, `pickQuestions()` |

---

## 🎨 Customisation

**Colour scheme** — edit CSS variables in `style.css`:
```css
:root {
  --clr-primary: #4f46e5;  --clr-secondary: #7c3aed;
  --clr-accent:  #f59e0b;  --clr-green:     #10b981;
}
```

**Subject emojis** — find `SUBJECT_EMOJI` in `script.js`:
```javascript
const SUBJECT_EMOJI = { Math:'➕', Science:'🔬', Hindi:'🇮🇳', Computer:'💻' };
```

**Add offline AI topics** — add to `TUTOR_KB` in `script.js`:
```javascript
{ keys: ["keyword"], answer: `Your <b>HTML</b> explanation 🌟` }
```

---

## 🔒 Privacy

All data stays in your browser (`localStorage`). Nothing is sent to any server except your chosen AI provider. API keys are stored locally only.

---

## 🆘 Troubleshooting

| Problem | Fix |
|---|---|
| Home shows "No questions loaded" | Go to 📂 Question Bank → Load Sample Bank |
| Class selector is empty | Upload any CSV with a `class` column |
| Exam short/long questions not changing | Upload an exam bank from ✍️ Exam Question Bank section |
| CSV upload fails | Check headers match schema; `correct_answer` must be A/B/C/D; save as UTF-8 |
| AI Tutor not responding | Check API key; try switching providers |
| PDF not downloading | Allow pop-ups for the app URL; try another browser |
| Progress not saving | `localStorage` may be disabled in private/incognito mode |

---

## 📋 Changelog

### Current Version
- **Dynamic hero subtitle** — shows active class once questions are loaded; generic message before load
- **Gap added** between nudge banner and feature tiles on home screen
- **✍️ Exam Question Bank system** — full upload/manage/delete pipeline for short, long and essay questions
  - `getExamQuestions(type)` — pulls from uploaded bank filtered by active class; falls back to built-in Class 7 defaults
  - `parseExamCSV()` — parses the simple `type, question, subject, class` schema
  - Sample load button + download template button in the CSV manager
  - Mock, Term and Annual exams all use `getExamQuestions()` instead of hardcoded arrays
  - Exam banks stored in `studyBuddy_examBanks` localStorage key, separate from MCQ banks
- **CSV-only MCQ architecture** — `QUESTION_BANK = []`; all MCQs from uploaded CSVs
- **2368-question starter pack** embedded and loadable in one click
- **Queue-based rotation** with 5-dimension scope key
- **Term Exam (50M) + Annual Exam (80M)** with timers and PDF download
- **Answer Review panel** after Quiz and Daily Practice

---

Made with ❤️ for students of all classes. Completely free, forever.
