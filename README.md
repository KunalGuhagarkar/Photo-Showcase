# Photo Showcase

A single-page HTML photo gallery that demonstrates how to handle images, captions, and embedded video with semantic, accessible markup. This project is intentionally **unstyled**. The focus is on the HTML that controls how media is loaded, described, and announced to assistive technology.

Built as a solution to the [Photo Showcase](https://roadmap.sh/projects/photo-showcase) project on [roadmap.sh](https://roadmap.sh).

## Features

- **Semantic page structure** using `<header>`, `<main>`, and `<footer>`
- **Six or more images**, each with:
  - a working `src`
  - descriptive `alt` text (describes the image, not the filename)
  - `width` and `height` attributes to reserve layout space and prevent layout shift while loading
- **Captions** on three or more images using `<figure>` and `<figcaption>`
- **One decorative image** with an empty `alt=""` so screen readers skip it
- **One embedded `<video>`** with `controls`, a `poster` image, and fallback text for browsers that don't support video
- **Head metadata**: `<title>`, `<meta charset>`, and `<meta name="viewport">`

## What I Learned

- `alt` text vs. captions: `alt` replaces the image when it can't be seen, while `<figcaption>` adds extra context for everyone
- Why `width` and `height` on `<img>` matter: they let the browser reserve space and avoid content jumping as images load
- Why decorative images need `alt=""` and why omitting the attribute entirely is different
- How `<video>` builds its player UI from attributes (`controls`, `poster`) and provides fallback content

## Project Structure

```
Photo-Showcase/
├── src/
│   ├── index.html
│   ├── images/
│   └── video/
└── README.md
```

## Getting Started

No build step or dependencies are required.

1. Clone the repository:
```bash
   git clone https://github.com/KunalGuhagarkar/Photo-Showcase.git
```
2. Go into the project folder:
```bash
   cd Photo-Showcase/src
```
3. Open `index.html` in your browser, or serve it locally:
```bash
   # Python 3
   python -m http.server 8000
```
   Then visit `http://localhost:8000`.

## Tech Stack

- HTML5

## Accessibility Notes

- Every meaningful image has descriptive alt text.
- The decorative image uses `alt=""` so it is skipped by screen readers.
- Landmark elements (`header`, `main`, `footer`) help screen reader users navigate the page.
- The video includes native controls and fallback text.

## Possible Next Steps

- Add CSS styling (the follow-up roadmap.sh project)
- Add responsive images with `srcset` and `sizes`
- Add `loading="lazy"` for below-the-fold images
- Add captions or subtitles to the video using `<track>`

## Acknowledgements

Project idea from [roadmap.sh](https://roadmap.sh/projects/photo-showcase).

## Author

**Kunal Guhagarkar**
[GitHub](https://github.com/KunalGuhagarkar)