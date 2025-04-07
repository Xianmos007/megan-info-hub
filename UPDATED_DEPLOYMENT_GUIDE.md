# Updated Deployment Guide for Megan's Information Hub

This guide provides two methods for deploying your website: Cloudflare Pages (recommended for static sites) and Cloudflare Workers.

## Method 1: Cloudflare Pages (Recommended for Static Sites)

### Option A: Deploy from Git Repository

1. Go to the [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Select "Pages" from the sidebar
3. Click "Create a project" → "Connect to Git"
4. Connect your GitHub account and select your repository
5. Configure your build settings:
   - Project name: "megan-info-hub" (or your preferred name)
   - Production branch: "main" or "master"
   - Build command: Leave empty (not needed for static HTML)
   - Build output directory: "." or "/" (root directory)
6. Click "Save and Deploy"

### Option B: Direct Upload (No Git Required)

1. Go to the [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. Select "Pages" from the sidebar
3. Click "Create a project" → "Direct upload"
4. Enter a project name (e.g., "megan-info-hub")
5. Drag and drop the folder containing all the HTML files
6. Click "Deploy site"

## Method 2: Cloudflare Workers

If you prefer to use Cloudflare Workers, follow these steps:

1. Make sure you have Node.js installed on your computer
2. Install Wrangler globally (if not already installed):
   ```
   npm install -g wrangler
   ```
3. Log in to your Cloudflare account:
   ```
   wrangler login
   ```
4. Navigate to your website directory (where the HTML files and wrangler.toml are located)
5. Deploy your site:
   ```
   wrangler deploy
   ```

The included wrangler.toml file is already configured to deploy your static site correctly.

## Troubleshooting

### Common Issues with Cloudflare Pages:

- **Build Failures**: For static HTML sites, leave the build command empty
- **404 Errors**: Make sure your index.html is in the root directory
- **CSS/JS Not Loading**: Check that all file paths are relative, not absolute

### Common Issues with Cloudflare Workers:

- **Missing Entry Point**: Make sure wrangler.toml is in the root directory of your project
- **Permission Errors**: Ensure you're logged in with `wrangler login`
- **Deployment Failures**: Check that your account has Workers enabled

For additional help, refer to the [Cloudflare Pages documentation](https://developers.cloudflare.com/pages/) or [Cloudflare Workers documentation](https://developers.cloudflare.com/workers/).
