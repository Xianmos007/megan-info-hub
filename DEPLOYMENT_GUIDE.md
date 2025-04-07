# Deployment Guide for Megan's Information Hub

This guide will walk you through deploying your website to Cloudflare Pages.

## Prerequisites

- A Cloudflare account (free tier is sufficient)
- A GitHub account (to store your website files)

## Step 1: Prepare Your Files for Deployment

The website files are already prepared and ready for deployment. They are simple HTML, CSS, and JavaScript files that will work perfectly with Cloudflare Pages.

## Step 2: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in to your account
2. Click the "+" icon in the top-right corner and select "New repository"
3. Name your repository (e.g., "megan-info-hub")
4. Make sure the repository is set to "Public"
5. Click "Create repository"

## Step 3: Upload Your Website Files to GitHub

1. Clone the repository to your local machine:
   ```
   git clone https://github.com/yourusername/megan-info-hub.git
   ```
2. Copy all the website files into the cloned repository folder
3. Add, commit, and push the files to GitHub:
   ```
   cd megan-info-hub
   git add .
   git commit -m "Initial website files"
   git push origin main
   ```

## Step 4: Deploy to Cloudflare Pages

1. Go to [Cloudflare Pages](https://pages.cloudflare.com/) and sign in
2. Click "Create a project"
3. Select "Connect to Git"
4. Connect your GitHub account if you haven't already
5. Select the repository you created in Step 2
6. Configure your build settings:
   - Project name: "megan-info-hub" (or your preferred name)
   - Production branch: "main"
   - Build command: Leave empty (not needed for static HTML)
   - Build output directory: Leave as "/" or set to "." (root directory)
7. Click "Save and Deploy"

## Step 5: Wait for Deployment

Cloudflare will now build and deploy your website. This usually takes less than a minute for simple static sites.

## Step 6: Access Your Website

Once deployment is complete, Cloudflare will provide you with a URL to access your website (typically something like `https://megan-info-hub.pages.dev`).

## Step 7: Set Up Custom Domain (Optional)

If you have a custom domain you'd like to use:

1. In your Cloudflare Pages project, go to "Custom domains"
2. Click "Set up a custom domain"
3. Enter your domain name and follow the instructions
4. Update your domain's DNS settings to point to Cloudflare Pages

## Updating Your Website

To update your website in the future:

1. Make changes to your local files
2. Commit and push the changes to GitHub:
   ```
   git add .
   git commit -m "Update website content"
   git push origin main
   ```
3. Cloudflare Pages will automatically detect the changes and redeploy your website

## Troubleshooting

If you encounter any issues during deployment:

- Make sure all file paths in your HTML files are relative (not absolute)
- Check that all files are properly uploaded to GitHub
- Verify that your Cloudflare Pages build settings are correct
- Review the build logs in Cloudflare Pages for any specific errors

For additional help, refer to the [Cloudflare Pages documentation](https://developers.cloudflare.com/pages/).
