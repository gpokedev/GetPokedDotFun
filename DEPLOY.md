# 🚀 Deployment Guide

This guide covers multiple ways to deploy your Pokémon game online.

## Option 1: GitHub Pages (Recommended - Already Configured)

Your project already has a GitHub Actions workflow set up for automatic deployment!

### Steps:

1. **Create a GitHub Repository** (if you haven't already):
   - Go to https://github.com/new
   - Name it `pokemon` (or any name you prefer)
   - Don't initialize with README, .gitignore, or license (you already have them)
   - Click "Create repository"

2. **Push Your Code to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/pokemon.git
   git push -u origin main
   ```
   Replace `YOUR_USERNAME` with your GitHub username.

3. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Click **Settings** → **Pages** (in the left sidebar)
   - Under "Source", select **GitHub Actions**
   - Save the settings

4. **Deploy**:
   - The GitHub Actions workflow (`.github/workflows/deploy.yml`) will automatically deploy on every push to `main`
   - Wait 1-2 minutes for deployment
   - Your game will be live at: `https://YOUR_USERNAME.github.io/pokemon/`

### Manual GitHub Pages (Alternative):
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main` / folder: `/ (root)`
   - Save

---

## Option 2: Vercel (Fast & Easy)

1. **Install Vercel CLI** (optional, or use web interface):
   ```bash
   npm install -g vercel
   ```

2. **Deploy**:
   ```bash
   vercel
   ```
   Follow the prompts. Or use the web interface:
   - Go to https://vercel.com
   - Import your GitHub repository
   - Vercel will auto-detect it's a static site
   - Click Deploy

3. **Your game will be live** at: `https://your-project.vercel.app`

**Note**: Make sure to set the build command to empty and output directory to `/` since it's a static site.

---

## Option 3: Netlify (Easy Drag & Drop)

1. **Build the project** (optional - not needed, it's already built):
   - Your project is already ready to deploy as-is

2. **Deploy**:
   - Go to https://app.netlify.com/drop
   - Drag and drop your project folder
   - Or connect your GitHub repository for continuous deployment

3. **Your game will be live** at: `https://random-name.netlify.app`

---

## Option 4: Surge.sh (Quick Command Line)

1. **Install Surge**:
   ```bash
   npm install -g surge
   ```

2. **Deploy**:
   ```bash
   surge
   ```
   - Follow the prompts
   - Choose a domain name (or use the random one)
   - Your project folder will be deployed

---

## Option 5: Cloudflare Pages

1. Go to https://pages.cloudflare.com
2. Connect your GitHub repository
3. Build settings:
   - Framework preset: None
   - Build command: (leave empty)
   - Build output directory: `/`
4. Click "Save and Deploy"

---

## 📝 Important Notes

### All Platforms:
- Your project is a **static site**, so no build step is needed
- Just deploy the root directory (`/`)
- Make sure all asset paths are relative (they already are: `./img/...`, `./audio/...`)

### CORS Issues:
- All the deployment platforms above handle CORS correctly
- You won't have the connection reset errors you see locally

### Custom Domain (Optional):
- Most platforms support custom domains for free
- Add your domain in the platform's settings

---

## ✅ Quickest Method

**For the fastest deployment right now:**

1. **GitHub Pages** - Push to GitHub and enable Pages (5 minutes)
2. **Netlify Drop** - Drag & drop your folder (1 minute, no account needed for testing)

---

## 🔄 Continuous Deployment

All methods above (except Surge manual deploy) support continuous deployment:
- **GitHub Pages**: Auto-deploys on push to `main` branch (already configured!)
- **Vercel/Netlify**: Auto-deploys on push to your connected branch
- **Cloudflare Pages**: Auto-deploys on push

Every time you push changes, your site will automatically update!






