# Deployment Guide - GitHub Pages

This guide explains how to deploy the Capoeira Ginga no Canavial website to GitHub Pages.

## 🚀 Automatic Deployment Setup

The project is configured for automatic deployment to GitHub Pages using GitHub Actions. Here's how it works:

### Repository Setup

1. **Repository URL**: `https://github.com/sierisimo/capoeira-ginga-no-canavial`
2. **Live Site**: `https://sierisimo.github.io/capoeira-ginga-no-canavial/`

### Deployment Workflow

The deployment happens automatically when you:
- Push changes to the `main` branch
- Manually trigger the workflow from GitHub Actions tab

### GitHub Actions Workflow

The workflow (`.github/workflows/deploy.yml`) does the following:

1. **Triggers**: On push to main branch or manual dispatch
2. **Build**: Creates a clean deployment directory with only necessary files
3. **Deploy**: Uploads the site to GitHub Pages

#### Files Included in Deployment:
- `index.html` - Main website file
- `assets/` - All CSS, JavaScript, and images
- `.nojekyll` - Prevents Jekyll processing

#### Files Excluded from Deployment:
- `node_modules/` - Development dependencies
- `docs/` - Documentation files
- `package.json` - Node.js configuration
- `.gitignore` - Git configuration
- `README.md` - Project documentation

## 📋 Setup Instructions

### 1. Repository Setup

1. Create a new repository on GitHub:
   ```
   Repository name: capoeira-ginga-no-canavial
   Owner: sierisimo
   ```

2. Initialize and push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Capoeira academy website"
   git branch -M main
   git remote add origin https://github.com/sierisimo/capoeira-ginga-no-canavial.git
   git push -u origin main
   ```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under **Source**, select **GitHub Actions**
4. The workflow will automatically deploy on the next push

### 3. First Deployment

Once you push to the main branch:

1. Go to the **Actions** tab in your repository
2. Watch the "Deploy to GitHub Pages" workflow run
3. Once complete, your site will be live at:
   ```
   https://sierisimo.github.io/capoeira-ginga-no-canavial/
   ```

## 🔧 Configuration Files

### `.github/workflows/deploy.yml`
- GitHub Actions workflow for automatic deployment
- Builds and deploys on every push to main
- Uses official GitHub Pages actions

### `.nojekyll`
- Empty file that prevents GitHub from processing the site with Jekyll
- Ensures our assets load correctly

### `package.json`
- Updated with correct repository URLs
- Homepage points to GitHub Pages URL

## 🐛 Troubleshooting

### Common Issues

1. **Site not loading**: 
   - Check that GitHub Pages is enabled in repository settings
   - Verify the workflow completed successfully in Actions tab

2. **Assets not loading**:
   - Ensure `.nojekyll` file exists
   - Check that asset paths are relative (start with `assets/`)

3. **Workflow failures**:
   - Check the Actions tab for error messages
   - Ensure repository has proper permissions for GitHub Pages

### Manual Deployment

If automatic deployment fails, you can deploy manually:

```bash
# Create deployment directory
mkdir -p _site
cp index.html _site/
cp -r assets/ _site/
cp .nojekyll _site/

# Deploy using GitHub CLI (if installed)
gh workflow run deploy.yml
```

## 📈 Monitoring

### Checking Deployment Status

1. **Actions Tab**: See workflow runs and logs
2. **Settings → Pages**: Check deployment status
3. **Commits**: Green checkmarks indicate successful deployments

### Analytics (Optional)

To add Google Analytics:

1. Create a Google Analytics account
2. Add the tracking code to `index.html` in the `<head>` section
3. Push changes to trigger redeployment

## 🔄 Updating the Site

To update the website:

1. Make changes to your local files
2. Commit and push to main branch:
   ```bash
   git add .
   git commit -m "Update: description of changes"
   git push origin main
   ```
3. GitHub Actions will automatically redeploy
4. Changes will be live in 1-2 minutes

## 🌐 Custom Domain (Optional)

To use a custom domain:

1. Add a `CNAME` file to the repository root with your domain
2. Configure DNS records with your domain provider
3. Enable custom domain in GitHub Pages settings

---

**Live Site**: [https://sierisimo.github.io/capoeira-ginga-no-canavial/](https://sierisimo.github.io/capoeira-ginga-no-canavial/)

*¡Axé! 🥋* 