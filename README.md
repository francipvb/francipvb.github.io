# Francisco Del Roio's personal website

A Jekyll site for a professional résumé, projects, contact information, and a future blog. The first version is in English. It is designed to work without JavaScript or third-party services.

## Run locally

Install Ruby 3.3 and Bundler, then run:

```sh
bundle install
bundle exec jekyll serve
```

Open the local address printed by Jekyll. To build without starting a server, run `bundle exec jekyll build --strict_front_matter`. The generated site is in `_site/`; edit the source files, not that directory.

## Edit the content

- Update the introduction in `index.md` and the page metadata in each file's front matter.
- Update `resume.md` with your profile, experience, skills, and education. Markdown headings, lists, and links become accessible HTML. Do not publish information you do not want to make public.
- Add or update project descriptions and repository links in `projects.md`.
- Update your email, GitHub, and LinkedIn links in `contact.md` if they change.
- If you want to offer a PDF résumé, add a PDF you have chosen to publish under `assets/` and add a descriptive link to it in `resume.md`, for example:

  ```liquid
  [Download my résumé (PDF)]({{ '/assets/resume.pdf' | relative_url }})
  ```

- `blog.md` is a welcome page. Jekyll supports posts in `_posts/` named `YYYY-MM-DD-title.md`; before publishing posts, update the blog page to list them and check the post layout and navigation.

## Languages

The site currently has English content only. Shared navigation labels are in `_data/en.yml`, and pages use the `lang` front-matter value to select the corresponding data file. To add Spanish later, create `_data/es.yml` with translated labels and Spanish page URLs, add translated pages under `/es/` with `lang: es`, and add an accessible language switcher linking equivalent pages. Translate page content and metadata as well as navigation; keep the existing English URLs stable.

## Deploy to GitHub Pages

In the repository's **Settings → Pages**, select **GitHub Actions** as the build and deployment source. The workflow in `.github/workflows/pages.yml` builds pull requests targeting `master` and builds and deploys pushes to `master`; it can also be started manually. The first successful deployment and repository settings must be checked on GitHub.

The configured production URL is `https://francipvb.github.io` with an empty base path. Update `url` and, if needed, `baseurl` in `_config.yml` if the hosting address changes. Internal links use Jekyll's URL filters so that a nonempty base path can be supported.

## Accessibility checks

After content or layout changes, build the site and check that all pages have clear headings and meaningful link text. Navigate using only the keyboard: verify the skip link, visible focus, navigation, and contact link. Check the layout at narrow and wide viewport sizes in Chromium and Firefox, including zoom and reduced-motion preferences.

With NVDA on Windows, check the page title and language, landmarks, heading and link lists, keyboard navigation, skip link, and reading order in Chromium and Firefox. Automated checks and a successful build do not replace this manual review.

## License

See [LICENSE](LICENSE).
