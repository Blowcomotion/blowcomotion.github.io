# blowcomotion.github.io

Static GitHub Pages site that redirects visitors from the apex domain `blowcomotion.org` to the www subdomain `https://www.blowcomotion.org`.

## Purpose

This repository serves as a redirect solution for the apex/naked domain. When users visit `https://blowcomotion.org`, they are automatically redirected to `https://www.blowcomotion.org` where the main website is hosted.

## How it works

The `index.html` file implements a multi-layered redirect approach:

1. **Meta refresh**: `<meta http-equiv="refresh" content="0; url=https://www.blowcomotion.org">`
2. **JavaScript redirect**: Fallback redirect using `window.location.href`
3. **Manual link**: User-clickable link in case automatic redirects fail

## Setup

1. This repository is configured as a GitHub Pages site
2. The apex domain `blowcomotion.org` is configured to point to GitHub Pages
3. GitHub Pages serves the `index.html` file when users visit the apex domain
4. Users are immediately redirected to `https://www.blowcomotion.org`

## SEO Considerations

- The page includes `<link rel="canonical" href="https://www.blowcomotion.org">` to indicate the preferred URL
- `<meta name="robots" content="noindex, nofollow">` prevents search engines from indexing the redirect page
- The redirect is fast (0-second delay) to minimize SEO impact

## Domain Configuration

To use this redirect:

1. Configure your apex domain DNS to point to GitHub Pages:

   ```dns
   A    185.199.108.153
   A    185.199.109.153
   A    185.199.110.153
   A    185.199.111.153
   ```

2. Enable GitHub Pages on this repository (Settings → Pages)

3. Configure your custom domain in GitHub Pages settings to `blowcomotion.org`

## Testing

You can test the redirect by visiting `https://blowcomotion.org` - it should automatically redirect to `https://www.blowcomotion.org`.
