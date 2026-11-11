# Maren Osei: personal site

A one-file website (`index.html`). No build step, no installs, nothing to configure.
To preview it on your computer, double-click `index.html`.

## Put it online with GitHub Pages (about 10 minutes, no command line)

1. Create a free account at github.com.
2. Click **+ → New repository**.
   - **Name:** `your-username.github.io` gives you the clean address `https://your-username.github.io`.
     Any other name works too; the site will live at `https://your-username.github.io/that-name/`.
   - Set it to **Public**, then click **Create repository**.
3. On the new repo page, click **uploading an existing file**. Unzip this folder first, then drag in
   `index.html`, `README.md` and the `images` folder (drag the *contents* of the unzipped folder, not the folder itself).
   Click **Commit changes**.
4. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*,
   choose branch **main** and folder **/ (root)**, and click **Save**.
5. Wait one or two minutes and refresh. Your live link appears at the top of that page.

### Editing later
Open `index.html` on GitHub, click the pencil icon, make your change, and click **Commit changes**.
The live site updates in about a minute. Use Ctrl/Cmd+F to find the text you want.

## What to replace (everything is placeholder content)

| What | How to find it |
|---|---|
| Name, bio, experience, press, projects, services, quotes | Search for the text you see on the page. |
| Email `hello@marenosei.com` | Appears 3 times. Search for it and replace all. |
| Links (projects, press, social) | 18 links are marked `href="#" data-placeholder`. Swap `#` for the real URL and delete the word `data-placeholder`. |
| Visitor counter and footer badges | Just decoration. Edit or delete the lines near the bottom of the file. |
| Colors | The four `--accent`, `--bg`, etc. blocks near the top of the file (one per skin). |

## Adding photos

1. Upload your photos into the `images` folder on GitHub (**Add file → Upload files**).
2. In `index.html`, find a project card. It looks like this:

       <div class="tile a6"><span class="chip">S3</span>...</div>

   Add an `<img>` as the first thing inside the tile:

       <div class="tile a6"><img src="images/open-studio-hours.jpg" alt="Describe the photo"><span class="chip">S3</span>...</div>

   The photo fills the tile; the colored pattern stays behind it as a fallback, and the small label sits on top.
   (Delete the `<span class="chip">` if you don't want the label.)
3. For your portrait, do the same inside `<div class="portrait a10">`, and delete the `[ your photo goes here ]` caption.

## Using your own domain (optional)

Buy a domain (Namecheap, Porkbun, Cloudflare, about $10-15 a year), then in **Settings → Pages → Custom domain** enter it
and follow GitHub's DNS instructions. Tick **Enforce HTTPS** once it's available.

## Notes

- The contact form opens the visitor's email app with their message filled in. It doesn't send anything on its own.
- The site works as one page with hash links (`index.html#audio`), so back/forward buttons and shared links work on GitHub Pages without any extra setup.
