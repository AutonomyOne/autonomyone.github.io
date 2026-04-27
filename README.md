# autonomyOne GitHub Pages starter

This is a minimal static landing page for the `autonomyOne` GitHub organisation.

## Repository

Create this repository in the `autonomyOne` organisation:

```text
autonomyone.github.io
```

The repository name must be lowercase because GitHub Pages requires uppercase letters in user or organisation names to be lowercased.

## Files

- `index.html` - homepage
- `styles.css` - styling
- `404.html` - simple not-found page
- `CNAME` - sets the custom domain to `autonomyone.ai`
- `.nojekyll` - tells GitHub Pages to serve files directly without Jekyll processing

## Launch commands

From inside this folder:

```bash
git init
git add .
git commit -m "Launch interim autonomyOne website"
git branch -M main
git remote add origin https://github.com/autonomyOne/autonomyone.github.io.git
git push -u origin main
```

Then in GitHub, go to the repository's Settings -> Pages and set:

```text
Source: Deploy from a branch
Branch: main
Folder: /root
Custom domain: autonomyone.ai
Enforce HTTPS: enabled, once GitHub allows it
```

## DNS records for GoDaddy

For the root domain `autonomyone.ai`, add A records for `@` pointing to GitHub Pages:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Optional IPv6 AAAA records for `@`:

```text
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

For `www.autonomyone.ai`, add a CNAME record:

```text
Name: www
Value: autonomyone.github.io
```

Keep any email-related MX, SPF, DKIM, and DMARC records intact.
