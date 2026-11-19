# Haimabati Dey — Academic Research Website

A lightweight, static academic website for GitHub Pages. It uses plain HTML, CSS, JavaScript, and JSON content files. No framework, package manager, build step, or paid service is required.

## Design principles
- Restrained academic presentation: white background, dark text, subtle blue links, simple typography.
- Content-first pages with modest navigation.
- No fabricated publications, metrics, affiliations, or project results.
- Project resource links and image galleries are optional. Empty values are not rendered.

## Preview locally
Because the site loads JSON files with `fetch`, open it through a local web server rather than double-clicking `index.html`.

From this folder run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish on GitHub Pages
1. Download and extract this ZIP.
2. Open your repository: https://haimavathi-hub.github.io
3. Upload the **contents** of this folder to the repository root (not the enclosing folder).
4. Keep `index.html` at the repository root.
5. Commit the upload. GitHub Pages should publish the site at https://haimavathi-hub.github.io/.

If replacing the current site, keep a local backup of the current repository files first.

## Where to edit content
Edit the JSON files in `content/`:
- `profile.json` — name, professional headline, contact links, biography, research interests.
- `experience.json` — academic research experience.
- `industry.json` — industrial experience.
- `education.json` — degrees and institutions.
- `skills.json` — technical skills.
- `projects.json` — project descriptions and resource links.
- `publications.json` — selected conference papers.
- `posters.json` — poster presentations.
- `awards.json` — awards and honors.
- `teaching.json` — teaching and mentoring.

Keep JSON syntax valid: use double quotes around strings, commas between entries, and no trailing comma after the final item.

## Add a project paper, notebook, or repository
Open `content/projects.json`. Each project can include:
```json
{
  "title": "Project title",
  "category": "Research area",
  "summary": "One-sentence description",
  "details": "More detailed explanation.",
  "paper": "https://doi.org/...",
  "notebook": "https://github.com/username/repo/blob/main/example.ipynb",
  "github": "https://github.com/username/repo",
  "result_images": [
    {"src": "results/transmission-spectrum.png", "alt": "Transmission spectrum", "caption": "Simulated transmission"}
  ],
  "schematic_images": [
    {"src": "diagrams/device-schematic.png", "alt": "Device schematic", "caption": "Device geometry"}
  ],
  "tags": ["FDTD", "Nanophotonics"]
}
```
Remove or leave `paper`, `notebook`, or `github` as an empty string until you have a real public link. Empty links are not shown.

## Add graphical results and schematic diagrams
1. Put plot/result images in `results/`.
2. Put device schematics and workflow diagrams in `diagrams/`.
3. Add their relative paths in the relevant project's `result_images` or `schematic_images` list.
4. Use descriptive captions and alt text. Prefer PNG, JPG, or WebP images.
5. Only publish figures you own or have permission to share. Label simulated, experimental, illustrative, and conceptual figures accurately.

## Upload your CV
The supplied file was LaTeX source, not a compiled PDF. Compile it to PDF, then upload the PDF as:
`cv/resume.pdf`

The CV page already links to this path. You can also place a copy at the repository root and link it from the homepage if desired.

## Important content note
The website content is based on the CV supplied for this build. The project entries are selected project areas as named in that CV; they do not assert that a particular paper, notebook, schematic, or result is publicly available. Add resources only when you can verify and share them.

The public website currently shows your professional email, LinkedIn, and GitHub links. Your mobile number from the CV is deliberately not displayed by default; add it only if you want it public.

## Main files
- `index.html` and the other `.html` files: page structure.
- `assets/css/style.css`: appearance.
- `assets/js/site.js`: rendering and navigation.
- `content/*.json`: editable content.
- `cv/`, `papers/`, `notebooks/`, `diagrams/`, `results/`: resource folders.
