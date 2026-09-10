# firstboss-legal

The privacy policy and terms of use for the **FirstBoss** iOS app, served over GitHub Pages at
<https://ashesashes.github.io/firstboss-legal/>.

Both pages are linked from inside the app (Settings → Legal), and the privacy URL is the one filed
in App Store Connect. **A dead link here is an App Store rejection**, so don't rename directories
or delete the trailing-slash paths `/privacy/` and `/terms/`.

## Editing

Don't edit the HTML by hand. The source of truth is the markdown in the app repo under
`projects/legal/specs/`. To publish a change:

```
python3 projects/legal/build.py ~/firstboss-legal
cd ~/firstboss-legal && git add -A && git commit && git push
```

`.nojekyll` disables the Jekyll build, so pushes go live in about a minute with no build step that
can fail.

## Moving to a custom domain

Setting a custom domain on this repo makes GitHub 301-redirect the `github.io` URLs to it, so URLs
already shipped inside a released binary keep working. See the running log in the app repo at
`projects/legal/decisions/running-log.md`.
