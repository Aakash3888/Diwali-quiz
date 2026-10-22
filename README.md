# 🪔 Diwali Special Quiz

Ek **single-file** HTML quiz app — Diwali theme, fireworks, score + streak bonus, aur result
WhatsApp pe directly share karne ke liye ready.

Link sabko bhejne ke baad har koi apna naam daal ke khele, apna score dekhe aur wahi link
apas mein aage bhejega 🔁 (growth loop).

---

## ✨ Features

| Feature | Detail |
|---|---|
| 16 Questions | Diwali GK (Hindi/Hinglish), har sawaal ka explanation |
| Timer | 15 sec per question, timeout pe auto-reveal |
| Scoring | 10 pts correct + 5 pts streak bonus (3+ streak) |
| Animations | Fireworks on correct answer, confetti + diyas background |
| Personalised | Naam ke saath score, local leaderboard (device par) |
| Sharing | WhatsApp, Copy Message, Copy Link, Native Share |
| Result card | Ek click me PNG image download (WhatsApp status ke liye) |
| Mobile | Fully responsive, Android/iOS friendly |
| Offline-safe | Single file, no build step, no dependencies |

---

## 🚀 GitHub Pages se host karo (2 minute)

1. **Repo banao** → GitHub par `New repository` → naam do (jaise `diwali-quiz`) → **Public** rakho.
2. **File upload** → repo me `Add file` → `Upload files` → `index.html` ko drag & drop karo → **Commit changes**.
3. **Pages on karo** → repo me **Settings** → **Pages** (left menu) →
   - Source: **Deploy from a branch**
   - Branch: **main** / **root**
   - Save
4. **Link copy karo** → 1-2 minute me ye link live ho jayega:

```
https://YOUR-USERNAME.github.io/diwali-quiz/
```

> Link me apna naam daal ke bhi bhej sakte ho — quiz us naam se greet karega:
> `https://YOUR-USERNAME.github.io/diwali-quiz/?name=Rahul`

5. **WhatsApp pe bhejo** → app me "Copy Link" → apni cast/custom list me paste karo. 🎉

### Local test (bina upload)

`index.html` ko browser me khol lo — sab kaam karega. Bas link `file:///` jaisa hoga, isliye
share karne se pehle GitHub Pages par zaroor host karo.

---

## ✏️ Apna naam / tagline change karo

`index.html` ke top me `CONFIG` block:

```js
const CONFIG = {
  hostName: "Aakash",        // <- apna naam
  hostTagline: "Diwali ki hardik shubhkamnayein! 🎇",
  whatsapp: ""               // optional: "919999999999"
};
```

### Apne questions add karo

`QUESTIONS` array me isi format me add karo:

```js
{
  q: "Sawal ka text?",
  o: ["Option A", "Option B", "Option C", "Option D"],
  a: 0,                      // sahi option ka index (0-3)
  e: "Answer ka explanation — result screen par dikhega."
}
```

> Options har question me automatically shuffle hote hain, toh sahi jawab hamesha "A" nahi hoga.

---

## 📁 Files

```
diwali-quiz/
├── index.html   # poora app (HTML + CSS + JS ek hi file me)
└── README.md
```

---

## 🎨 Customise (optional)

- **Theme colours**: `index.html` me `:root` me `--gold`, `--gold2`, `--bg`, `--bg2` badlo.
- **Timer**: `const TIME_PER_Q = 15;` badlo (seconds).
- **Quiz length**: `QUESTIONS` array me se questions hatao — baaki sab apne aap adjust ho jayega.
- **Preview image** (WhatsApp link preview): `og:image` ke liye `preview.png` add karke uska URL
  `index.html` ke `<head>` me daalo.

---

Made with 🪔 for Diwali 🎇
