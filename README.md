# h1m_1208 — Personal Website

This repository contains the source for my personal website: a simple place to
share my projects, work, and interests.

🌐 **Visit the site:** [h1m1208.github.io](https://h1m1208.github.io)

## Files

- `index.html` is the About page and the website's home page.
- `projects.html` contains the projects page.
- `contact.html` contains the contact page.
- `style.css` contains the page and notes styles.
- `assets/images/profile_pic.png` is the profile image shown on the About page.
- `notes/index.html` is the cybersecurity notes index.
- `_layouts/` and `_includes/` contain the shared page layout and recursive
  notes navigation tree.

To change the profile picture, replace `assets/images/profile_pic.png` with
another image using the same filename. The image is cropped to fit a responsive
square frame without stretching.

The About, Projects, and Contact pages use plain HTML and CSS. GitHub Actions
fetches Markdown and image files from
[h1m1208/notes](https://github.com/h1m1208/notes) and builds the notes pages
with Jekyll. The directory structure is preserved under `/notes/`, with a
clickable tree beside the notes and the site's header and footer on every
page. The source repository's top-level `README.md` is excluded so it doesn't
replace the notes index. For example,
`pentesting/active_directory/active_directory.md` is published at
`/notes/pentesting/active_directory/active_directory/`.

The workflow runs when this repository's `main` branch changes, once daily to
pick up notes-repository updates, or when started manually from the Actions
tab. To enable deployment, set **Settings → Pages → Build and deployment →
Source** to **GitHub Actions**. The first deployment then publishes the site
and notes together.