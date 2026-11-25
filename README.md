# emberpieretti.com

Personal site of Emberson Pieretti. Static files only, no build step.

## Pages
- `/` (`index.html`): home with the bunny, the Elton button and the mini card fan.
- `/projects/` (`projects/index.html`): the card-fan carousel, one card per project.

## Hosting
- Netlify project `emberpieretti-projetos` (site id `3b65df2c-116c-480e-b990-06136fcfb53b`), custom domain emberpieretti.com (www redirects).
- DNS at GoDaddy: A `@` → `75.2.60.5`, CNAME `www` → `emberpieretti-projetos.netlify.app`. No changes needed.
- Goal: connect this folder's GitHub repo to that existing Netlify project so every push goes live. Do not create a new Netlify project.

## Structure
```
index.html              home (HTML, CSS, JS in one file)
media/                  bunny video, head cut-out layers, card thumbnails
projects/index.html     projects page
projects/img/           project screenshots for the cards (640 x 1120 px)
netlify.toml            no build, publish the root folder
```

## Home details
- `media/bunny.mp4` plays once: the bunny walks in and points. It is hosted here (no third-party link).
- At the fingertip: a glossy navy "Elton, clique aqui" button linking to https://cotador.emberpieretti.com.
- Left of it (below it on phones): a miniature of the projects card fan (`media/thumbs/`) with the line
  "Acompanhe o que estou construindo" and a round arrow; it links to `/projects/`.
- After the video ends, the head is swapped for a cut-out (`media/head.webp` over the clean patch `media/plate.webp`)
  that turns toward the cursor. Fingertip measured at (1113, 464) on the 1920 x 1080 final frame.
- Reduced motion or blocked autoplay: jumps to the final frame and shows everything at once.

## Projects details
- React 18.3.1 (UMD, cdnjs) and GSAP 3.15.0 (jsDelivr). Fonts: Bricolage Grotesque, Instrument Sans.
- Edit the `PROJECTS` list in `projects/index.html` (the `en` text is what shows). `src: 'img/x.jpg'` uses a screenshot; without `src` the card draws an illustration.
- More than 7 cards shows the arrows. Today: 7 projects and 2 example cards (`ex3`, `ex4`).
