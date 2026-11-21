# Loose Leaf: how to put it online for free

This folder has two files that go online:

- `index.html` is the site.
- `content.json` holds all the text (posts, About me, contact). You change your site by changing this file.

## 1. Host it for free (pick one)

You get a free address like `yourname.github.io` or `yourname.netlify.app`. A custom domain such as `kushan.com` costs money; free options are the subdomains below.

**Netlify (easiest, no account tools needed)**
1. Go to app.netlify.com and sign up for free.
2. Choose "Add new site", then "Deploy manually".
3. Drag this whole folder onto the page. Your site is live in under a minute.
4. In Site settings, choose "Change site name" to get `your-name.netlify.app`.

**GitHub Pages**
1. Create a free GitHub account and a new public repository named `yourname.github.io`.
2. Upload `index.html` and `content.json` to it.
3. In the repository, open Settings, then Pages, and set the source to the main branch.
4. Your site appears at `https://yourname.github.io`.

**Cloudflare Pages**: create a free account, choose "Create a project", then "Upload assets", and drop in the folder. You get `your-name.pages.dev`.

Check each service's current free-plan terms before you rely on it.

## 2. Open edit mode (only you)

Edit mode is hidden from visitors. Open your site once with this ending on the address:

    https://your-site-address/#kushan-edit-2026

An "Edit mode" switch then appears in the top bar, in that browser only. Choose "Exit owner mode" in the edit toolbar to hide it again.

Change the secret word: open `index.html` in a text editor, find `OWNER_KEY = "kushan-edit-2026"`, replace the text inside the quotes with your own word (letters, numbers and hyphens), and upload the file again.

## 3. Publish your edits to visitors

Edits you make in edit mode are saved in your own browser. Visitors do not see them until you publish them:

1. In edit mode, choose "Copy or import data" and then "Copy".
2. Open `content.json` on your host, delete everything in it, paste the copied text, and save.
   - Netlify: upload the folder again (or replace the file in the site's Deploys page).
   - GitHub: open `content.json` in your repository, click the pencil icon, paste, and commit.
3. Reload the site in a private window to check what visitors see.

If the page in your browser ever shows old text after you update `content.json`, use "Discard my changes" in the edit toolbar to load the published version again.

## Good to know

- The secret link keeps edit mode out of sight, but it is not a password system. Nothing a visitor does can change what other people see, because content only changes when you replace `content.json`.
- Contact details show as text with a Copy button, because email and phone links often fail on hosted pages.
