# Surgery Day Builder - Complete Website

A complete, production-ready web application where users can create and share healthcare journey timelines using AI.

## ⚡ Quick Start

### For GitHub Pages (Documentation Site)
1. Push all files to GitHub
2. Go to Settings → Pages
3. Select `main` branch as source
4. Site will be live at `https://yourusername.github.io/repository-name/`

### For Actual Website Deployment
Deploy the Flask app to:
- Heroku
- AWS EC2
- DigitalOcean
- Your own server

See `COMPLETE_INSTALLATION_GUIDE.md` for details.

## 📁 What's Included

### Backend (Production-Ready Flask App)
- `app.py` - Complete Flask application
- `config.py` - Configuration
- `requirements.txt` - Python dependencies
- `models_health_journey.py` - Database models
- `services_journey_generator.py` - Claude AI integration
- `routes_journey.py` - API routes

### Frontend (HTML/CSS/JavaScript)
- 11 HTML templates (all pages)
- 4 CSS stylesheets (2000+ lines)
- 2 JavaScript files (chat functionality)

### Documentation
- `COMPLETE_INSTALLATION_GUIDE.md` - Setup guide
- `LAUNCH_YOUR_WEBSITE.md` - Quick start (15 min)
- `INTEGRATION_GUIDE.md` - Integration steps
- `DATA_STORAGE_GUIDE.md` - Database guide
- And more...

## 🚀 Setup (15 minutes)

```bash
# 1. Create virtual environment
python3 -m venv venv
source venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Create .env file
echo "ANTHROPIC_API_KEY=sk-ant-YOUR_KEY_HERE" > .env
echo "DATABASE_URL=postgresql://localhost/surgery_day_builder" >> .env
echo "SECRET_KEY=your-secret-key-here" >> .env

# 4. Set up database
createdb surgery_day_builder
flask db upgrade

# 5. Run server
flask run
```

Visit: http://localhost:5000

## 📋 Features

✅ User registration & login
✅ AI-powered journey builder (Claude)
✅ Beautiful timeline display
✅ Comments & reactions
✅ Shareable journeys (public/private)
✅ User dashboard
✅ Responsive design
✅ Error handling

## 🛠️ Technology Stack

- **Backend**: Flask + SQLAlchemy + PostgreSQL
- **Frontend**: HTML5 + CSS3 + Vanilla JavaScript
- **AI**: Claude API (Anthropic)
- **Authentication**: Flask-Login
- **Database Migrations**: Flask-Migrate

## 📖 Documentation

Start with these in order:

1. **COMPLETE_INSTALLATION_GUIDE.md** - Step-by-step setup
2. **LAUNCH_YOUR_WEBSITE.md** - Quick 15-minute start
3. **INTEGRATION_GUIDE.md** - Integrate into existing project
4. **DATA_STORAGE_GUIDE.md** - Database & storage
5. **README_SURGERY_DAY_BUILDER.md** - Full documentation

## 🔑 Environment Variables

Required:
```
ANTHROPIC_API_KEY=sk-ant-...
DATABASE_URL=postgresql://user:password@localhost/dbname
SECRET_KEY=your-secret-key
FLASK_ENV=development
```

Optional:
```
UPLOAD_FOLDER=static/uploads
MAX_FILE_SIZE=52428800
REDIS_URL=redis://localhost:6379/0
```

## 📱 Routes

### Public
- `GET /` - Homepage
- `GET /about` - About page
- `GET /resources` - Healthcare resources
- `GET /health-journey/<slug>` - View journey

### Authentication
- `POST /auth/register` - Register account
- `POST /auth/login` - Login
- `GET /auth/logout` - Logout

### User Routes (Login Required)
- `GET /journey/builder` - Create journey
- `GET /journey/dashboard` - Your journeys
- `POST /api/journey` - Publish journey

### API
- `POST /api/journey/chat` - Chat with AI
- `POST /api/journey/<id>/comments` - Comment on journey
- `POST /api/journey/<id>/upload-photo` - Upload photo

## 🚀 Deployment

### Heroku (Easiest)
```bash
heroku login
heroku create your-app-name
heroku addons:create heroku-postgresql
git push heroku main
heroku run flask db upgrade
```

### Docker
```bash
docker build -t surgery-day-builder .
docker run -p 8000:8000 surgery-day-builder
```

### AWS EC2
1. Launch Ubuntu instance
2. Install Python, PostgreSQL, Nginx
3. Clone repo
4. Set up virtual environment
5. Run gunicorn

See deployment guides in documentation.

## 🐛 Troubleshooting

**Database connection error:**
```bash
# Ensure PostgreSQL is running
createdb surgery_day_builder
```

**Module not found:**
```bash
# Activate venv and reinstall
source venv/bin/activate
pip install -r requirements.txt
```

**ANTHROPIC_API_KEY error:**
```bash
# Create .env file with your key
echo "ANTHROPIC_API_KEY=sk-ant-..." > .env
```

**Static files not loading:**
- Check CSS/JS file paths
- Clear browser cache
- Check Flask static folder

## 📞 Support

For issues or questions:
1. Check the documentation files
2. Review error messages in Flask console
3. Check database migrations
4. Verify environment variables

## 📄 License

Built for Peck's Mission healthcare storytelling platform.

## 🙏 Built With

- Flask
- SQLAlchemy
- PostgreSQL
- Claude API
- Vanilla JavaScript
- CSS3

---

**Ready to launch?** Follow `COMPLETE_INSTALLATION_GUIDE.md`!

For GitHub Pages only: The documentation and guides are accessible through this repository.

For the actual web application: Deploy using the instructions in the documentation.
