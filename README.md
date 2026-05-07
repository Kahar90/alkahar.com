# nabilalkahar.com

Personal website of Nabil Alkahar — Solutions Architect, Software Engineer, and Writer.

## Tech Stack

- **Astro** — Static site generation
- **Tailwind CSS** — Utility-first styling
- **TypeScript** — Type safety
- **Astro Content Collections** — Markdown blog processing
- **Sharp** — Image optimization at build time
- **Bun** — JavaScript runtime and package manager

## Getting Started

```bash
bun install
bun run dev
```

Open [http://localhost:4321](http://localhost:4321).

## Adding a Blog Post

1. Create a new `.md` file in `src/content/blog/`
2. Add frontmatter:
   ```yaml
   ---
   title: "Your Post Title"
   date: "2025-05-01"
   excerpt: "Short description for the listing page"
   tags: ["topic"]
   ---
   ```
3. Write your content in Markdown below the frontmatter
4. Commit and push — the build process will pick it up automatically

### Adding Images to Blog Posts

Drop images into `public/blog/` and reference them in your markdown:

```markdown
![Alt text here](/blog/your-image.jpg)
```

No imports needed — Astro serves them as static files.

## Adding Gallery Photos

1. Drop image files into `src/assets/gallery/` (`.jpg`, `.jpeg`, `.png`, or `.webp`)
2. Add an entry to `src/data/gallery.json`:
   ```json
   {
     "file": "your-photo.jpg",
     "alt": "Description shown on hover and for screen readers"
   }
   ```
3. Images are automatically optimized by Sharp at build time

## Building for Production

```bash
bun run build
```

The static site is output to the `dist/` directory. Deploy it to GitHub Pages, Vercel, Cloudflare Pages, or any static host.

## Dark Mode

Click the theme toggle button in the top-right corner to switch between light and dark mode. Your preference is saved in `localStorage` and respected on your next visit. The site also respects your system preference on first load.

## Accessibility

- Skip-to-content link for keyboard users
- Focus management in gallery lightbox and easter egg dialog
- `prefers-reduced-motion` support disables animations
- All gallery images include descriptive alt text

## License

MIT
