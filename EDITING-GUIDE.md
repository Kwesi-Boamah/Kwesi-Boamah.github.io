# How to Update jboamah.com

Your website is built from the GitHub repository **Kwesi-Boamah/Kwesi-Boamah.github.io** (branch `master`). Every time you save (commit) a change there, GitHub Pages rebuilds the site automatically. The new version is usually live at https://jboamah.com within 1–3 minutes. You do not need to touch Cloudflare for normal content updates.

## The easiest way to edit (in your browser)

1. Go to https://github.com/Kwesi-Boamah/Kwesi-Boamah.github.io and sign in.
2. Open the file you want to change (see the table below).
3. Click the pencil icon (Edit this file).
4. Make your change. Keep the formatting the same: dashes for list items, `**bold**`, and so on.
5. Click **Commit changes…**, write a short note (e.g. "Update awards"), then click **Commit changes** again.
6. Wait 1–3 minutes, then refresh https://jboamah.com. If you still see the old version, press Ctrl+F5 (Windows) or Cmd+Shift+R (Mac).

## Which file controls what

| What you want to change | File to edit |
| --- | --- |
| Home page text (About Me, Research Interests, Publications summary, Education, Selected Awards, Contact) | `_pages/about.md` |
| CV page on the website (full Education, Work, Awards, Service, Skills) | `_pages/cv.md` |
| Sidebar: name, short bio, email, location, employer | `_config.yml` (the `author:` section) |
| Google Scholar, ORCID, LinkedIn links | `_config.yml` (`googlescholar`, `orcid`, `linkedin`) |
| Research page entries | Files in `_publications/` (one file per paper) |
| Top menu (Research, CV) | `_data/navigation.yml` |
| Profile photo | Replace `images/PIC.jpeg` (keep the same file name) |
| Colours | `_sass/theme/_default_light.scss` (see below) |
| Fonts, buttons, spacing, photo frame | `assets/css/main.scss` (bottom of the file) |

## Replacing your CV (PDF)

The website links to `files/John_Boamah_CV.pdf`. The older link `files/cv.pdf` also exists.

1. Save your Word CV as a PDF (in Word: File → Save As → PDF).
2. Rename the PDF to exactly **John_Boamah_CV.pdf**.
3. On GitHub, open the `files` folder, click **Add file → Upload files**, and drag the PDF in. Uploading a file with the same name replaces the old one.
4. Click **Commit changes**.
5. Optional: upload the same PDF again under the name **cv.pdf**, so the older link also shows the new CV.

Remember that the CV page (`_pages/cv.md`) and the home page awards (`_pages/about.md`) are text. They do not update automatically from the PDF, so edit them too when your CV changes.

## Adding a new publication

1. Open the `_publications` folder and copy an existing file, e.g. `2025-06-26-e-levy-stock-market.md`.
2. Create a new file named `YYYY-MM-DD-short-title.md` with the same structure. Update `title`, `date`, `venue`, `paperurl` (the DOI link), `citation`, `excerpt`, and the `permalink` (it must be unique).
3. Set `category:` to one of `manuscripts` (journal articles), `chapters` (book chapters) or `workingpapers` (working papers).
4. Also add a one-line entry to the Publications list in `_pages/about.md` and `_pages/cv.md`.

## Changing the colours

Open `_sass/theme/_default_light.scss`. The main values are:

- `$primary-color` (currently `#1f3a5f`, deep navy): buttons and accents
- `--global-link-color` (currently `#1f4e8c`): links
- `--global-link-color-hover` (currently `#13294b`): links on hover
- `--global-text-color` (currently `#2b2f33`): body text

Replace a hex code with another (pick colours at https://htmlcolorcodes.com) and commit. Keep text and link colours dark enough to read easily on white.

## If the site stops updating

A typo in a `.scss` or `_config.yml` file (for example, a missing `}` or a bad indent) makes the build fail. When that happens, the live site silently stays on the old version.

- Check the build status at https://github.com/Kwesi-Boamah/Kwesi-Boamah.github.io/deployments, or look for a red ✗ next to your latest commit.
- To undo a bad change, open the file's **History**, view the previous version, and copy it back. You can also ask me to fix it.
- In `_config.yml`, keep the spacing exactly as it is (spaces, not tabs), and put text values in "quotes".

## Asking me to do it

You can also just send me the change, such as an updated CV, a new paper or new wording. I'll edit the repository, check the build, and confirm it's live.
