# GitHub Pages Setup Instructions

This repository is now configured for GitHub Pages deployment. Follow these steps to enable and access your documentation site.

## What Has Been Configured

The following files have been created to enable GitHub Pages:

1. **`docs/_config.yml`** - Jekyll configuration for the documentation site
2. **`.github/workflows/pages.yml`** - GitHub Actions workflow for automatic deployment
3. **Updated documentation pages** - Added Jekyll front matter for proper navigation

## Enabling GitHub Pages

### Step 1: Enable GitHub Pages in Repository Settings

1. Go to your repository on GitHub
2. Click on **Settings** (top navigation bar)
3. In the left sidebar, click on **Pages** (under "Code and automation")
4. Under **Build and deployment**:
   - **Source**: Select **GitHub Actions**
   - This will use the workflow file we created (`.github/workflows/pages.yml`)

### Step 2: Trigger the First Deployment

The GitHub Actions workflow is configured to run automatically on:
- Every push to the `main` branch
- Manual trigger from the Actions tab

To trigger the first deployment:

**Option A: Push to main branch**
```bash
git add .
git commit -m "Enable GitHub Pages"
git push origin main
```

**Option B: Manual trigger**
1. Go to the **Actions** tab in your repository
2. Click on "Deploy Jekyll site to Pages" workflow
3. Click **Run workflow** button
4. Select the `main` branch and click **Run workflow**

### Step 3: Monitor Deployment

1. Go to the **Actions** tab in your repository
2. You should see a workflow run in progress
3. Wait for the workflow to complete (usually takes 1-2 minutes)
4. Once complete, you'll see a green checkmark ✓

### Step 4: Access Your Site

After successful deployment, your documentation will be available at:

```
https://[your-username].github.io/[repository-name]/
```

For example, if your GitHub username is `AgentToolkit` and repository is `agent-lifecycle-toolkit`:
```
https://agenttoolkit.github.io/agent-lifecycle-toolkit/
```

You can also find the exact URL in:
- Repository Settings → Pages (will show the published URL)
- The Actions workflow run (in the deployment step output)

## Site Structure

Your GitHub Pages site includes:

- **Home Page** (`/`) - Main landing page from `docs/index.md`
- **Kaizen Documentation** (`/kaizen.html`) - Detailed Kaizen documentation from `docs/kaizen.md`
- **Assets** - All images and logos from `docs/assets/`

## Navigation

The site includes automatic navigation between pages:
- Home (nav_order: 1)
- Kaizen (nav_order: 2)

## Customization

### Changing the Theme

To use a different Jekyll theme, edit `docs/_config.yml`:

```yaml
theme: minima  # Change to: jekyll-theme-cayman, jekyll-theme-slate, etc.
```

Supported GitHub Pages themes:
- `minima` (default, clean and simple)
- `jekyll-theme-cayman`
- `jekyll-theme-slate`
- `jekyll-theme-minimal`
- `jekyll-theme-architect`
- `jekyll-theme-time-machine`

### Adding New Pages

1. Create a new `.md` file in the `docs/` directory
2. Add Jekyll front matter at the top:
   ```yaml
   ---
   layout: default
   title: Your Page Title
   nav_order: 3
   ---
   ```
3. Write your content in Markdown
4. Commit and push - the page will be automatically deployed

### Updating Site Information

Edit `docs/_config.yml` to change:
- `title`: Site title
- `description`: Site description
- `baseurl`: If your site is in a subdirectory
- `url`: Your site's URL

## Troubleshooting

### Deployment Failed

1. Check the Actions tab for error messages
2. Ensure the workflow file is in `.github/workflows/pages.yml`
3. Verify that GitHub Pages is set to use "GitHub Actions" as the source

### Site Not Updating

1. Check that your changes are pushed to the `main` branch
2. Wait for the GitHub Actions workflow to complete
3. Clear your browser cache (Ctrl+Shift+R or Cmd+Shift+R)
4. GitHub Pages can take a few minutes to update

### 404 Errors

1. Ensure all internal links use relative paths (e.g., `kaizen.md` not `/kaizen.md`)
2. Check that image paths are correct (e.g., `assets/logo.png`)
3. Verify file names match exactly (case-sensitive)

### Images Not Loading

1. Ensure images are in the `docs/assets/` directory
2. Use relative paths: `assets/image.png` (not `/assets/image.png`)
3. Check that image files are committed to the repository

## Maintenance

### Automatic Updates

The site will automatically rebuild and deploy whenever you:
- Push changes to the `main` branch
- Merge a pull request to `main`

### Manual Rebuild

To manually trigger a rebuild:
1. Go to Actions tab
2. Select "Deploy Jekyll site to Pages"
3. Click "Run workflow"

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [Markdown Guide](https://www.markdownguide.org/)
- [Jekyll Themes](https://pages.github.com/themes/)

## Support

If you encounter issues:
1. Check the [GitHub Pages status](https://www.githubstatus.com/)
2. Review the Actions workflow logs for detailed error messages
3. Consult the [GitHub Pages troubleshooting guide](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)