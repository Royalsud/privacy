# Privacy policies

Public privacy policy pages for the Android apps published by **Sudip Mondal**, served free by
GitHub Pages. Google Play requires a public policy URL that needs no login — these are it.

**Live site:** https://royalsud.github.io/privacy/

| App | Package | Policy URL |
|---|---|---|
| Shadow Dungeon 3D | `com.sudip.shadowdungeon3d` | https://royalsud.github.io/privacy/shadow-dungeon-3d/ |

## Adding the next app

```bash
cp -r template my-next-app          # 1. copy the template folder
                                    # 2. edit my-next-app/index.html — replace every {{PLACEHOLDER}}
                                    # 3. add a matching <a class="card"> to index.html
git add -A && git commit -m "Add my-next-app policy" && git push
```

The page is live at `https://royalsud.github.io/privacy/my-next-app/` about a minute after the push.

If that app *does* use AdMob, Firebase or any other SDK, uncomment the “4b. Services used by this
app” block in the template and make sure Play Console → **Data safety** says the same thing. A
mismatch between the policy and the Data safety form is the usual reason Play rejects a release.

## Repo setup (already done, for reference)

- Repo must be **public** — GitHub Pages on a private repo requires a paid plan.
- Settings → Pages → Deploy from a branch → `main` / `/ (root)`.
- `.nojekyll` tells Pages to serve the files as they are, with no Jekyll build step.
- `style.css` is shared by every page; edit it once and all policies restyle.

Do **not** hand Google Play a `raw.githubusercontent.com` link instead — those are served as
plain text rather than a web page.
