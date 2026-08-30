# The NeuroCove Foundation

The website for The NeuroCove Foundation, a nonprofit dedicated to sharing immigrant stories and humanizing each immigrant's journey through illustrated books.

A multi-page static site built with plain HTML and CSS.

## Pages

| Page | File | Content |
|---|---|---|
| Home | `index.html` | Hero, milestone timeline, photo highlights, Instagram feed |
| About | `about.html` | Who the foundation is and why it exists |
| Our Impact | `impact.html` | Results, numbers, and stories from the work |
| Initiatives | `initiatives.html` | Programs including the Cove of Stories |
| Resources | `resources.html` | Materials for the community |
| Join Us | `get-involved.html` | Volunteer and participation pathways |

`mission.html` is a redirect page that forwards to `impact.html`, preserving an older URL that was already in circulation.

Volunteer signups, story submissions, and other forms are handled through external Google Forms.

## Running it locally

Open `index.html` in any browser. No build step, no dependencies.

To serve it over HTTP:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Tech stack

- Semantic HTML5 across seven pages
- A single shared stylesheet, roughly 3,100 lines, with no framework
- Google Forms for all form handling
- Embedded Instagram feed on the home page

## Project structure

```
index.html          Home
about.html          About
impact.html         Our Impact
initiatives.html    Initiatives
resources.html      Resources
get-involved.html   Join Us
mission.html        Redirect to impact.html

css/styles.css      All site styling

Media/              Photography and logos
  partners/         Partner organization logos
```

## Partners

Partner logos in `Media/partners/` include the UN DTC, RefugeeOne, Young Planet Leaders, SSIP, Capital Storytelling, Dynamic Teen Coalition, and Their Story Is Our Story.

## Repository note

The repository is named **NueroCove**, but the organization is **NeuroCove** — the `e` and `u` are transposed. The site content spells it correctly throughout; only the repository name is affected.

This is worth fixing before the repo is shared widely. On GitHub, go to **Settings → General → Repository name** and rename it to `NeuroCove`. GitHub will redirect the old URL automatically, so existing links will not break. If the site is deployed on GitHub Pages, the published URL will change to match, so update any links pointing at it.

## Deploying

The site is fully static and can be hosted free on GitHub Pages. Go to **Settings → Pages**, select the `main` branch as the source, and it will be live at `https://katesatori-mal.github.io/NeuroCove/`.

Netlify and Vercel both work as well. For a custom domain, add a `CNAME` file with the domain name and point the DNS at the host.

## Possible improvements

- Add `<meta name="description">` tags to the interior pages; only the home page has one
- Add Open Graph tags so links shared on social media show a preview image and title
- Compress the photography in `Media/` — the images appear to be straight from a phone camera and are likely slowing page loads
- Rename image files from `IMG_4225.jpg` to descriptive names, which helps both maintenance and image search
