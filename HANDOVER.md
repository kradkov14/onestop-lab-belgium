# Taking over the site after OneSTOP ends

Hosting, the SSL certificate and Pages CMS are free. The only possible cost is your own domain (about €10–15 a year), and only if the `onestop-project.eu` subdomain is no longer available.

## 1. Get a GitHub account

Create a free GitHub account or organisation for your institution, e.g. `belgium-living-lab`. An organisation is better: several people can manage it, and it does not depend on one person.

## 2. Receive the repository

The OneSTOP team transfers this repository to you (**Settings → General → Transfer ownership**). You will get an e-mail from GitHub to accept it. The website keeps its full history, images and settings.

## 3. Reconnect Pages CMS

1. Go to https://app.pagescms.org and sign in with GitHub.
2. Install the Pages CMS GitHub App for your account or organisation and give it access to this repository.
3. Open the repository in Pages CMS and invite your editors by e-mail under **Collaborators**. Invitations from the OneSTOP period do not carry over.

## 4. Check GitHub Pages

In the repository, open **Settings → Pages** and confirm *Source: Deploy from a branch, main, / (root)*.

## 5. Domain

**If `onestop-project.eu` is still maintained:** ask whoever manages its DNS to change the CNAME record of your subdomain (e.g. `belgium.onestop-project.eu`) from `onestop-living-labs.github.io` to `<your-account>.github.io`. Nothing else changes.

**If it is not:**

1. Buy a domain, e.g. `belgium-livinglab.eu`.
2. At your registrar, add a CNAME record for `www` pointing to `<your-account>.github.io`. For the bare domain, add the four GitHub Pages A records listed in [GitHub's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).
3. In **Settings → Pages → Custom domain**, enter the new domain and save. Tick **Enforce HTTPS** once it becomes available.
4. Recommended: verify the domain under your account's **Settings → Pages** so nobody else can claim it.

## Without a domain

The site also works without a custom domain at `https://<your-account>.github.io/<repository>/`. Remove the domain under **Settings → Pages** and set `baseurl: "/<repository>"` in `_config.yml`.
