# opsguy.io

Personal blog and portfolio site for Brandon Cantrell.

## Stack

- [Hugo](https://gohugo.io/) (static site generator)
- [Congo](https://github.com/jpanther/congo) theme
- Hosted on AWS (S3 + CloudFront)

## Local Development

Requires Hugo extended edition and Go.

```bash
cd site
hugo server -D
```

Site runs at http://localhost:1313

## Deployment

Push to `main` triggers GitHub Actions workflow:
1. Builds site with Hugo
2. Syncs to S3
3. Invalidates CloudFront cache

PRs to `main` run the build for validation but don't deploy.

## Creating Content

```bash
# New blog post
cd site && hugo new posts/my-post-title/index.md

# New page
cd site && hugo new pagename/index.md
```
