# OneSTOP Living Lab website

A static website for one OneSTOP Living Lab, hosted free on GitHub Pages and edited with [Pages CMS](https://app.pagescms.org).

## Editing the site

1. Open the invitation e-mail from Pages CMS and sign in with your e-mail address (no GitHub account needed).
2. Pick the section to edit in the left menu:
   - **Home page**: heading, header image, introduction, main text, key facts, highlight cards, photo gallery.
   - **News**: add, edit or delete news items.
   - **Extra pages**: add pages such as "Events" or "Partners". Tick *Show in menu* to list them in the top menu.
   - **Lab details**: lab name, institutions, logo, contact e-mail, "Get involved" text.
3. Click **Save**. The live site updates in about a minute.

Photos: upload JPG or PNG files, ideally 1600–2400 px wide and under 1 MB each.

You can change texts, images, news and extra pages. The design, colours, menu layout and footer are part of the OneSTOP template and cannot be changed from Pages CMS.

## Files

| Path | What it is | Editable in Pages CMS |
| --- | --- | --- |
| `index.md` | Home page content | yes |
| `_posts/` | News items | yes |
| `_subpages/` | Extra pages | yes |
| `_data/lab.yml` | Lab name, logo, contact | yes |
| `images/` | Uploaded images | yes |
| `.pages.yml` | Pages CMS form definition | no |
| `_layouts/`, `_includes/`, `assets/` | Template and design | no |
| `_config.yml`, `CNAME` | Technical settings and domain | no |

## Preview locally (developers)

```bash
docker run --rm -p 4000:4000 -e PAGES_REPO_NWO=owner/repo -v "$PWD:/srv/site" -w /srv/site ruby:3.3 \
  bash -c 'bundle install && bundle exec jekyll serve --host 0.0.0.0'
```

Then open http://localhost:4000.

See [HANDOVER.md](HANDOVER.md) for taking over hosting after the OneSTOP project ends.
