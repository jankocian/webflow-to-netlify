# Project Dorian

Dorian is a static site generator that converts a website into a static site by scraping any content found from the origin. Postprocessing is done to perform optimizations on the downloaded content.

# The fastest way to get the site up and running

https://app.netlify.com/start/deploy?repository=https%3A%2F%2Fgithub.com%2Fjankocian%2Fwebflow-to-netlify

# Documentation on how to set up Netlify and Webflow

https://smarterlabs.notion.site/CryoLayer-Documentation-acbce2c61d464deeb16ffc3b865009d3

# Excluding pages from the sitemap

In Webflow, add this custom attribute to the "body" tag of the page you want to exclude from the sitemap:

Name: `sitemap`
Value: `no`

## Local usage

Make sure you have 2 environment variables set:

- `URL`: The destination URL
- `WEBFLOW_URL`: The original source URL to be scraped

To do this, you can create a `.env` file with the contents of `.env.template`. and fill in the variables.

Then run:

```bash
yarn build
```

It should output the files to the `public` folder in the project root. You can test the site out locally by running:

```bash
yarn serve
```

# Getting updates from the upstream repo

```bash
git pull upstream master && git push origin master
```
