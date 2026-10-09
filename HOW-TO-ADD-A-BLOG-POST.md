# How to Add a New Blog Post (No Coding Needed)

This is the simplest way to publish a new post yourself, using only your web browser — no install, no terminal.

There are 4 topics on the blog, each with its own folder:

| Topic | Folder |
|---|---|
| Integrating AI Into Real Workflows | `blog/integrating-ai-workflows/` |
| Pricing AI the Way You'd Price Risk | `blog/pricing-ai-vs-risk/` |
| What I'm Learning About AI, and Why | `blog/learning-ai/` |
| Ruminations | `blog/rumination/` |

Adding a post means **3 edits** on GitHub.com. Do them in this order.

---

## Step 1 — Create the new post page

1. Go to [github.com/ketibak-ai/pink-analytica-website](https://github.com/ketibak-ai/pink-analytica-website)
2. Open the topic folder you're posting in (e.g. click `blog`, then `integrating-ai-workflows`)
3. Click **Add file → Create new file**
4. For the file name, type a short url-friendly slug followed by `/index.html` — for example:

   ```
   my-new-post-title/index.html
   ```

   (lowercase, words separated by dashes, no spaces or punctuation)
5. Paste the template below into the editor box, filling in your own title, date, and paragraphs
6. Scroll down, click **Commit changes**

### Template to copy/paste

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>YOUR POST TITLE &middot; Pink Analytica</title>
<link rel="icon" type="image/svg+xml" href="../../../favicon.svg">
<meta name="description" content="ONE SENTENCE SUMMARY OF THE POST.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Serif:ital,wght@0,400;0,500;0,600;1,400&family=IBM+Plex+Sans:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="../../../styles.css">
</head>
<body>

<div class="topbar">
  <div class="wrap">
    <div class="topbar-name"><a href="../../../index.html" style="color:inherit; text-decoration:none;">Pink Analyt<span class="i-mark"><svg viewBox="0 0 20 34" aria-hidden="true"><ellipse cx="10" cy="4" rx="3.6" ry="3"/><polygon points="10,9 16,19 4,19"/><line x1="2" y1="20" x2="18" y2="20"/><line x1="10" y1="20" x2="10" y2="32"/></svg><span class="sr-only">i</span></span>ca</a></div>
    <nav>
      <a href="../../../index.html#what-i-do">What It Does</a>
      <a href="../../../index.html#work">Featured Work</a>
      <a href="../../../index.html#why">Why Pink Analytica</a>
      <a href="../../../index.html#about">About</a>
      <a href="../../index.html">Blog</a>
      <a href="../../../index.html#contact">Contact</a>
    </nav>
  </div>
</div>

<main class="wrap" style="padding-top:56px;">
<article class="post">
  <div class="post-header">
    <p class="eyebrow reveal"><a href="../index.html" class="back-link">&larr; TOPIC NAME</a></p>
    <h1>YOUR POST TITLE</h1>
    <div class="post-meta">MONTH DAY, YEAR</div>
  </div>
  <div class="post-body">
    <p>First paragraph goes here.</p>
    <p>Second paragraph goes here.</p>
    <h2>Optional subheading</h2>
    <p>More text under the subheading.</p>
  </div>
  <div class="post-footer">
    <a href="../index.html" class="back-link">&larr; More on TOPIC NAME</a>
  </div>
</article>
</main>

<footer>
  <div class="wrap">
    <div class="fname">Pink Analyt<span class="i-mark"><svg viewBox="0 0 20 34" aria-hidden="true"><ellipse cx="10" cy="4" rx="3.6" ry="3"/><polygon points="10,9 16,19 4,19"/><line x1="2" y1="20" x2="18" y2="20"/><line x1="10" y1="20" x2="10" y2="32"/></svg><span class="sr-only">i</span></span>ca</div>
    <div class="fmeta"><a href="https://www.linkedin.com/in/ketibakiri" target="_blank" rel="noopener">LinkedIn</a> &nbsp;&middot;&nbsp; <a href="https://github.com/ketibak-ai" target="_blank" rel="noopener">GitHub</a></div>
  </div>
</footer>

</body>
</html>
```

**What to fill in:**
- `YOUR POST TITLE` (appears twice, plus once in the page `<title>`)
- `ONE SENTENCE SUMMARY OF THE POST`
- `TOPIC NAME` (appears twice — e.g. "Integrating AI Into Real Workflows")
- `MONTH DAY, YEAR`
- The paragraphs and optional subheadings under `post-body`

Each extra paragraph is just `<p>Your text here.</p>`. Each extra subheading is `<h2>Your subheading</h2>`.

---

## Step 2 — List it on the topic page

1. Open the topic's `index.html` (e.g. `blog/integrating-ai-workflows/index.html`)
2. Click the pencil icon to edit
3. Find the `<div class="post-list">` section
4. Add a new card **above** the existing ones (newest first):

```html
<a class="post-card" href="my-new-post-title/index.html">
  <div class="post-date">MONTH DAY, YEAR</div>
  <h3>YOUR POST TITLE</h3>
  <p>ONE SENTENCE SUMMARY OF THE POST.</p>
</a>
```

5. Commit changes.

---

## Step 3 — Update the post count on the main blog page

1. Open `blog/index.html`, click the pencil icon
2. Find the card for the topic you posted in
3. Change `<div class="post-date">1 post</div>` to the new total (e.g. `2 posts`)
4. Commit changes

---

## That's it

The site rebuilds automatically after each commit — give it 30–60 seconds, then refresh pinkanalytica.com to see it live. If something looks broken, you can always undo by clicking **History** on the file in GitHub and reverting to the previous version.

For anything beyond adding posts — new pages, layout or styling changes, icons, colors — it's safer to come back and ask for help, since those touch multiple files at once.
