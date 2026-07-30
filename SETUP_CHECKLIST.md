# Setup checklist — abinesh65/abinesh65

Do these in order. Full detail in the companion Setup Guide PDF you already have.

## 1. Create the profile repo
- [ ] Go to github.com/new, name it exactly `abinesh65` (must match your username)
- [ ] Public, add a README
- [ ] Upload `dark.svg`, `light.svg`, `README.md`, and the `.github/workflows/snake.yml` from this bundle to the repo root (drag-and-drop preserves the `.github/workflows/` path)

## 2. Banner
- [ ] Already wired into README.md via `<picture>` — nothing else to do once the SVGs are uploaded
- [ ] Test: switch GitHub theme (avatar → Settings → Appearance) and reload your profile page

## 3. Stats cards (self-hosted)
- [ ] github.com/settings/tokens → Tokens (classic) → Generate new (classic) → scope `repo` → No expiration → copy the token immediately (never paste it anywhere public)
- [ ] Fork github.com/anuraghazra/github-readme-stats
- [ ] vercel.com → Sign up with GitHub → Hobby (free) → Add New Project → import your fork
- [ ] Environment variable: `PAT_1` = your token → Deploy
- [ ] Copy your instance URL (`your-instance.vercel.app`)
- [ ] In README.md, replace every `YOUR-INSTANCE` with your real Vercel URL

## 4. Contribution snake
- [ ] Repo Settings (the repo's tab, not your account) → Actions → General → Workflow permissions → **Read and write permissions** → Save
- [ ] `snake.yml` is already in the bundle at `.github/workflows/snake.yml`
- [ ] After upload, check the Actions tab — it should go green in ~1 minute and create an `output` branch
- [ ] The snake `<picture>` block in README.md is already wired — it just needs that `output` branch to exist first

## 5. Trophies & Featured Projects (new)
- [ ] Upload `projects-dark.svg` and `projects-light.svg` to the repo root — README.md is already wired to use them
- [ ] Trophy bar needs no setup — it's a live badge, just make sure your GitHub profile isn't private

## 6. Badges
- [ ] Already in README.md — LinkedIn, Portfolio, Email
- [ ] LinkedIn uses brand blue (#0A66C2) — this is required, shields.io silently drops the logo on any other color

## Notes
- Banner file sizes: dark.svg ~450KB, light.svg ~745KB (light mode has far more ink since it dots the whole photo, not just the segmented subject — normal for this style)
- If a change "didn't show up," it's almost always CDN caching — open the raw file URL with `?v=999` appended and search for your edit before assuming something's broken
- Scheduled Actions pause after ~60 days of repo inactivity — push or click "Enable workflow" to wake it back up
