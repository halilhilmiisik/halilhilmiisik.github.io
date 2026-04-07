# Wortschatz PWA

A personal German vocabulary flashcard app that works offline and installs on your iPhone home screen.

## Files

```
wortschatz-pwa/
├── index.html      ← The entire app
├── words.js        ← Your word list (edit this!)
├── manifest.json   ← PWA metadata
└── sw.js           ← Service worker (offline support)
```

## How to add your words

Open `words.js` and add your words to the `WORDS` array. Each entry looks like this:

```js
{
  word: "die Sehnsucht",
  translation: "longing, yearning",
  sentence: "Er fühlte eine tiefe Sehnsucht nach seiner Heimat.",
  sentenceTranslation: "He felt a deep longing for his homeland."
}
```

## Deploy to iPhone (free)

### Option A — GitHub Pages (recommended)
1. Create a free account at github.com
2. Create a new repository, e.g. `wortschatz`
3. Upload all 4 files
4. Go to Settings → Pages → Branch: main → Save
5. Your app is live at: `https://yourusername.github.io/wortschatz`
6. Open that URL on your iPhone in Safari
7. Tap the Share button → "Add to Home Screen"

### Option B — Netlify (drag & drop)
1. Go to netlify.com → Log in
2. Drag the entire `wortschatz-pwa` folder onto the deploy area
3. Done — you get a URL instantly
4. Open it in Safari on iPhone → Add to Home Screen

## How the app works

- **Tap the card** to flip and reveal the translation + example sentence
- **Tap the speaker icon** to hear the sentence read aloud in German
- **Swipe right** or tap ✓ Gewusst when you know the word
- **Swipe left** or tap ✗ Nochmal when you need to practice more
- Cards shuffle randomly each session
- Works fully **offline** once loaded

## Next steps (optional upgrades)

- Add spaced repetition scheduling (SM-2 algorithm) to track progress across days
- Let the app pull words from a Google Sheet so you can edit from anywhere
- Add a "hard words" mode that only shows your worst-performing cards
- Dark/light mode toggle
