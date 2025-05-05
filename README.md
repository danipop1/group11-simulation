# simulation-template

This is a *bare-minimum* template to create a simulation site.

To get started with creating a site, simply:

1. click "[use this template]" to create a GitHub repository
   - note: don't **fork** the repository
3. go to Settings > Pages > Build and deployment > Source, and select GitHub Actions
   - note: you don't need to do any further configuration as they are already in place

After completing the creation of your new site on GitHub, update it as needed:

## Replace the content of the template pages

Update the following files to your own content:

- `index.md` (your new home page)
- `_config.yml` (meta info of your website)
- `_data` (containing map data and etc.)
- `_drafts` (unpublished pages)
- `assets` (put anything that is not text here)
- other `.md` files (GitHub will process each of them and generate a webpage)

Configuration files that you might not want to mess up with:

- `.devcontainer` (only useful if you'd like to develop locally on your computer)
- `.github` (containing the workflow for building the website)
- `.vscode` (containing predefined tasks if you want to develop locally; `Build` to build and `Serve` to run the website)
- `_includes` (containing JavaScript files for map; you may add others if needed)
- `_layouts` (containing the layouts; in particular, `event.html` includes code for [giscus](giscus))
- `.gitignore` (only useful if you'd like to develop locally)
- `Gemfile` (environment config for Ruby; only useful if you'd like to develop locally)
- `LICENSE` (by default, we are using Creative Commons)
- `README.md` (information for those who access your site repo on GitHub)

You may update or delete other `.md` files and/or folders as needed.

## Publishing your site on GitHub Pages

1.  If your created site is `YOUR-USERNAME/YOUR-SITE-NAME`, update `_config.yml` to:

    ```yaml
    title: YOUR TITLE
    description: YOUR DESCRIPTION
    footer_content: 'YOUR FOOTNOTE.'
    ```

2.  Push your updated `_config.yml` to your site on GitHub.

3.  In your newly created repo on GitHub:
    - go to the `Settings` tab -> `Pages` -> `Build and deployment`, then select `Source`: `GitHub Actions`.
    - if there were any failed Actions, go to the `Actions` tab and click on `Re-run jobs`.

## Supporting discussions

[giscus](https://giscus.app/) is a comment system powered by GitHub Discussions. You could use this feature for
facilitating communication among players, submitting reports, and/or collecting feedback. To enable it,
config your giscus app, and replace the JavaScript code in `_layouts/event.html`.
