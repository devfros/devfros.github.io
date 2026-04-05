# devfros.github.io

Personal site and blog, built with [Jekyll](https://jekyllrb.com/) and the [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme, deployed with [GitHub Actions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#publishing-with-a-custom-github-actions-workflow).

Live site: [https://devfros.github.io](https://devfros.github.io)

## Local preview

Requirements: Ruby (the workflow uses Ruby 3.3) and Bundler.

```sh
bundle install
bundle exec jekyll serve
```

Then open the URL Jekyll prints (usually `http://127.0.0.1:4000`).

## GitHub Pages

1. In the repository **Settings → Pages**, set **Build and deployment → Source** to **GitHub Actions** (not “Deploy from a branch”).
2. Push to `main` (or `master`); the workflow in `.github/workflows/pages-deploy.yml` builds the site and publishes it.

## Giscus comments

Comments use [Giscus](https://giscus.app/) (GitHub Discussions under the hood).

1. Enable **Discussions** on this repository (**Settings → General → Features**).
2. Open [giscus.app](https://giscus.app), sign in with GitHub, and choose repository `devfros/devfros.github.io`.
3. Copy **repository ID** and **category ID** into `_config.yml` under `comments.giscus` as `repo_id` and `category_id` (category is often “General”).
4. Commit and push; the comment box appears on posts after the next deploy.

Until `repo_id` and `category_id` are set, the comment widget may not load correctly.

## License

See `LICENSE` if present; theme licensing follows [jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy).
