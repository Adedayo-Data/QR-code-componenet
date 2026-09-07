# Frontend Mentor - QR code component solution

This is a solution to the [QR code component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/qr-code-component-iux_sIO_H). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

A simple card component displaying a QR code, built as my first Frontend Mentor challenge to practice HTML and CSS fundamentals — layout, centering, and typography.

### Links

- Solution URL: [Github](https://github.com/Adedayo-Data/QR-code-componenet)
- Live Site URL: [QR code](https://adedayo-data.github.io/QR-code-componenet/)

## My process

### Built with

- Semantic HTML5 markup
- CSS (Flexbox, CSS Grid)
- Mobile-first workflow
- Google Fonts (Outfit)

### What I learned

This project taught me a rule I'll carry into every layout from here: **centering CSS goes on the parent of the thing you want centered, not on the thing itself.** I originally put `display: grid; place-items: center;` on my card (`.qr-section`), which only centered the content _inside_ the card. The fix was moving that rule to `main` — the card's parent — so it centers the card itself on the screen.

```css
main {
  height: 100vh;
  display: grid;
  place-items: center;
}
```

I also learned that `height: 100vh` matters here — without giving the parent full viewport height, there's no extra space to center anything within in the first place.

Two smaller but sticky lessons:

- `hsl()` values need `%` on the saturation and lightness numbers (`hsl(0, 0%, 100%)`), or the browser silently drops the whole declaration instead of throwing an error — which made a missing background color hard to spot at first.
- Importing a custom font (Google Fonts' Outfit, weights 400/700) takes two steps: a `<link>` in the HTML `<head>` to actually fetch the font, then `font-family` in CSS to apply it — the link alone doesn't do anything on its own.

## Author

- Frontend Mentor - [@Adedayo](https://www.frontendmentor.io/profile/Adedayo)
