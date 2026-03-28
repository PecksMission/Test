# 🚀 GitHub Setup Instructions - Surgery Day Builder

## Step 1: Create GitHub Repository

### Option A: New Repository
1. Go to https://github.com/new
2. **Repository name**: `surgery-day-builder` (or your preferred name)
3. **Description**: "AI-powered healthcare journey timeline creator"
4. **Public** (so it can be viewed)
5. **Check** "Add a README file" (optional, we have one)
6. Click "Create repository"

### Option B: If you have TEST repo
Use your existing `pecksmission/TEST` repository

---

## Step 2: Push Files to GitHub

### Using Git Command Line

```bash
# Clone the repository (if new)
git clone https://github.com/yourusername/surgery-day-builder.git
cd surgery-day-builder

# Or navigate to existing repo
cd /path/to/your/repo

# Copy ALL files from this package into the repo folder
# (All files from the Surgery_Day_Builder_COMPLETE.zip)

# Add all files
git add .

# Commit
git commit -m "Initial commit: Surgery Day Builder complete website"

# Push to GitHub
git push origin main
```

### Using GitHub Web Interface (No Git Required)

1. Go to your GitHub repository
2. Click "Add file" → "Upload files"
3. Drag & drop all files (or select them)
4. Scroll down
5. Click "Commit changes"
6. GitHub will upload everything

---

## Step 3: Enable GitHub Pages

1. Go to your repo → **Settings**
2. Scroll to **"Pages"** section (left sidebar)
3. Under "Build and deployment":
   - **Source**: Select `Deploy from a branch`
   - **Branch**: Select `main` and `/root`
   - Click **Save**

4. Wait 1-2 minutes
5. Your site will be live at:
   ```
   https://yourusername.github.io/surgery-day-builder/
   ```
   (or your repo name)

---

## Step 4: Verify Jekyll Build

The `_config.yml` file tells GitHub Pages how to build your site.

**Check Build Status:**
1. Go to your repo
2. Click **"Deployments"** (right sidebar)
3. Look for "GitHub Pages"
4. You should see a green ✅ if successful

**If build fails:**
1. Click on the failed deployment
2. Check error messages
3. Most common: Jinja2 template syntax (fixed for you!)

---

## What Gets Deployed to GitHub Pages

✅ **Documentation files** (.md, .txt)
✅ **HTML files** (templates)
✅ **CSS files** (stylesheets)
✅ **JavaScript files** (client-side scripts)
✅ **Images & static assets**

❌ **NOT deployed**: Python files (app.py, etc.) - those go on your server

---

## Your GitHub Pages Site Will Have

### Homepage
- Link to `README.md` (project overview)
- Links to all documentation

### Documentation Structure
- Installation guide
- Quick reference
- Integration guide
- And more...

### Code Files
- All HTML templates (viewable)
- All CSS (viewable)
- All JavaScript (viewable)
- Python files (readable source code)

---

## Deploy the ACTUAL Website

GitHub Pages is just for documentation and code viewing.

To actually **run the website**, deploy the Flask app to:

### Heroku (Easiest - Free tier available)
```bash
# Install Heroku CLI
brew install heroku  # or download

# Login
heroku login

# Create app
heroku create your-app-name

# Add PostgreSQL
heroku addons:create heroku-postgresql

# Push code
git push heroku main

# Run migrations
heroku run flask db upgrade

# Open site
heroku open
```

Your site will be live at: `https://your-app-name.herokuapp.com`

### AWS EC2
1. Launch Ubuntu instance
2. SSH in
3. Clone your GitHub repo
4. Install dependencies
5. Set up PostgreSQL
6. Run Flask app with Gunicorn
7. Point domain to EC2 IP

### DigitalOcean (Affordable VPS)
1. Create Ubuntu droplet
2. SSH in
3. Follow same steps as AWS

### Your Own Server
1. Copy files to server
2. Install Python & PostgreSQL
3. Run Flask app
4. Use Nginx as reverse proxy

See `COMPLETE_INSTALLATION_GUIDE.md` for detailed deployment instructions.

---

## File Structure After Upload

```
your-github-repo/
├── README.md                              # Main documentation
├── _config.yml                            # Jekyll configuration
├── Gemfile                                # Ruby dependencies
├── .gitignore                             # Git ignore file
│
├── COMPLETE_INSTALLATION_GUIDE.md
├── LAUNCH_YOUR_WEBSITE.md
├── INTEGRATION_GUIDE.md
├── DATA_STORAGE_GUIDE.md
├── QUICK_REFERENCE.md
├── And more documentation...
│
├── app.py                                 # Flask app (source code)
├── config.py                              # Configuration
├── requirements.txt                       # Python dependencies
├── models_health_journey.py               # Database models
├── services_journey_generator.py          # Claude API
├── routes_journey.py                      # Routes
│
├── templates_*.html                       # HTML templates
├── static_css_*.css                       # CSS files
├── static_js_*.js                         # JavaScript files
│
└── CaringBridge research docs & specs
```

---

## GitHub Pages URL Format

```
https://[username].github.io/[repository-name]/
```

Examples:
- `https://pecksmission.github.io/surgery-day-builder/`
- `https://yourusername.github.io/TEST/`
- `https://yourusername.github.io/my-app/`

---

## What Visitors Will See

When someone goes to your GitHub Pages URL:

1. **README.md** as homepage
2. **Links to documentation** (all .md files)
3. **Source code** viewable on GitHub
4. **Live preview** if you have an index.html

---

## Troubleshooting GitHub Pages

### Build failing?
1. Check `_config.yml` syntax
2. Check for Jinja2 template issues
3. Look at deployment logs

### Can't find site?
1. Verify Settings → Pages
2. Check branch is set to `main`
3. Wait 2-3 minutes for rebuild
4. Clear browser cache

### 404 errors?
1. Check file names are correct
2. Verify markdown files end in `.md`
3. Check folder structure

### Want custom domain?
1. Go to Settings → Pages
2. Under "Custom domain", enter your domain
3. Update DNS records (instructions will appear)

---

## Next Steps

1. ✅ Push all files to GitHub
2. ✅ Enable GitHub Pages (Settings → Pages)
3. ✅ Wait 2 minutes for build
4. ✅ Visit your GitHub Pages URL
5. ✅ Verify documentation is live
6. 🚀 Deploy Flask app to actual server (Heroku, AWS, etc.)

---

## Quick Checklist

- [ ] Created GitHub repository
- [ ] Pushed all files
- [ ] Enabled GitHub Pages
- [ ] Checked deployment status
- [ ] Visited GitHub Pages URL
- [ ] Saw homepage with documentation
- [ ] Read COMPLETE_INSTALLATION_GUIDE.md
- [ ] Ready to deploy Flask app

---

## Support

For GitHub Pages issues:
→ Check GitHub Pages documentation

For Flask app deployment:
→ See COMPLETE_INSTALLATION_GUIDE.md

For surgical journey builder issues:
→ See README_SURGERY_DAY_BUILDER.md

---

**You're all set!** 🚀

Push to GitHub → Enable Pages → Site goes live in 2 minutes.

Then deploy the actual Flask app to a server for the interactive website.
