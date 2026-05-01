# nabilalkahar.com

Personal website of Nabil Alkahar — Solutions Architect, Software Engineer, and Writer.

## Tech Stack

- **Astro** — Static site generation
- **Tailwind CSS** — Utility-first styling
- **TypeScript** — Type safety
- **Astro Content Collections** — Markdown blog processing
- **Sharp** — Image optimization at build time

## Getting Started

```bash
npm install
npm run dev
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
     "alt": "Description shown on hover (optional)"
   }
   ```
3. Images are automatically optimized by Sharp at build time
4. Leave `"alt"` as `""` if you don't want a caption overlay

## Building for Production

```bash
npm run build
```

The static site is output to the `dist/` directory. Deploy it to GitHub Pages, Vercel, Cloudflare Pages, or any static host.

## Dark Mode

Click the `[theme]` button in the top-right corner to toggle between light and dark mode. Your preference is saved in localStorage and respected on your next visit. The site also respects your system preference on first load.

## Custom Domain

Configure your DNS to point to your hosting provider. No additional config needed in the code.

## License

MIT
