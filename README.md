# Founders Table Static Site

This repository contains the static rebuild of the Founders Table website. The refresh aims to capture the clean, minimal aesthetic of world-class brands like Apple and Nike while keeping the build straightforward and maintenance-free.

## Project Structure

```
index.html          # Home page with hero and introduction
about.html          # About us page with mission and background
careers.html        # Careers page listing job opportunities
contact.html        # Contact page with form placeholder and Google Map
assets/
  css/
    tailwind.css    # Tailwind CSS import and space for custom styles
  img/              # Placeholder directory for images
README.md           # This file
```

## Setup

No build step is required. Each HTML file references Tailwind CSS from a CDN for styling. To preview the site locally, open `index.html` in any modern web browser.

## Git & Deployment

To deploy this site on Vercel:

1. **Initialize a Git repository and commit the files**

   ```sh
   git init
   git add .
   git commit -m "Initial commit – Founders Table static site"
   ```

2. **Push to GitHub**

   Create a new repository (for example, `founderstable-site`) in your GitHub account and push the local repository to it:

   ```sh
   git remote add origin git@github.com:<your-username>/founderstable-site.git
   git branch -M main
   git push -u origin main
   ```

3. **Deploy with Vercel**

   Sign in to [Vercel](https://vercel.com) with your GitHub account and import the repository. Choose the default settings; Vercel will automatically detect this as a static project and deploy it. Vercel also manages HTTPS certificates automatically, so the site will be served securely over SSL.

## DNS Setup

Once your project is live on Vercel, you can point your custom domain (for example, `founderstable.ai`) to it:

1. In your domain registrar’s DNS management, create a CNAME record pointing the subdomain (e.g. `www.founderstable.ai`) to your Vercel-assigned domain (e.g. `your-project-name.vercel.app`). To route the root domain, follow Vercel’s instructions for configuring an apex domain.
2. In your Vercel dashboard, add the custom domain to the project under the **Domains** section.
3. Allow time for DNS propagation. Vercel will automatically provision an SSL certificate for your domain.

## Notes

* The contact form in `contact.html` is a non-functional placeholder; it does not submit data. You can connect it to a back-end service or form handler when you’re ready.
* Replace placeholder text and add your own imagery under `assets/img/` as content becomes available. The design emphasises simplicity and whitespace; use high-quality, uncluttered images where appropriate.
