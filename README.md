# emberpieretti.com

Personal site of Emberson Pieretti. Static files only, no build step. Everything is in English.

## Pages
- `/` (`index.html`): home. A 3D bunny video plays once, walks in and points; a glossy 3D button
  "Explore projects in progress" appears where he points and links to `/projects/`.
- `/projects/` (`projects/index.html`): the card-fan carousel, one card per project.

## Hosting
- Netlify project `emberpieretti-projetos` (site id `3b65df2c-116c-480e-b990-06136fcfb53b`), custom domain emberpieretti.com (www redirects).
- DNS at GoDaddy: A `@` → `75.2.60.5`, CNAME `www` → `emberpieretti-projetos.netlify.app`. No changes needed.
- Goal: connect this folder's GitHub repo to that existing Netlify project so every push goes live. Do not create a new Netlify project.

## Structure
```
index.html              home (HTML, CSS, JS in one file)
media/                  optional: put bunny.mp4 here to self-host the video (see below)
projects/index.html     projects page
projects/img/           project screenshots for the cards (640 x 1120 px)
netlify.toml            no build, publish the root folder
```

## Home details
- The video tries `media/bunny.mp4` first, then falls back to the original hosted file on
  pub-86dc5b5484314368ac5436a674b0d919.r2.dev. To self-host, save the mp4 as `media/bunny.mp4`.
- The button position comes from the fingertip measured on the last frame (1113, 464 in a 1920 x 1080 frame)
  and is recalculated on resize. It appears at 2.5 s, when the arm reaches the pointing pose.
- Narrow screens show the slice of the frame from the target to the bunny, faded into the page colour.
- Reduced motion or blocked autoplay: jumps to the final pointing frame and shows the button at once.

## Projects details
- React 18.3.1 (UMD, cdnjs) and GSAP 3.15.0 (jsDelivr). Fonts: Bricolage Grotesque, Instrument Sans.
- Edit the `PROJECTS` list in `projects/index.html` (the `en` text is what shows). `src: 'img/x.jpg'` uses a screenshot; without `src` the card draws an illustration.
- More than 7 cards shows the arrows. Today: 7 projects and 2 example cards (`ex3`, `ex4`).
