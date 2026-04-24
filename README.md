# GitHub Profile Visual Upgrades
## Every widget below is free. Replace `yourusername` with your actual GitHub username everywhere.

---

## 1. Animated Typing Header
**What it looks like:** A headline that types itself out on your profile. Looks alive, not static.
**How to add:** Paste this at the very top of your README.

```markdown
[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=6C63FF&width=600&lines=Hey%2C+I'm+Sameer+%F0%9F%91%8B;Freelance+ML+%2F+AI+Engineer;Python+%C2%B7+LLMs+%C2%B7+RAG+%C2%B7+Deep+Learning;Building+AI+that+works+in+the+real+world)](https://git.io/typing-svg)
```

**Customise it:** Go to https://readme-typing-svg.demolab.com and change the `lines=` part to whatever you want typed out. Each line is separated by `;`.

---

## 2. GitHub Stats Card
**What it looks like:** A card showing your total stars, commits, PRs, issues, and contribution streak.
**How to add:**

```markdown
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="48%" />
</p>
```

**Themes you can swap in** (replace `tokyonight`):
`dark` `radical` `merko` `gruvbox` `tokyonight` `onedark` `cobalt` `synthwave` `highcontrast` `dracula`

Preview all themes: https://github.com/anuraghazra/github-readme-stats/blob/master/themes/README.md

---

## 3. Top Languages Card
**What it looks like:** A card breaking down your most-used languages by percentage.
**How to add:** Put this right next to your stats card so they sit side by side.

```markdown
<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=yourusername&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" width="48%" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=yourusername&layout=compact&theme=tokyonight&hide_border=true" width="48%" />
</p>
```

---

## 4. GitHub Streak Stats
**What it looks like:** Shows your current streak, longest streak, and total contributions. One of the most impressive widgets — clients love seeing consistency.
**How to add:**

```markdown
<p align="center">
  <img src="https://streak-stats.demolab.com?user=yourusername&theme=tokyonight&hide_border=true" width="60%" />
</p>
```

Customise themes here: https://github.com/DenverCoder1/github-readme-streak-stats/blob/main/docs/themes.md

---

## 5. Contribution Graph (Activity Graph)
**What it looks like:** A full-width graph of all your commits over the past year — the green squares grid, but bigger and styled.
**How to add:**

```markdown
<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=yourusername&theme=tokyo-night&hide_border=true" width="100%" />
</p>
```

Available themes: https://github.com/Ashutosh00710/github-readme-activity-graph/blob/main/THEMES.md

---

## 6. GitHub Trophies
**What it looks like:** A row of trophies for milestones — stars earned, commits, followers, PRs, etc.
**How to add:**

```markdown
<p align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=yourusername&theme=tokyonight&no-frame=true&row=1&column=7" width="100%" />
</p>
```

---

## 7. Skill Badges (shields.io)
**What it looks like:** Coloured pill-shaped badges for each of your skills. Clean and scannable.
**How to add:** Copy and paste the ones you use:

```markdown
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
```

Make your own badge for anything: https://shields.io/badges

---

## 8. Profile View Counter
**What it looks like:** A small badge showing how many times your profile has been viewed. Adds social proof.
**How to add:** Put this near the top of your README.

```markdown
![Profile Views](https://komarev.com/ghpvc/?username=yourusername&color=6C63FF&style=for-the-badge&label=PROFILE+VIEWS)
```

---

## 9. Snake Contribution Animation
**What it looks like:** An animated snake eating your contribution squares. Sounds gimmicky — actually looks incredible.
**This one needs 2 steps:**

**Step 1:** In your profile repo, create this file: `.github/workflows/snake.yml` with this content:

```yaml
name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**Step 2:** After the action runs (go to Actions tab and trigger it manually first time), add this to your README:

```markdown
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/yourusername/yourusername/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/yourusername/yourusername/output/github-snake.svg" />
    <img src="https://raw.githubusercontent.com/yourusername/yourusername/output/github-snake.svg" alt="snake animation" />
  </picture>
</p>
```

---

## 10. Project Showcase Cards
**What it looks like:** Pinned repo-style cards embedded directly in the README, not just the pinned section below.
**How to add:** One card per project. Replace `repo-name` with the actual repo name.

```markdown
<p align="center">
  <a href="https://github.com/yourusername/cognitive-decline-detection">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=yourusername&repo=cognitive-decline-detection&theme=tokyonight&hide_border=true" />
  </a>
</p>
```

---

## How to put it all together — final order

Paste sections in this order for maximum visual impact:

```
1. Typing animation header
2. Profile view counter badge
3. One-liner bio (plain text)
4. Skill badges section
5. Stats card + Top languages side by side
6. Streak stats
7. Activity graph
8. Trophies
9. Project cards
10. Snake animation (at the very bottom — it's the bow on the package)
11. Contact section
```

---

## Quick links to all tools used
| Tool | Link |
|------|------|
| Typing SVG | https://readme-typing-svg.demolab.com |
| GitHub Stats | https://github.com/anuraghazra/github-readme-stats |
| Streak Stats | https://streak-stats.demolab.com |
| Activity Graph | https://github.com/Ashutosh00710/github-readme-activity-graph |
| Trophies | https://github.com/ryo-ma/github-profile-trophy |
| Badges | https://shields.io |
| Profile Views | https://komarev.com/ghpvc |
| Snake | https://github.com/Platane/snk |
