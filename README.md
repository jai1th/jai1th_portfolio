# Jaivanth Melanaturu — Portfolio

Personal portfolio site. `index.html` (self-contained) + `projects/` case-study pages + `style.css`. No build step; fonts via Google Fonts CDN.

## Structure

```
index.html                     — main page
style.css                      — shared styles for project pages
projects/
  vlm-robotics.html            — Research Assistant · VLM + UR5E
  kart-perception.html         — Autonomous go-kart · perception lead
  video-detection.html         — M.S. thesis case study
  daps.html                    — Parking-space detection
  feral-animal.html            — Edge AI · Jetson Nano
  voxel51.html                 — Hackathon 1st place
  miq-forecasting.html         — Industry internship · MiQ
```

Each project page follows a recruiter-scan structure: overview box (role / goal / key outcome) up top, quantified metric tiles, then problem → approach → results → skills.

## Deploy to GitHub Pages

**Option A — user site (recommended, cleanest URL → `jai1th.github.io`)**

1. Create a new public repo named exactly **`jai1th.github.io`**.
2. Add the whole folder contents (`index.html`, `style.css`, `projects/`, plus `resume.pdf` + `headshot.jpg` once you have them) to the repo root.
3. Push. GitHub Pages auto-builds. Live in ~1 min at **https://jai1th.github.io**.

```bash
git init
git add .
git commit -m "portfolio"
git branch -M main
git remote add origin https://github.com/jai1th/jai1th.github.io.git
git push -u origin main
```

**Option B — project site (URL → `jai1th.github.io/portfolio`)**

1. Push these files to any repo (e.g. `portfolio`).
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → `main` / `root` → Save.

## Before you go live — swap the placeholders

The pages have placeholder blocks (dashed boxes labeled in monospace):

| Placeholder | Where | Replace with |
|---|---|---|
| ~~`headshot.jpg`~~ | index hero | ✅ done — `assets/headshot.jpg` |
| `results_chart.png` | index thesis + video-detection page | ✅ done — EER + FPR/FNR charts |
| ~~`real / ai-gen / detect` frames~~ | index thesis | replaced by real EER chart |
| ~~`ur5e_setup.jpg`~~ | vlm-robotics page | ✅ done — camera rig + detection + JSONL |
| ~~`corridor_overlay.png`~~ | kart-perception page | ✅ done — `assets/kart-segmentation.png` |
| ~~`daps_masks.png`~~ | daps page | ✅ done — two real detection frames |
| `night_detection.jpg` | feral-animal page | IR detection frame |
| `demo_screenshot.png` | voxel51 page | app screenshot |
| `forecast_vs_actual.png` | miq page | forecast chart |
| `résumé.pdf` button | index hero | drop `resume.pdf` in repo root — already linked |

Swap any `.ph` block for `<img src="..." alt="...">`. Everything else (links, email `mjaivanth@outlook.com`, metrics) is live and accurate.

**Pages without imagery** (feral-animal, voxel51, miq) intentionally have no figure — their results sections are full-width text. Add an `<img>` there later if you get photos.

## Custom domain (optional)

Add a `CNAME` file containing your domain (e.g. `jaivanth.dev`), then point your DNS at GitHub Pages per their docs.
