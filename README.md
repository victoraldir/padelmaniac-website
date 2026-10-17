# Padel Pro website

Static site for the Padel Pro padel game: landing page, privacy policy and support/FAQ. Plain HTML and CSS, no build step. GitHub Pages serves it from the `main` branch root.

| Page | What |
|---|---|
| `index.html` | Landing page: features, screenshots, shot book |
| `privacy.html` | Privacy Policy (linked from the Google Play listing) |
| `support.html` | FAQ and contact |
| `404.html` | Not-found page |

## Develop

```sh
python3 -m http.server 8000   # then open http://localhost:8000
```

## Notes

- **Screenshots** in `assets/img/` were captured from the game itself (1600×900).
- **Google Play button:** it shows "Coming soon" while the listing isn't public. Once it is, replace the disabled button in `index.html` with a link to `https://play.google.com/store/apps/details?id=com.quartzodev.padelmaniac` (see the comment in the hero).
- **Privacy policy:** keep it in sync with the game and the `infra/` backend in the game repo. Update the effective date whenever data handling changes.
- **`404.html`** uses absolute `/padelmaniac-website/` paths, which is the GitHub Pages project URL. Update them if the site moves to a custom domain.
