# 🪔 Happy Diwali 2026 · Kanak Dovloper 🪔

**Premium, HD, pro-style** Diwali celebration app — ek hi HTML file me:
Diwali **Quiz** + **Lucky Wheel** + **Diya Dash** game + **Wish Generator** + shareable result card.

Link sabko bhejo → har koi apna naam daal ke khele → apna score + wish WhatsApp par bheje → wahi link
apas mein aage jaaye 🔁

---

## 🎮 Features

| # | Feature | Detail |
|---|---|---|
| 1 | 🎯 **Diwali Quiz** | 16 GK questions (Hinglish), 15s timer, auto-reveal, explanation har sawaal ke saath |
| 2 | 🎡 **Lucky Wheel** | 8 prize segments, 4.4s smooth spin, winner popup + shareable prize message |
| 3 | 🪔 **Diya Dash** | 20-second reflex game — diyas tap karo, bombs se bacho, score share karo |
| 4 | 💌 **Wish Generator** | 4 tones (Warm / Funny / Desi / Pro) — naam + link ke saath auto message, copy & share |
| 5 | 🏆 **Scoring** | 10 pts per correct + 5 pts streak bonus (3+ streak) — max 160 |
| 6 | 📊 **Result Card** | Dial gauge, stats, aur ek click me **PNG card** download (WhatsApp status ke liye) |
| 7 | 📲 **Sharing** | WhatsApp, Copy Message, Copy Link, Native Share (mobile) |
| 8 | 👑 **Leaderboard** | Device-par local leaderboard (naam + score) |
| 9 | ✨ **Design** | Gold-foil typography, glassmorphism, aurora blobs, film grain, fireworks, confetti, ripple buttons, 3D hover |
| 10 | 📱 **Mobile** | Fully responsive + `prefers-reduced-motion` support |

---

## 🚀 GitHub Pages par host karo (2 minute)

1. **Repo banao** → GitHub par `New repository` → naam do (e.g. `diwali-quiz`) → **Public** rakho.
2. **Upload** → `Add file` → `Upload files` → `index.html` drag & drop → **Commit changes**.
3. **Pages on** → **Settings** → **Pages** →
   - Source: **Deploy from a branch**
   - Branch: **main** / **root** → **Save**
4. **Link ready** (1-2 min me):

```
https://YOUR-USERNAME.github.io/diwali-quiz/
```

5. **WhatsApp pe bhejo** → app me **🔗 Link** button → apni cast/custom list me paste karo 🎉

> Naam ke saath link: `https://YOUR-USERNAME.github.io/diwali-quiz/?name=Rahul`
> (quiz us naam se greet karega)

**Local test:** `index.html` ko browser me khol lo — sab chalta hai, bas share ka link `file:///`
hoga, isliye share karne se pehle Pages par host zaroor karo.

---

## ✏️ Apni details badlo

`index.html` ke top me `CONFIG` block (search `const CONFIG`):

```js
const CONFIG = {
  brand: "Kanak Dovloper",     // <- apna naam / brand
  tagline: "Khelo, jeeto aur apna score sabke saath share karo! 🎇",
  timePerQuestion: 15,         // quiz timer (seconds)
  prizes: [                    // Lucky Wheel ke prizes (label + color)
    { t: "₹100 Cashback", c: "#f5c451" },
    { t: "Mithai Box",    c: "#ff8a3d" },
    /* ... 8 total ... */
  ]
};
```

Brand ka spelling ya logo text badalna ho → sirf `CONFIG.brand` change karo, poora app update ho jayega
(top bar, hero, footer, share messages, result card — sab jagah).

### Apne questions add karo

`QUESTIONS` array me isi format me:

```js
{
  q: "Sawal ka text?",
  o: ["Option A", "Option B", "Option C", "Option D"],
  a: 0,                      // sahi option ka index (0-3)
  e: "Explanation — result screen par dikhega."
}
```

> Options har question me auto-shuffle hote hain, isliye sahi jawab hamesha "A" nahi hoga.

---

## 🎨 Design tweaks

- **Colours**: `:root` me `--gold`, `--saffron`, `--wine`, `--foil` (gold-foil gradient) badlo.
- **Font**: `<head>` me Google Fonts link — abhi **Cinzel** (display) + **Plus Jakarta Sans** (UI) + **Baloo 2** (Hindi).
- **Result card image**: canvas 1080×1350 (4:5, WhatsApp status perfect).
- **Preview image** (WhatsApp link preview): `og:image` ke liye `preview.png` rakho aur uska URL `<head>` me daalo.

---

## 📁 Files

```
diwali-quiz/
├── index.html   # poora app (HTML + CSS + JS — ek hi file, zero dependency)
└── README.md
```

---

Made with 🪔 by **Kanak Dovloper** · Happy Diwali 2026 🎇
