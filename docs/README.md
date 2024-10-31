Welcome to the docs project

## Internal note

If you're reading this on the Cloudflare pages site, this is how we deploy:

1. Commit to /main
2. This triggers sync to github via pipeline
3. CloudFlare Pages monitors github and will automatically deploy to the site

**Please don't nest further than 1 level deep - i.e. no subfolders within /Admin-Guide, etc. Going deeper will break relative image links on MkDocs**

We use MkDocs to power the site. See `requirements.txt`. 

- `mkdocs.yml` is the configuration file for MkDocs
- `docs/` is where the markdown files live
- `docs/.pages` is used to tell MkDocs which pages to include in the navigation
- `mkdocs serve` will run the site locally
- `mkdocs build` will build the site to the `site/` directory

When building locally, make sure to use Python 3.7 w/ a venv