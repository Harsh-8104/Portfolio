# Harsh Chauhan — Portfolio

A single-file, zero-dependency personal portfolio built with vanilla HTML, CSS and JavaScript. It has a dark, terminal-meets-editorial look: amber accents, scanline and grain overlays, and a command palette for keyboard navigation.

**Live demo:** _add your Netlify / GitHub Pages URL here_

<!-- ![Portfolio preview](./preview.png) -->

---

## Features

- **Animated intro** – boot-style loader with progress bar, then a reveal of the hero section
- **Hero** – glitch-effect name, typing animation for rotating taglines, and quick stats
- **Command palette** – press `Ctrl + K` or `/` to jump to any section, open LinkedIn, or send an email (navigate with `↑` `↓`, run with `Enter`, close with `Esc`)
- **Skills** – tabbed view (Frontend / Backend / Tools) with animated proficiency bars
- **Projects** – case-study cards rendered from a JS array
- **Experience & Education** – twin timelines rendered from data
- **Certifications** – filterable grid (All / Frontend / Backend / Tools) with a modal viewer; supports `←` `→` navigation and optional certificate images
- **Contact form** – submits through [Web3Forms](https://web3forms.com) with no backend needed, plus a success message
- **Polish** – scroll progress bar, scroll-reveal animations, sticky blurred nav, mobile hamburger menu, custom scrollbar and selection colours, responsive layout

## Tech Stack

| Layer | Details |
|---|---|
| Markup / Styling | HTML5, CSS3 (custom properties, grid, flexbox, keyframe animations) |
| Logic | Vanilla JavaScript (ES5-style, no frameworks, no build step) |
| Fonts | Bebas Neue, IBM Plex Mono, Instrument Serif via Google Fonts |
| Forms | Web3Forms API |

## Project Structure

```
.
├── index.html   # entire site: markup, styles and scripts
└── README.md
```

## Getting Started

No installation or build step is needed.

```bash
git clone https://github.com/Harsh-8104/<your-repo>.git
cd <your-repo>

# Option 1: just open the file
open index.html

# Option 2: serve it locally
npx serve .
# or
python -m http.server 8000
```

## Customisation

All content lives in data arrays at the top of the `<script>` block in `index.html`:

| What to change | Where |
|---|---|
| Skills and proficiency bars | `SKILLS` (`frontend`, `backend`, `tools`) |
| Project cards | `PROJECTS` (`id`, `emoji`, `name`, `desc`, `tags`) |
| Work history | `EXP` |
| Education | `EDU` |
| Certifications | `CERTS` (`icon`, `name`, `issuer`, `date`, `category`, `badge`, `link`, optional `image` URL or base64) |
| Typing-effect lines | `words` |
| Command palette actions | `CMD_COMMANDS` |
| Colours | CSS variables in `:root` (`--ink`, `--paper`, `--amber`, `--dim`) |

### Setup checklist before deploying

1. **Contact form** – get a free access key at [web3forms.com](https://web3forms.com) and replace `YOUR_ACCESS_KEY_HERE` in the `#contactForm` hidden input.
2. **Social links** – update the GitHub, LinkedIn and Twitter links in the contact section and footer, plus the LinkedIn action in `CMD_COMMANDS`. These currently point to placeholder profile URLs.
3. **Résumé** – replace the `href="#"` on the *Download Résumé* button (and the matching command-palette action) with a link to your PDF.
4. **Certificates** – replace each `link:'#'` with your credential URL and add an `image` where you have one.
5. **Content** – review the Experience, Education, Certification and hero-stat entries so every line reflects your actual background.
6. **Profile photo** – the About section uses an emoji placeholder; swap it for an `<img>`.

## Deployment

Since it is a static site, any static host works:

- **Netlify** – drag and drop the folder, or connect the repo
- **GitHub Pages** – Settings → Pages → deploy from the `main` branch
- **Vercel / Cloudflare Pages** – import the repo, with no build command and the output directory as `/`

## Browser Support

Works in current versions of Chrome, Edge, Firefox and Safari. It uses `backdrop-filter`, CSS `inset` and `clamp()`, so very old browsers may degrade visually.

## Author

**Harsh Chauhan** — Full Stack Developer & BCA student, Noida, India

- GitHub: [@Harsh-8104](https://github.com/Harsh-8104)
- LinkedIn: [harsh-chauhan08](https://linkedin.com/in/harsh-chauhan08)

## License

Released under the MIT License. Feel free to fork it for your own portfolio, and a credit link is appreciated.
