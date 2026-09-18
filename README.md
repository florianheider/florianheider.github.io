# florianheider.github.io

Source for <https://florianheider.github.io>.

Plain HTML and one stylesheet. There is no build step: the files here are
exactly what gets served.

| File | |
|---|---|
| `index.html` | Home |
| `research.html` | Working papers, publications, inactive papers |
| `policy.html` | Policy publications, commentary, other writing |
| `teaching.html` | Courses and doctoral supervision |
| `style.css` | All styling. Colours, fonts and the text column width are the variables at the top |
| `cv.pdf` | Curriculum vitae |

## Publishing a change

From this folder:

```bash
git add -A && git commit -m "Update" && git push
```

GitHub rebuilds the site within about a minute.

## Adding a paper

In `research.html`, copy an existing entry and change the text:

```html
<article class="pub">
  <h3 class="pub-title"><a href="LINK">Title</a></h3>
  <p class="pub-meta">with Co-author &middot; <em>Journal</em>, vol, pages (year)</p>
  <p class="pub-note">One or two sentences on what the paper shows.</p>
  <p class="pub-links"><a href="URL">SSRN</a></p>
</article>
```

Drop any line that does not apply. When a working paper is accepted, move the
whole block from Working papers down into Publications.

In `policy.html` and `teaching.html` the entries are shorter:

```html
<li><span class="t"><a href="URL">Title</a></span><span class="m">with Co-authors &middot; Series (year)</span></li>
```

## Adding a news item

In `index.html`, copy one `<li>` inside `<ul class="news">`. Newest first.

## Using your own domain

1. Buy a domain.
2. At the registrar, create four `A` records for the bare domain pointing to
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`,
   and a `CNAME` for `www` pointing to `florianheider.github.io`.
3. Settings → Pages → Custom domain, then tick "Enforce HTTPS".
