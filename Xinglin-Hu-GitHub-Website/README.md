# Xinglin Hu

Personal academic website, published with GitHub Pages.

Website: https://xinglin-hu.github.io/

## Publish using GitHub in your browser

1. Upload these files and folders to the root of the public repository `xinglin-hu.github.io` under the account `Xinglin-Hu`.
2. In **Settings → Pages**, select **Deploy from a branch**, then **main** and **/ (root)**. Save.
3. Wait for the Pages build to finish, then visit the website.

The repository root must contain `index.html`, `_config.yml`, `_data`, `assets`, and `files`. Upload the extracted contents, not the ZIP or its enclosing folder.

## Edit in your browser

Open a file, click the pencil, edit, and commit to `main`. GitHub republishes the site automatically.

| Content | File |
| --- | --- |
| Biography, contact details, interests | `_data/profile.yml` |
| Publications and links | `_data/publications.yml` |
| Research and industry experience | `_data/experience.yml` |
| Education | `_data/education.yml` |
| Projects and reading seminars | `_data/projects.yml` |
| Honors | `_data/awards.yml` |
| Downloadable CV | `files/cv.pdf` |
| Site title, description, URL | `_config.yml` |
| Layout | `index.html` |
| Styles | `assets/style.css` |

Keep YAML indentation and quotation marks when editing. Duplicate a complete entry to add a publication. Update the `updated` field in `_data/profile.yml` after changing the content.

List each research work once in `publications.yml`. Use its `versions` list for an alternate title and venue of the same work; otherwise keep `versions: []`. ORGEval and its ICML CTB Workshop title are grouped this way.

Optional Google Scholar and portrait fields start empty. They appear only after a real URL or image path is added. To add a portrait, upload it under `assets` and set `portrait` to a path such as `assets/portrait.jpg`.

Replace `files/cv.pdf` with a new file of the same name to keep the download URL stable. The included CV is the original supplied PDF.

## Technical notes

This site uses GitHub Pages' built-in Jekyll support. It has no theme dependency, custom plugins, JavaScript, external fonts, or analytics. Do not add `.nojekyll`: the page is rendered from the data files by Jekyll. No local software installation or package maintenance is required for the browser workflow.

See [GUIDE.zh-CN.md](GUIDE.zh-CN.md) for the detailed Chinese setup guide. This guide and README are excluded from the published website.
