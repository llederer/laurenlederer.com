# laurenlederer.com

A minimalist static personal site. No build step, no dependencies: five HTML files and one stylesheet.

```
index.html      Home
work.html       Work
venture.html    Venture
teaching.html   Teaching
writing.html    Writing
style.css       Shared styles (light + dark mode)
```

## Preview locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Any static host works. Three easy options:

**Netlify (drag and drop)**
Go to https://app.netlify.com/drop and drop this folder. Done.

**Vercel**
```sh
npm i -g vercel
vercel
```

**GitHub Pages**
```sh
git init && git add . && git commit -m "Initial site"
gh repo create laurenlederer.com --public --source=. --push
```
Then in the repo: Settings → Pages → Source: `main` / root.

### Custom domain
Point `laurenlederer.com` at your host. For GitHub Pages, add a `CNAME` file containing `laurenlederer.com` and set A records to GitHub's IPs. For Netlify/Vercel, follow the domain prompt in their dashboard.

## Editing

- Nav and footer are repeated in each file. To change them, edit all five (or search and replace).
- To add an item to Work, Teaching, or Writing, copy an existing `<li>` block in `.items`.
- `workshop/` is the rendered output of the Quarto project at `~/Desktop/wearables-quarto`. After re-rendering, copy `_site/` back into `workshop/`.
