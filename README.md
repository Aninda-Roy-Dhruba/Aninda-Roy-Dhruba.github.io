# Academic portfolio (GitHub Pages)

Static Jekyll site, built natively by GitHub Pages. No build tools, no Actions needed.

## Folder map
| Path | Purpose |
|---|---|
| `_data/profile.yml` | **All profile text**: intro, interests, research, projects, contact. Edit this for almost every change. |
| `assets/cv/CV.pdf` | Your CV. Replace it to update the download and in-browser view. |
| `_vlog/` | One Markdown file per vlog entry. |
| `templates/vlog-entry.md` | Entry template. |
| `_config.yml` | Site title, description, `url`, `baseurl`. |
| `_layouts/`, `_includes/`, `index.html`, `vlog/`, `assets/` | Layout code. You should not need to edit these. |

## Deploy to GitHub Pages
1. Create a repository. Name it `USERNAME.github.io` for a user site, or any name (e.g. `portfolio`) for a project site.
2. Upload all files (GitHub web UI: **Add file → Upload files**; keep the folder structure, including hidden `.gitkeep`).
3. Open `_config.yml` and set `url: "https://USERNAME.github.io"`. For a project site also set `baseurl: "/portfolio"` (the repo name); for a user site leave `baseurl: ""`.
4. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Save.
5. Wait one or two minutes. Your site appears at the address shown on that page.

## Preview locally (optional)
```
bundle install
bundle exec jekyll serve
```
Open http://localhost:4000 (add your `baseurl` if set).

## Edit profile content
Open `_data/profile.yml` on GitHub, click the pencil icon, edit, and commit. Lines marked `# TODO` need your input. A link with `url: ""` is hidden automatically.

## Replace the CV
Upload a new PDF to `assets/cv/` named exactly `CV.pdf` (overwrites the old one). To use another name, change `cv_file` in `profile.yml`.

## Add a vlog entry
1. Open `templates/vlog-entry.md`, copy its contents.
2. In `_vlog/`, choose **Add file → Create new file** named like `2026-11-15-first-update.md`.
3. Paste, fill in `title`, `date`, `description`, `video`, and optional text. Commit.
Entries sort newest first by `date`. Supported `video` values: YouTube watch or youtu.be links, Vimeo links, or a path to an `.mp4` in the repo. Omit `video` for a text-only entry.

**Edit** an entry by editing its file. **Remove** it by deleting the file. With no entries the page shows an empty-state message.

## Why Jekyll
It is the only static generator GitHub Pages builds without extra setup, and it lets entries be plain Markdown files with no component edits. The trade-off is that it needs `bundle` for local preview.
