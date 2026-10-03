# Updating dipendranathmahato.com

The site is still plain HTML/CSS/JavaScript and works directly on GitHub Pages. No build step is required.

## Routine UTRGV updates — edit one file

Open `assets/js/site-data.js`.

You can change:
- current semester (`teaching.currentTerm`)
- current courses (`teaching.courses`)
- office hours (`teaching.officeHours`)
- Edinburg/current profile information (`profile`)
- Box/Dropbox document links (`documents.external`)

### Add a Box or Dropbox PDF

Inside `documents.external`, add an object like:

```js
{ label: "MATH 2412 — Practice Test 1", url: "https://your-share-link", type: "Box" }
```

The UTRGV page renders it automatically. Large PDFs do not need to live in the GitHub repository.

### Add a course

Copy one object inside `teaching.courses`, then change `code`, `title`, `section`, `term`, and its links. The course card is generated automatically.

## Page structure

- `index.html` — professional homepage
- `research.html` — research
- `teaching.html` — full teaching history
- `utrgv.html` — **current UTRGV teaching hub**
- `presentations.html` — talks
- `cv.html` — CV
- `resources.html` — general resources
- `assets/js/site-data.js` — **routine current information**
- `assets/js/utrgv.js` — renders UTRGV data; normally do not edit
- `style.css` — global visual design

## Recommended semester workflow

1. Change `currentTerm`.
2. Replace/update the objects in `teaching.courses`.
3. Change office hours.
4. Paste new Box/Dropbox links.
5. Commit and push.

That is enough for most semester-to-semester updates.
