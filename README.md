# Uzair Amin — Portfolio

A responsive, four-page portfolio for a video editor, videographer, and content creator. Plain HTML, CSS, and JavaScript. No installation, build, paid service, or API key required.

## Start here

Open `index.html` to view it on your computer. The four visitor pages are Home, Work, About, and Contact. All links use relative paths so the site works in a GitHub Pages project repository.

**Before sharing publicly:** replace the clearly marked sample projects in `content.js`, add Uzair’s real social links and email, and review the About copy with him. The included SVG artwork is original illustrative placeholder artwork, not his actual work. No client claims or testimonials have been invented.

## Update everything in one file

Open **content.js** in GitHub and click the pencil icon. Edit the values, then choose Commit changes. GitHub Pages will update after deployment. Keep the first line `window.PORTFOLIO =` and the final semicolon. Use double quotes for strings; put commas between items, but not after the last item. Use `\"` for quotes within a string.

### Profile

- `email`: his real email address. Enables an email link and opens the visitor’s email app with the completed project brief.
- `instagram`: full Instagram profile URL.
- `youtube`: full YouTube channel URL.
- `whatsapp`: international number using digits only, e.g. Pakistan starts with `92`; no spaces or plus sign.
- `portrait`: add a photo to assets and use `assets/uzair.jpg`, or leave blank for the monogram.
- `about`, `intro`, `availability`, `title`: editable page text.
- `name` and `tagline` are retained as reference fields; page headlines and the visible brand name are designed in HTML. Change these directly in the HTML if desired.

### Add a project

Add this object to the `projects` array (put a comma between this and the previous object):

```js
{
  "id": "my-first-film",
  "title": "My first film",
  "category": "Films",
  "year": "2026",
  "description": "A short description of this real project.",
  "role": "Videography & editing",
  "url": "https://www.youtube.com/watch?v=YOUR_VIDEO_ID",
  "thumbnail": "assets/my-first-film.jpg",
  "featured": true,
  "demo": false,
  "comments": []
}
```

Upload the cover image into `assets/`. Use a landscape JPG or WebP, ideally 1200px wide. Use a unique id for each project. Set `featured` to true to include it among the first three featured projects on Home. New category names become filter buttons automatically. Remove sample projects once you add real ones.

YouTube watch, youtu.be, and Shorts links support optional embedded playback. Visitors choose to load the YouTube player. A link to the original video is also shown in case embedding is disabled by the owner. Instagram Reel/post links open on Instagram; they do not depend on Instagram’s embed script. Any other full HTTPS video link opens on its original platform.

### Comments and testimonials

Project `comments` are curated quotes added by Uzair, not an open public comment feed:

```js
"comments": [
  { "author": "Client name (with permission)", "text": "Their real approved comment." }
]
```

Global `testimonials` appear on About only when added:

```js
"testimonials": [
  { "author": "Client name", "role": "Project or role", "text": "A real approved testimonial." }
]
```

Never add invented feedback. Public visitor comments would require an external commenting service or backend; they are not part of this static version.

## Publish on GitHub Pages — easiest method

1. Create a GitHub repository, for example `uzair-portfolio`. A public repository is the simplest option for free Pages hosting.
2. Extract the downloaded ZIP. Upload the **contents** of the `uzair-amin` folder to the repository root, so `index.html` sits at the root rather than inside a second folder. Include assets.
3. Open repository **Settings → Pages**.
4. Under Build and deployment, choose **Deploy from a branch**.
5. Choose **main** and **/(root)**, then Save.
6. Wait for the Pages deployment to finish. Use the URL shown in Settings → Pages; typically `https://USERNAME.github.io/uzair-portfolio/`.

No special hosting configuration is needed. `.nojekyll` disables Jekyll processing.

### Optional GitHub Actions deployment

If uploading through Git or a method that preserves hidden directories, an optional `.github/workflows/pages.yml` is included. In Settings → Pages, choose **GitHub Actions** instead of branch deployment. The workflow publishes the root static website on pushes to main. Use one deployment method. If the GitHub web uploader doesn’t include hidden files, branch deployment is fine.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Contact form behavior

The form opens a drafted message in the visitor’s email app when Uzair’s email is configured. It does not automatically send anything. Without an email address, it copies the brief (with a manual-copy fallback). There is no server, inbox database, visitor account, or storage of submitted details.

## Files

- `index.html`, `work.html`, `about.html`, `contact.html`: the four pages.
- `content.js`: profile, links, projects, services, and approved comments.
- `style.css`: responsive design.
- `app.js`: filters, project dialog, video player, and contact brief.
- `assets/`: original SVG sample illustrations, favicon, and your uploaded images.

## Verification

JavaScript syntax and local file/link integrity were checked. Browser visual QA was unavailable in the creation environment. Verify the appearance on mobile and desktop, test your real video links, and send yourself a project enquiry before sharing the site.
