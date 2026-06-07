# GLK Legal Website

Static website for GLK Legal migration and recruitment services.

## Local Preview

Open `index.html` in a browser, or serve the folder with any simple static server.

Example with Python:

```powershell
python -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

## Pages

- `index.html` - home page
- `migration.html` - migration services
- `recruitment.html` - recruitment services
- `styles.css` - site styling
- `script.js` - navigation, forms, and page interactions
- `Files/` - downloadable documents
- `Logos/` - logo assets
- `migration Images/` - migration page images
- `Recruitment Images/` - recruitment page images

## GitHub Pages Setup

This repository includes a GitHub Actions workflow at `.github/workflows/pages.yml`.

1. Push the repository to GitHub.
2. In GitHub, open the repository settings.
3. Go to `Pages`.
4. Under `Build and deployment`, set `Source` to `GitHub Actions`.
5. Push to the `main` branch.
6. Wait for the `Deploy static site to GitHub Pages` action to finish.

Before the custom domain is connected, the site will be published at:

```text
https://FNIT-Guy.github.io/GLK/
```

The custom domain for this site is:

```text
https://glkservices.com.au/
```

## Custom Domain

This repository includes a `CNAME` file for:

```text
glkservices.com.au
```

In GitHub, add `glkservices.com.au` in `Settings > Pages > Custom domain`.

In GoDaddy DNS, use these records:

```text
Type: A
Name: @
Value: 185.199.108.153

Type: A
Name: @
Value: 185.199.109.153

Type: A
Name: @
Value: 185.199.110.153

Type: A
Name: @
Value: 185.199.111.153

Type: CNAME
Name: www
Value: FNIT-Guy.github.io
```

After DNS has propagated and GitHub shows the domain as valid, enable `Enforce HTTPS`.

## Notes

- The site is plain HTML, CSS, and JavaScript, so there is no build step.
- `.nojekyll` is included so GitHub Pages serves the repository files directly.
- Keep file and folder names unchanged unless you also update every matching link in the HTML, CSS, and JavaScript.
