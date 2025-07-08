# Deployment Guide for BlogCraft Elite

This guide will help you deploy your luxury blog CMS to GitHub and various hosting platforms.

## 📋 Prerequisites

- Node.js 18+ installed
- Git installed
- GitHub account
- Basic knowledge of command line

## 🚀 Step-by-Step GitHub Deployment

### 1. Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name it `blogcraft-elite` (or your preferred name)
5. Make it public or private
6. **Don't** initialize with README (we already have one)
7. Click "Create repository"

### 2. Download Project Files

Since you're working in Bolt, you'll need to download the project files:

1. In Bolt, click the download button to get all project files
2. Extract the files to a folder on your computer
3. Open terminal/command prompt in that folder

### 3. Initialize Git and Push to GitHub

```bash
# Initialize git repository
git init

# Add all files
git add .

# Make initial commit
git commit -m "Initial commit: BlogCraft Elite luxury blog CMS"

# Add your GitHub repository as origin
git remote add origin https://github.com/YOUR_USERNAME/blogcraft-elite.git

# Push to GitHub
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

### 4. Set up GitHub Pages (Optional)

If you want to host directly on GitHub Pages:

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" section
4. Under "Source", select "GitHub Actions"
5. Create `.github/workflows/deploy.yml` (see below)

## 🔄 GitHub Actions Deployment

Create this file in your repository: `.github/workflows/deploy.yml`

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout
      uses: actions/checkout@v4
      
    - name: Setup Node.js
      uses: actions/setup-node@v4
      with:
        node-version: '18'
        cache: 'npm'
        
    - name: Install dependencies
      run: npm ci
      
    - name: Build
      run: npm run build
      
    - name: Deploy to GitHub Pages
      uses: peaceiris/actions-gh-pages@v3
      if: github.ref == 'refs/heads/main'
      with:
        github_token: ${{ secrets.GITHUB_TOKEN }}
        publish_dir: ./dist
```

## 🌐 Alternative Hosting Options

### Netlify (Recommended)

1. Go to [Netlify.com](https://netlify.com)
2. Sign up/login with GitHub
3. Click "New site from Git"
4. Choose your repository
5. Set build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Deploy site"

### Vercel

1. Go to [Vercel.com](https://vercel.com)
2. Sign up/login with GitHub
3. Click "New Project"
4. Import your repository
5. Vercel will auto-detect Vite settings
6. Click "Deploy"

### Render

1. Go to [Render.com](https://render.com)
2. Sign up/login with GitHub
3. Click "New Static Site"
4. Connect your repository
5. Set:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Create Static Site"

## 🔧 Build Configuration

Your `package.json` already includes the necessary scripts:

```json
{
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  }
}
```

## 🌍 Custom Domain (Optional)

### For Netlify:
1. Go to Site settings > Domain management
2. Add custom domain
3. Follow DNS configuration instructions

### For GitHub Pages:
1. Add `CNAME` file to your repository root
2. Put your domain name in the file
3. Configure DNS with your domain provider

## 🔍 Troubleshooting

### Build Fails
- Check Node.js version (should be 18+)
- Run `npm install` to ensure all dependencies are installed
- Check for TypeScript errors: `npm run lint`

### Deployment Issues
- Ensure `dist` folder is being published
- Check build logs for errors
- Verify all environment variables are set

### 404 Errors on Refresh
Add this to your `public/_redirects` file for Netlify:
```
/*    /index.html   200
```

For other platforms, configure SPA routing in their settings.

## 📞 Need Help?

If you encounter issues:
1. Check the build logs
2. Ensure all files are committed to Git
3. Verify your repository is public (if using free hosting)
4. Check the hosting platform's documentation

Your luxury blog CMS should now be live and accessible to the world! 🚀