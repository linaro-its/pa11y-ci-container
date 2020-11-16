# pa11y-ci container

This container includes all of the tools required to carry out a CI-triggered accessibility analysis of a website.

Example command:

```bash
docker run --rm -it pa11y-ci pa11y-ci --sitemap https://www.linaro.org/sitemap.xml --sitemap-exclude ".+\.pdf" -j > site-report.json
docker run --rm -it -v./working-directory:/home/pptruser/working pa11y-ci pa11y-ci-reporter-html -s working/site-report.json -d working/site-directory
```
