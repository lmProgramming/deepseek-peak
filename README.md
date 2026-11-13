# DeepSeek Peak

A tiny, dependency-free DeepSeek API peak/off-peak pricing tracker.

## GitHub Pages deployment

This repository is prepared for GitHub Pages using GitHub Actions.

1. Push these files to the `main` branch of `lmProgramming/deepseek-peak`.
2. Open **Settings → Pages** in the repository.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Open the **Actions** tab and wait for the `Deploy GitHub Pages` workflow to finish.
5. The site should be available at:

   https://lmprogramming.github.io/deepseek-peak/

GitHub may take several minutes to publish the first deployment.

## Local preview

Open `index.html` directly in a browser. No build step, package manager, server, or API key is required.

## Schedule

The tracker uses the schedule published in the [official DeepSeek pricing documentation](https://api-docs.deepseek.com/quick_start/pricing/):

- Peak: 01:00–04:00 UTC and 06:00–10:00 UTC, Monday through Friday.
- Off-peak: all other times, including weekends and Chinese public holidays.
- Off-peak prices are half of peak prices.

Chinese public holidays are not hard-coded because the dates change each year. The `CHINESE_PUBLIC_HOLIDAYS` set in `index.html` can be updated with `YYYY-MM-DD` dates when confirmed against the official calendar. Until updated, the tracker applies the weekday/hour schedule but does not automatically detect public holidays.

## SEO

The site includes:
- A descriptive title and meta description.
- Canonical URL for the GitHub Pages project site.
- Open Graph and Twitter metadata with a social preview image.
- `robots.txt` and `sitemap.xml`.
- WebApplication structured data.
- Semantic headings and explanatory, crawlable page content.
- A custom 404 page and favicon.

After deployment, verify the URL in [Google Search Console](https://search.google.com/search-console) and submit `/sitemap.xml`. Indexing and ranking are controlled by search engines and are not guaranteed.

## Important

This is an independent utility and is not affiliated with DeepSeek. Always verify current rates and schedule details against the official pricing documentation.
