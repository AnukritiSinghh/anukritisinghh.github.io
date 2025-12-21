# GitHub Setup Guide

## Step 1: Install Git (if not already installed)

1. Download Git for Windows: https://git-scm.com/download/win
2. Install with default settings
3. Restart your terminal/PowerShell after installation

## Step 2: Verify Git Installation

Open PowerShell or Command Prompt and run:
```bash
git --version
```

## Step 3: Configure Git (First Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "anukriti@terpmail.umd.edu"
```

## Step 4: Initialize Git Repository (if not already initialized)

Navigate to your project folder:
```bash
cd "E:\anukritisinghh.github.io-main\anukritisinghh.github.io-main"
```

Initialize git (if needed):
```bash
git init
```

## Step 5: Add All Files

```bash
git add .
```

## Step 6: Commit Your Changes

```bash
git commit -m "Update website with modern design and add video/GIF support for projects"
```

## Step 7: Connect to GitHub Repository

### Option A: If repository already exists on GitHub

```bash
git remote add origin https://github.com/anukritisinghh/anukritisinghh.github.io.git
```

### Option B: If you need to create a new repository

1. Go to https://github.com/new
2. Repository name: `anukritisinghh.github.io`
3. Make it **Public** (required for GitHub Pages)
4. **DO NOT** initialize with README, .gitignore, or license
5. Click "Create repository"
6. Then run:
```bash
git remote add origin https://github.com/anukritisinghh/anukritisinghh.github.io.git
```

## Step 8: Push to GitHub

```bash
git branch -M main
git push -u origin main
```

If you get an error about authentication, you may need to:
- Use a Personal Access Token instead of password
- Or use GitHub Desktop (easier option)

## Step 9: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll to **Pages** section
4. Under "Source", select **main branch** (or **master** if that's your branch)
5. Click **Save**
6. Your site will be live at: `https://anukritisinghh.github.io`

## Alternative: Using GitHub Desktop (Easier)

1. Download GitHub Desktop: https://desktop.github.com/
2. Sign in with your GitHub account
3. Click **File** → **Add Local Repository**
4. Browse to: `E:\anukritisinghh.github.io-main\anukritisinghh.github.io-main`
5. Click **Publish repository** button
6. Make sure it's named: `anukritisinghh.github.io`
7. Click **Publish**

## Troubleshooting

### If you get "remote origin already exists" error:
```bash
git remote remove origin
git remote add origin https://github.com/anukritisinghh/anukritisinghh.github.io.git
```

### If you need to force push (be careful!):
```bash
git push -u origin main --force
```

### Check your remote:
```bash
git remote -v
```

## Adding Videos/GIFs Later

After pushing, you can add your video files:
1. Add files to `/videos/` or `/files/` folders
2. Run:
```bash
git add videos/ files/
git commit -m "Add project videos and GIFs"
git push
```

