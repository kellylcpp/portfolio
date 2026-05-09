# Entertainment Marketing Portfolio

A professional portfolio website built with [Quarto](https://quarto.org) and deployed via GitHub Pages.

## 📁 File Structure

```
portfolio/
├── _quarto.yml          # Site config, navbar, Google Analytics
├── custom.scss          # Navy/white/gold color theme
├── index.qmd            # Home page
├── projects.qmd         # Marketing projects showcase
├── dashboard.qmd        # Analytics dashboard (Observable JS charts)
├── presentation.qmd     # Revealjs slide deck
├── contact.qmd          # Contact form
├── images/              # Add your headshot, logo, favicon here
└── files/               # Add your resume PDF here
```

## 🚀 Quick Setup

### 1. Clone the template repo
```bash
git clone https://github.com/CCIDM/portfolio-website-template
cd portfolio-website-template
```

### 2. Replace files
Copy the `.qmd` files and `_quarto.yml` from this project into the cloned repo, replacing the originals.

### 3. Personalize — find every placeholder:
- `Alex Morgan` → Your full name
- `alex.morgan@email.com` → Your email
- `linkedin.com/in/alexmorgan` → Your LinkedIn URL
- `github.com/alexmorgan` → Your GitHub URL
- `Your University, 2025` → Your school and grad year
- `Los Angeles, CA` → Your city
- `G-XXXXXXXXXX` in `_quarto.yml` → Your GA4 Measurement ID

### 4. Add your photo
Place your headshot at `images/headshot.jpg`, then replace the initials avatar in `index.qmd`:
```html
<!-- Replace this div: -->
<div style="...font-size:2.5rem;color:#C9A84C;">AM</div>

<!-- With this: -->
<img src="images/headshot.jpg" style="width:120px;height:120px;border-radius:50%;border:3px solid #C9A84C;object-fit:cover;">
```

### 5. Add your resume
Place your resume PDF at `files/your-name-resume.pdf` and update the link in `contact.qmd`.

### 6. Set up the contact form
Register at [Formspree.io](https://formspree.io) (free tier), create a form, and replace `YOUR_FORM_ID` in `contact.qmd` with your actual form ID.

### 7. Set up Google Analytics
1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a GA4 property for your site
3. Copy the Measurement ID (starts with `G-`)
4. Replace `G-XXXXXXXXXX` in `_quarto.yml`

### 8. Preview locally
```bash
quarto preview
```

### 9. Render the site
```bash
quarto render
```

### 10. Deploy to GitHub Pages
In your repo Settings → Pages → set source to `gh-pages` branch, then:
```bash
quarto publish gh-pages
```

Your site will be live at: `https://yourusername.github.io/your-repo-name`

## ✏️ Customizing Projects
Each project card in `projects.qmd` has a clear structure. To add your own real projects:
1. Change the emoji in the thumbnail div
2. Update the category label, title, and description paragraphs
3. Edit the bullet points under "Key Results"
4. Update the `<span class="proj-tag">` tags

## 📊 Updating Dashboard Data
In `dashboard.qmd`, find the Observable JS block labeled `campaignData` and update the numbers with your actual campaign metrics.

## 🎨 Changing Colors
All colors are defined as Sass variables at the top of `custom.scss`. Modify `$navy`, `$gold`, etc. to change the entire palette.
