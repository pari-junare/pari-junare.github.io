# Academic Website - Single Page Design

A modern, minimalist academic website built with pure HTML and CSS. Single-page layout with smooth scrolling navigation - no frameworks, no build tools required.

## Features

- ✨ Clean, professional single-page design
- 📱 Fully responsive (mobile, tablet, desktop)
- ⚡ Fast loading (no dependencies)
- 🎨 Easy to customize with CSS variables
- ♿ Accessible HTML structure
- 🔗 Smooth scrolling anchor navigation

## What's Included

- **index.html** - Your complete website (includes all sections)
- **style.css** - All styling
- **README.md** - This file

All content is on ONE page - no separate navigation tabs needed!

## Quick Start

### Step 1: Customize Content

Open `index.html` in a text editor and replace placeholder text with your information:

#### Replace everywhere:
- `Your Name` → Your full name
- `your.email@university.edu` → Your email
- `[Your Field]` → Your academic discipline
- `[Your Position/Degree]` → Your position (e.g., "PhD student")
- `[Your Institution]` → Your university name

#### Profile Section:
- Update the welcome text in the `.welcome-section`
- Add your social media links (Twitter, etc.)
- Link your CV PDF

#### Research Section:
- Add your publications with titles, authors, years
- Link to DOI, PDF, Google Scholar
- Update research areas

#### Teaching Section:
- List your current courses using the provided three-line format (title + period, university, instructor)
- Add past courses similarly or simply as paragraphs
- Describe your teaching philosophy

The template includes example markup and accompanying CSS to make the course name bold and larger, the time period italic, the university italic on the next line, and the professor name bold on the third line.

#### CV Section:
- Fill in education details
- Add your current position
- List grants, awards, service
- Link to PDF CV

### Step 2: Add Your Photo (Optional but Recommended)

1. Create an `assets` folder in your repository
2. Save your headshot as `profile.jpg` (recommend: 500×500px)
3. The code already references this location

### Step 3: Create GitHub Repository

1. Go to [github.com](https://github.com)
2. Click **"New repository"**
3. **IMPORTANT:** Name it: `yourusername.github.io` (replace with your actual GitHub username)
4. Select **Public**
5. Click **"Create repository"**

### Step 4: Upload Files to GitHub

**Easy Method - Web Upload:**

1. Open your new repository on GitHub
2. Click **"Add file"** → **"Upload files"**
3. Drag & drop these files:
   - `index.html`
   - `style.css`
   - `README.md`
4. If you created an `assets` folder:
   - Create the `assets` folder in your repo first
   - Upload `profile.jpg` there
5. Scroll down and click **"Commit changes"**

**Using Git Command Line:**

```bash
cd /path/to/academic-website
git init
git add .
git commit -m "Initial commit: academic website"
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Step 5: Enable GitHub Pages

1. Go to your repository → **Settings** (gear icon)
2. Scroll to **"Pages"** section
3. Under "Source," select **"main"** branch
4. Click **"Save"**

### Step 6: View Your Website

Your website is now live at:
```
https://yourusername.github.io
```

**Note:** It may take 1-3 minutes to deploy. If it doesn't appear:
- Wait and refresh your browser
- Check Settings → Pages to verify deployment status

---

## How the Layout Works

### Single Page Structure

All content is on `index.html`:

```
Header (Your Name)
    ↓
Profile Section
├── Profile Photo
├── Navigation Links (Research / Teaching / CV)
└── Welcome Text
    ↓
Research Section (#research)
├── Research Areas
├── Publications
└── Working Papers
    ↓
Teaching Section (#teaching)
├── Current Courses
├── Past Courses
└── Student Mentoring
    ↓
CV Section (#cv)
├── Education
├── Positions
├── Grants & Funding
└── Professional Service
    ↓
Footer
```

**Navigation:** Users click "Research," "Teaching," or "CV" links to scroll to those sections. No page reloads—everything is smooth and fast!

---

## Customizing Colors

Edit `style.css` at the top to change your color scheme:

```css
:root {
    --primary-color: #2c3e50;      /* Dark blue - headings */
    --secondary-color: #3498db;    /* Light blue - links */
    --accent-color: #e74c3c;       /* Red - hover effects */
    --light-text: #666;            /* Gray - body text */
}
```

### Color Scheme Ideas

**Professional Academic:**
```
--primary-color: #1e3a5f;
--secondary-color: #4a90e2;
--accent-color: #e74c3c;
```

> The stylesheet also includes helper classes for the teaching section (`.course-header`, `.course-period`, `.course-institution`, `.course-instructor`) that control font size, bolding, and italics. You can adjust or remove them as needed.

**Modern Green:**
```
--primary-color: #2d5016;
--secondary-color: #52b788;
--accent-color: #d62828;
```

**Classic Purple:**
```
--primary-color: #4a2463;
--secondary-color: #9d4edd;
--accent-color: #ff006e;
```

---

## File Structure

```
your-site/
├── index.html        # Your complete website
├── style.css         # All styling
├── README.md         # This file
└── assets/           # (Optional) Folder for images
    ├── profile.jpg   # Your headshot
    └── cv.pdf        # Your CV (optional)
```

---

## Making Updates

After deploying, you can update content anytime:

**Via GitHub Web Editor:**
1. Click on `index.html`
2. Click the pencil icon (Edit)
3. Make changes
4. Click "Commit changes"
5. Changes appear in ~1 minute

**Via Git Command Line:**
```bash
# Make changes to index.html or style.css locally
git add .
git commit -m "Update publications"
git push
```

---

## Advanced Customizations

### Change Profile Photo Size

In `index.html`, find `.profile-photo img` section and adjust in `style.css`:

```css
.profile-photo img {
    width: 200px;    /* Change this */
    height: 200px;   /* And this */
    border-radius: 50%;
}
```

### Add More Sections

Simply add a new section to `index.html`:

```html
<section id="projects" class="content-section">
    <div class="container-center">
        <h2>Projects</h2>
        <h3>Project Title</h3>
        <p>Project description here...</p>
    </div>
</section>
```

Then add a link to it in the navigation:

```html
<div class="nav-links">
    <a href="#research">Research</a>
    <span class="separator">/</span>
    <a href="#teaching">Teaching</a>
    <span class="separator">/</span>
    <a href="#projects">Projects</a>
    <span class="separator">/</span>
    <a href="#cv">CV</a>
</div>
```

### Add a CV PDF Download

1. Save your CV as `cv.pdf`
2. Upload to `assets` folder
3. In the CV section, the download link already references this:

```html
<a href="assets/cv.pdf" class="cv-download">Download PDF</a>
```

### Add Social Media Links

In the `.welcome-section`, add more links:

```html
<p>
    Follow me on <a href="https://twitter.com/yourusername" target="_blank">Twitter</a>,
    <a href="https://scholar.google.com/citations?user=XXXXX" target="_blank">Google Scholar</a>,
    or <a href="https://github.com/yourusername" target="_blank">GitHub</a>.
</p>
```

---

## Tips for Academic Websites

✨ **Keep it simple** - Visitors want to find information quickly
📚 **Link to publications** - DOI, PDF, Google Scholar links are essential
🎓 **Update regularly** - Add new publications and courses as they happen
📸 **Use a good photo** - Professional headshot (500×500px minimum)
🔗 **Include all links** - Email, CV, Scholar profile, ORCID, etc.
📱 **Test on mobile** - Most academics visit on phones

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Site not showing | Repo must be named exactly `yourusername.github.io` |
| Pages disabled | Go Settings → Pages → Select "main" branch |
| Styles not loading | Make sure `style.css` is in root folder |
| Links not working | Check filenames are exact (case-sensitive) |
| Photo not showing | Verify `assets/profile.jpg` exists in repo |
| Takes forever to appear | GitHub Pages needs 1-3 min to deploy |

---

## Browser Support

Works on all modern browsers:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers

---

## License

Feel free to use and modify this template for your academic website. Enjoy!

---

**Questions?** The comments in `index.html` and `style.css` explain each section. Customize freely!
