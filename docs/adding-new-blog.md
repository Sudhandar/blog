# Adding a New Blog Post (Internal Guide)

## Quick Steps

1. Create new blog file in `docs/blog/`:
   ```bash
   touch docs/blog/your-blog-title.md
   ```

2. Add frontmatter:
   ```markdown
   ---
   title: Your Blog Title
   date: YYYY-MM-DD
   tags:
     - tag1
     - tag2
   ---
   ```

3. Add images to `docs/images/` and reference in markdown:
   ```markdown
   ![Alt text](../images/your-image.png)
   ```

4. Update `mkdocs.yml` navigation:
   ```yaml
   nav:
     - Blog:
         - Category:
             - "Your Blog Title": blog/your-blog-title.md
   ```

5. Update `docs/blog.md` list:
   ```markdown
   ## Category
   - [Your Blog Title](blog/your-blog-title.md) - Brief Description
   ```

6. Test locally:
   ```bash
   mkdocs serve
   ```

7. Deploy:
   ```bash
   git add .
   git commit -m "Add new blog post: Your Blog Title"
   git push origin main
   mkdocs gh-deploy --force
   ```

## Notes
- Use kebab-case for filenames
- Keep image sizes optimized
- Test locally before deploying
- Check GitHub Actions for deployment status 