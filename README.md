# personal-site

Static hello-world page.

## Local preview

```
open index.html
```

## Deploy (GitHub Pages)

1. Create a new repo on GitHub (e.g. `your-domain.com`).
2. From this directory:
   ```
   git init
   git add .
   git commit -m "init"
   git branch -M main
   git remote add origin git@github.com:<your-user>/<repo>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source: `main` / `/ (root)`**. Wait ~1 min.
4. Site will be live at `https://<your-user>.github.io/<repo>/`.

## Point your Namecheap domain at it

1. On GitHub: **Settings → Pages → Custom domain →** enter your domain (e.g. `arjun.com`). Save.
2. On Namecheap: **Domain List → Manage → Advanced DNS**. Delete defaults. Add:

   | Type  | Host | Value                  |
   | ----- | ---- | ---------------------- |
   | A     | @    | 185.199.108.153        |
   | A     | @    | 185.199.109.153        |
   | A     | @    | 185.199.110.153        |
   | A     | @    | 185.199.111.153        |
   | CNAME | www  | `<your-user>.github.io.` |

3. Wait 10–60 min for DNS to propagate, then on GitHub Pages tick **Enforce HTTPS**.
