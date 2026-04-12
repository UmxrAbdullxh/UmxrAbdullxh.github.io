# Home..

A minimal personal blog built with Astro.

---

## How to run locally

### Step 1 — Install Node.js

You need Node.js 18 or higher. Check if you have it:

```bash
node -v
```

If not, download it from https://nodejs.org (pick the LTS version).

---

### Step 2 — Install dependencies

Open a terminal in this folder and run:

```bash
npm install
```

---

### Step 3 — Start the dev server

```bash
npm run dev
```

Open http://localhost:4321 in your browser. The site hot-reloads when you save files.

---

### Step 4 — Build for production (when ready to deploy)

```bash
npm run build
```

This outputs a `dist/` folder with static HTML files ready to deploy anywhere.

---

## Writing a new post

1. Create a new `.md` file inside `src/content/blog/`:

```
src/content/blog/my-new-post.md
```

2. Start with this frontmatter (the `---` block at the top):

```markdown
---
title: My new post
date: 2025-04-12
---

Write your content here in plain Markdown.
```

3. Save the file. It appears automatically on the `/blog` page, sorted by date. The URL will be `/blog/my-new-post`.

That's it. No config to touch, no imports to add.

---

## Project structure

```
src/
  content/
    blog/         ← your posts go here (.md files)
    config.ts     ← tells Astro what fields each post has
  layouts/
    Base.astro    ← nav + footer, wraps every page
  pages/
    index.astro          ← home / about page
    blog/
      index.astro        ← lists all posts
      [slug].astro       ← renders each individual post
  styles/
    global.css    ← base dark styles
astro.config.mjs
package.json
```

---

## Customising

| What | Where |
|---|---|
| Your name | `src/pages/index.astro` |
| About text | `src/pages/index.astro` |
| Social links | `src/pages/index.astro` |
| Colors / font | `src/styles/global.css` |
| Nav items | `src/layouts/Base.astro` |
