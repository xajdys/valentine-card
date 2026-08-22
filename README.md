# 💌 Valentine's Card

A cozy, warm-toned digital Valentine's card built with pure HTML and CSS Flexbox — no frameworks, no JavaScript, just handwritten love (and a lot of debugging).

## 🌹 Preview

A centered card featuring:
- A heading with heart icons
- A rose-heart image on the left
- A heartfelt handwritten message on the right
- A soft, star-dotted warm background
- A subtle hover effect on both halves of the card

## ✨ Features

- Fully centered layout — stays centered at any screen size
- Responsive image handling with `object-fit: cover` (no stretching/distortion)
- Full-bleed background image using `background` shorthand (no repeat, fully covers viewport)
- Soft shadows and rounded corners for a genuine "card" feel
- Smooth scale-up hover transition on both card sections

## 🛠️ Built With

- **HTML5** — semantic structure
- **CSS3 (Flexbox)** — layout, centering, and responsive behavior
  - `display: flex`, `flex-direction`, `justify-content`, `align-items`, `flex-wrap`
  - `gap` for clean spacing (no margin hacks)
  - `object-fit`, `box-shadow`, `border-radius`, `background` shorthand

## 📚 What I Learned

This was my first hands-on Flexbox project after learning the fundamentals. A few real bugs I ran into and fixed along the way:

- **`flex: 1` inside a `column`-direction parent** was stretching my card way taller than intended — main axis behaves differently once direction changes.
- **Old margin-based spacing conflicting with new flex-based centering** — once I centered the page with `justify-content`/`align-items`, I had to remove leftover fixed margins and replace them with `gap` instead.
- **A single typo (`83w` instead of `83vw`)** silently broke my heading's width — CSS doesn't error on invalid values, it just ignores that line entirely.
- **Default `background-image` tiling** — had to explicitly add `background-repeat: no-repeat` and `background-size: cover` to stop it from repeating across the page.
- **`<img>` is inline by default**, which caused unexpected sizing quirks when trying to make it fill its container — fixed with `display: block`.

## 🚀 Running Locally

1. Clone this repo
2. Make sure `background.jpg` and `roses.png` are in the same folder as `index.html`
3. Open `index.html` in any browser — no build step, no dependencies

## 📂 File Structure

```
valentines-card/
├── index.html
├── styles.css
├── background.jpg
└── roses.png
```

## 💭 Notes

Built as a learning project while studying CSS Flexbox — the goal was less about a "perfect" design and more about applying flex concepts (centering, wrapping, growing/shrinking) to a real, finished piece rather than isolated code snippets.

