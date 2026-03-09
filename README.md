# 🤖 AI Study Buddy – Class 7 CBSE

A **completely free**, browser-based study app for Class 7 CBSE students.  
No server. No API keys. No installation. Just open and learn!

---

## ✨ Features

| Feature | Description |
|---|---|
| 💬 AI Tutor | Rule-based tutor that explains concepts in kid-friendly language |
| 📝 Practice Quiz | Chapter-wise MCQ quiz (5 questions per session) |
| ☀️ Daily Practice | 10 mixed questions from all subjects |
| 🎓 Mock Exam | Full exam: 5 MCQ + 3 Short + 2 Long answer questions |
| 📊 Progress Tracker | Score, accuracy, streaks, subject breakdown, achievements |

---

## 🚀 How to Run Locally

1. Download / clone this folder
2. Make sure all 3 files are in the **same folder**:
   - `index.html`
   - `style.css`
   - `script.js`
3. Double-click `index.html` — it opens in your browser!

> No internet needed after the first load (fonts load from Google, but app works offline too).

---

## 🌐 Deploy Free on GitHub Pages

1. Create a free account at [github.com](https://github.com)
2. Click **New Repository** → name it `study-buddy`
3. Upload all 3 files (`index.html`, `style.css`, `script.js`)
4. Go to **Settings → Pages**
5. Set Source to **Deploy from branch → main → / (root)**
6. Click Save — your app is live at:  
   `https://YOUR-USERNAME.github.io/study-buddy`

---

## ▲ Deploy Free on Vercel

1. Create account at [vercel.com](https://vercel.com)
2. Click **Add New Project → Import Git Repository** (or drag & drop folder)
3. Upload the 3 files — Vercel auto-detects static site
4. Click Deploy → your app is live instantly!

---

## ➕ How to Add More Questions

Open `script.js` and find the `QUESTION_BANK` array (around line 60).

Add a new question object like this:

```javascript
{
  q: "Your question here?",
  opts: ["Option A", "Option B", "Option C", "Option D"],
  ans: 0,   // 0 = A, 1 = B, 2 = C, 3 = D (index of correct answer)
  exp: "Short explanation why this answer is correct! 🎯",
  subject: "Math",      // Math | Science | English | SST
  chapter: "Integers"   // Must match a chapter name in CHAPTERS object
}
```

### Adding a new AI Tutor topic:

Find `TUTOR_KB` array and add:

```javascript
{
  keys: ["keyword1", "keyword2", "keyword3"],   // words the student might type
  answer: `Your HTML explanation here with <b>bold</b> and emojis! 🌟`
}
```

---

## 📁 File Structure

```
study-buddy/
├── index.html    ← App structure & pages
├── style.css     ← All styles (colors, layout, animations)
└── script.js     ← Logic, question bank, AI tutor, scoring
```

---

## 🎨 Customization Tips

- **Change colors**: Edit CSS variables at the top of `style.css` (`:root { --clr-primary: ... }`)
- **Add subjects**: Add to `CHAPTERS` object and add questions to `QUESTION_BANK`
- **Add achievements**: Add to `checkAchievements()` function in `script.js`
- **Change grade thresholds**: Edit the `submitMock()` function

---

## 📚 Subjects & Chapters Covered

**Mathematics**: Integers, Fractions, Data Handling, Simple Equations, Lines & Angles, Triangles, Comparing Quantities, Rational Numbers, Algebraic Expressions

**Science**: Nutrition in Plants/Animals, Heat, Acids Bases & Salts, Physical & Chemical Changes, Respiration, Transportation, Reproduction in Plants

**English**: Grammar (Nouns, Verbs, Adjectives, Pronouns), Reading Comprehension, Writing Skills

**Social Science**: Mughal Empire, New Kings & Kingdoms, Inside Our Earth, Democracy, State Government, Markets

---

Made with ❤️ for young learners. Completely free, forever.
# Tutor
