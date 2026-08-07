# Comics for Comfort website

A one-page site for the Comics for Comfort project. No backend, no accounts, no
build step. It is a single file (`index.html`) that runs anywhere.

- **To look at it:** double-click `index.html` and it opens in your browser.

## The design, in one line

The comic artwork carries all the colour, so the page itself stays deliberately
plain: black ink, newsprint, and one red. That is the whole palette. It keeps the
comics looking like the loudest thing on the screen, which is the point.

The logo (`logo.svg`) is a heart inside a speech balloon, drawn for this project.
It is a vector, so it stays sharp at any size and doubles as the browser-tab icon.

---

## ✏️ Editing it (no coding needed)

Everything you'll normally change (email, tally, crew, photos) lives in **one
box** near the bottom of `index.html`. Open the file in any text editor (Notepad,
TextEdit, VS Code) and search for:

```
★★★  EDIT YOUR SITE HERE  ★★★
```

Inside that box you can change:

| What | How |
|------|-----|
| **Contact email** | Change the address in `email: "..."`. |
| **The tally numbers** | Update the `tally: { ... }` block after each sort or delivery. Commas are fine, so `"1,450"` works. |
| **"Last updated" date** | Put the date in `tallyUpdated: "..."` (just the date; the words "Last updated" get added for you). Leave `""` to hide it. |
| **Who runs this** | Add or edit people in the `crew: [ ... ]` list. |
| **Your photos** | Add lines to the `gallery: [ ... ]` list (see below). |

**Save the file, then refresh your browser.** That's it.

A few rules keep it working:

- Leave every quote `"` and comma `,` where they already are.
- Don't type a straight quote `"` inside a value. Use an apostrophe `'` instead.
- **If anything looks off, hit Ctrl+Z to undo and save again.** A typo can't break
  the design. Worst case, the one part you were editing falls back to a default.

> Keep the tally the same as your master log, so the number people see matches
> your records.

---

## 🖼️ Adding your own photos

The photo log is empty on purpose. To add a photo:

1. Drop the image file into the **`images`** folder next to `index.html`.
2. In the `gallery:` list, add one line per photo:

   ```js
   gallery: [
     { src: "images/sort-day-1.jpg",      caption: "First sort day, Week 2" },
     { src: "images/library-handoff.jpg", caption: "Delivery to Kinnelon Library" }
   ]
   ```

3. Save and refresh.

**Filenames are case-sensitive once the site is online.** `images/Photo.JPG` is
not the same as `images/photo.jpg`, so type the `src` to match the real filename
exactly, or the photo works on your computer and breaks after you publish.

**Privacy:** shoot the books, the boxes, and the crew. No kids' or patients'
faces, and no shots inside a facility, without written permission.

---

## ⚠️ One thing to decide before you publish

The `art/` folder holds the classic comic scans (Batman, Iron Man, X-Men,
Spider-Man, Silver Surfer, and several interior pages). They are used throughout
the site — the fanned stack on the cover, the three how-it-works panels, the two
full-width banners, and the scrolling shelf.

Those images are owned by Marvel and DC. The footer carries a credit line saying
so and stating that the project is independent and unaffiliated, which is the
honest framing: you are showing the kind of books you collect and give away.

That is a normal thing for a comic drive to do, but it is not zero-risk on a
public site that partner organisations and admissions readers will see. Worth a
five-minute gut-check with an adult before it goes live. If you'd rather not use
them, say the word and the same layout works with photos of your own boxes.

---

## 🌐 Putting it online (free)

- **Netlify Drop:** go to [app.netlify.com/drop](https://app.netlify.com/drop)
  and drag this folder onto the page. You get a live link in seconds.
- **GitHub Pages:** make a repository, upload these files, then turn on Pages in
  Settings → Pages.

Upload the **whole folder** so `art/`, `images/`, and `logo.svg` come along.

---

## Files

```
comics-for-comfort-v2/
├── index.html   (the entire website; edit the box near the bottom)
├── logo.svg     (the logo, drawn for this project; also the tab icon)
├── art/         (the comic scans used across the page)
├── images/      (put YOUR OWN photos here)
└── README.md    (this guide)
```
