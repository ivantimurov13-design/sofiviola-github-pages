# Sofiviola site

Static Sofiviola catalog at https://sofiviola.ru/.

`sofiviola-site` is the private source repository and Cloudflare Pages preview
(https://sofiviola.pages.dev/). `sofiviola-github-pages` is the public GitHub
Pages repository serving `sofiviola.ru`. Edit the site in `sofiviola-site`.

## Publish

1. Commit and push changes to `main` in `sofiviola-site`.
2. Keep a clean local checkout of `sofiviola-github-pages` next to this repo, or
   set `SOFIVIOLA_PUBLIC_REPO` to its path.
3. Run `bash scripts/publish.sh` from `sofiviola-site`.

The script checks that both checkouts match their remote `main`, copies
`index.html`, `assets/`, icons, and this README, then commits and pushes the
public repository if anything changed. The public repository's `CNAME` stays
there and is not copied from the source.

## Local preview

```bash
python3 -m http.server 4174 --bind 127.0.0.1
```

Open http://127.0.0.1:4174/.
