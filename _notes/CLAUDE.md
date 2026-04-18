# Project: See What I'm Listeneing To

A personal music page that displays what the owner is currently listening to. Cards are added manually via a JSON file — newest on top, oldest at the bottom. The goal is fast, simple, and easy to update. No frameworks, no build tools, no dependencies. Plain HTML, CSS, and a small amount of vanilla JavaScript to read the JSON and render the cards.

Deployed to Cloudflare Pages. File paths are case-sensitive.

---

## File Structure

```
index.html
albums.json
Images/
_private/
  (notes, spec docs — gitignored)
.gitignore
```

---

## Page

- Background: white (`#ffffff`)
- Max content width: standard boxed layout, centered, appropriate for each viewport
- Page padding: generous — let it breathe

---

## Typography

- Font: `Roboto Mono` (load from Google Fonts)
- All text color: black (`#000000`)
- Page title: 64px, regular weight, centered
- Page title text: `See What I'm Listeneing To` — preserve the typo exactly
- Song title: 40px, regular weight
- Artist name: 20px, light, italic

---

## Card

- Background: `#2BCEBE`
- Border: 5px solid black
- Border radius: 21px
- Drop shadow: `box-shadow: 20px 20px 0 0 #000` (hard neobrutalist, no blur)
- Padding: 40px top/bottom, 20px left/right
- Gap between cards: 40px

---

## Album Art

- Size: 180px × 180px, fixed
- Border: 4px solid white
- Border radius: 14px
- Object fit: cover

---

## Listen Button

- Background: white
- Text: black
- Border: 2px solid black
- Border radius: 10px
- No shadow
- Font size: 16px
- Padding: 10px top/bottom, 40px left/right
- Links to Spotify URL from the JSON

---

## Card Layout (Desktop)

Left column: album art (180×180px)
Right column: song title, artist name, listen button — stacked vertically

Image on the left, content on the right. Use CSS Grid or Flexbox.

---

## Mobile Layout (≤600px)

Stack vertically:
1. Album art (centered or full width)
2. Song title
3. Artist name
4. Listen button

---

## Data Format

Albums live in `albums.json` in the project root. JavaScript reads this file on load and renders the cards. Newest entry = top of the array = top of the page.

```json
[
  {
    "title": "Stormy Night",
    "artist": "Roland Burrell",
    "cover": "Images/Stormy Night - Roland Burrell.jpeg",
    "link": "https://open.spotify.com/track/3cQ6hoLs6nN9iRIbSmkIVs"
  }
]
```

To add a new album: add a new object to the **top** of the array. That's it.

---

## JavaScript

One small script at the bottom of `index.html`. It:
1. Fetches `albums.json`
2. Loops through the array
3. Builds and injects the card HTML into the page

No libraries. No frameworks. Vanilla JS only.

---

## What Not To Do

- Do not add hover effects, transitions, or animations
- Do not add a footer
- Do not add navigation
- Do not add any styling not specified above
- Do not use any framework or build tool
- Preserve the typo in the page title exactly: `See What I'm Listeneing To`
- File paths are case-sensitive — image paths must match exactly
