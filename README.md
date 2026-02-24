# My Article Podcast - GitHub Pages Setup

## 📁 Files in this folder

- `feed.xml` - RSS podcast feed (subscribe to this URL)
- `index.html` - Web page with episodes
- `episodes/` - Folder containing MP3 files

## 🚀 Deployment Instructions

### Step 1: Create a GitHub Repository

1. Go to https://github.com/new
2. Create a new repository named `podcast` (or any name you prefer)
3. Make it **Public** (required for GitHub Pages)
4. Don't initialize with README

### Step 2: Upload Files

```bash
# Navigate to this folder
cd /a0/usr/workdir/podcast_feed

# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial podcast feed"

# Add your remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/podcast.git

# Push to main branch
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository Settings
2. Click "Pages" in the left sidebar
3. Under "Source", select "Deploy from a branch"
4. Select branch: `main`, folder: `/ (root)`
5. Click "Save"

### Step 4: Get Your Podcast URL

After a few minutes, your podcast will be live at:

```
https://YOUR_USERNAME.github.io/podcast/feed.xml
```

### Step 5: Subscribe in Your Podcast App

**Pocket Casts:**
1. Tap + (Add) → + Add Podcast
2. Scroll down → "Add a podcast by URL"
3. Paste: `https://YOUR_USERNAME.github.io/podcast/feed.xml`

**Overcast:**
1. Tap + → Add URL
2. Paste the feed.xml URL

**Apple Podcasts:**
1. Open Podcasts app
2. Search → scroll down → "Subscribe by URL"
3. Paste the feed.xml URL

**Podcast Addict (Android):**
1. Tap + → Add podcast
2. "By URL" → paste feed.xml URL

## 📝 Adding New Episodes

When you want to add a new episode:

1. Generate the new MP3 file
2. Save it to `episodes/` folder
3. Update `feed.xml` - add new `<item>` at the top (after the existing item)
4. Update `index.html` - add new episode div
5. Commit and push:
   ```bash
   git add .
   git commit -m "Add episode: [Episode Title]"
   git push
   ```

## 🔧 Customization

Edit these in `feed.xml`:
- `<title>` - Your podcast name
- `<itunes:author>` - Your name
- `<itunes:email>` - Your email
- `<link>` - Your GitHub Pages URL

## 📊 File Structure

```
podcast/
├── feed.xml          # RSS feed (subscribe to this)
├── index.html        # Web page
├── episodes/
│   └── article_complete.mp3  # Episode 1
└── README.md         # This file
```

---

**Need help?** The RSS feed is the key file - podcast apps read this to discover episodes.
