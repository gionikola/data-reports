# Daily Economic Data Report

`index.html` contains the report with all data visualizations.

`index.html` is produced by the `Render Report` GitHub Actions workflow specified in `update-report.yaml`, which gets triggered to knit the `index.Rmd` in the `main` branch every day at 8:00 AM UTC. 

The `main` branch is then merged with the `gh-pages` branch by the `Merge main branch to gh-pages` GitHub Actions workflow specified in `merge-main-to-pages.yaml`, which gets triggered every day at 12:00 PM UTC. 

After each push to the `gh-pages` branch, the `pages-build-deployment` GitHub Actions workflow then syncs the `gh-pages` branch with the website to update the https://giorginikolaishvili.com/data-reports webpage. 
GitHub Pages knows to produce the contents of the webpage using the `index.html` file by default. 
