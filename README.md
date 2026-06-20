# Hey there! I'm Xhinzu 👋

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Outfit&size=24&duration=3000&pause=1000&color=F3F4F6&center=true&vCenter=true&width=600&lines=Game+Dev+%7C+C%2B%2B+Enthusiast;Digital+Content+Creator;Hardware+%26+DIY+Geek;Valorant+Ascendant+1" alt="Typing SVG" />
</div>

---

### 💫 About Me

I am a Computer Science student at **Rajagiri Higher Secondary School** and a digital content creator under the handle **Xhinzu**. I love bridging the gap between software development, hardware tinkering, and gaming. 

Whether I'm writing C++ code for my next indie game, repurposing old electronics, or flashing animations for an energy monitoring app, I'm always building something new.

---

### 🛠️ Tech Stack & Toolkit

<div align="center">

| Category | Technologies |
| :--- | :--- |
| **Languages** | ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) |
| **Frameworks & Libraries** | ![Raylib](https://img.shields.io/badge/Raylib-E11936?style=for-the-badge&logo=raylib&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white) |
| **Hardware & IoT** | ![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=Arduino&logoColor=white) ![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-C51A4A?style=for-the-badge&logo=Raspberry-Pi&logoColor=white) |
| **Tools** | ![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) |

</div>

---

### 🎮 Current Projects

#### 🌌 **Midnight Shift**
*An indie stealth-horror game developed in C++ using Raylib.*
* **Status:** In active development 🛠️
* **Tech:** C++, Raylib
* **Focus:** Custom rendering pipelines, game loop optimization, and atmospheric retro graphics.

#### ⚡ **WattEveR**
*A sleek energy monitoring application with rich, dynamic animations.*
* **Status:** Finished animations & visual elements 🌟
* **Focus:** Interactive UI components, clean vector rendering, and smooth state transitions.

---

### 🖥️ Hardware & Battlestation

I’m a PC hardware enthusiast who loves DIY electronics and hardware repurposing. 

```ini
[Desktop Specs]
CPU       = AMD Ryzen 7 5700X (8 Cores, 16 Threads)
GPU       = NVIDIA GeForce RTX 4060
Memory    = 32GB DDR4 @ 3200MHz
Storage   = 1TB NVMe M.2 SSD + 2TB HDD
```

* **DIY Hobbies:** Reclaiming old screens, customizing peripherals, and building micro-controller gadgets.

---

### 🎯 Gaming Profile

When I am not coding or editing, you can find me on Valorant.

* **Rank:** **Ascendant 1** 💎
* **Main Agent:** Jett 🌪️
* **Playstyle:** Aggressive entry-fragging, space creation, and fast-paced utility usage.

---

### 🐍 GitHub Contribution Snake Game

Below is the automated contribution snake. It eats my contributions and turns them into a retro game screen!

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Xhinzu/Xhinzu/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Xhinzu/Xhinzu/output/github-contribution-grid-snake.svg">
  <img alt="GitHub Contribution Snake" src="https://raw.githubusercontent.com/Xhinzu/Xhinzu/output/github-contribution-grid-snake.svg">
</picture>

*(See instructions below to set this up for your own GitHub profile repository)*

---

### 🌐 Connect with Me

If you'd like to collaborate on a project, talk about PC hardware, or play some Valorant, feel free to reach out!

<p align="left">
  <a href="https://github.com/Xhinzu" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="https://youtube.com/@Xhinzuu" target="_blank">
    <img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="YouTube" />
  </a>
  <a href="mailto:contact@xhinzuu.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</p>

---

## ⚙️ How to Enable the Snake Game Contribution Graph

To make the contribution snake work automatically on your profile, follow these simple steps:

1. Create a public repository named exactly matching your GitHub username (e.g. `Xhinzu/Xhinzu`).
2. Inside that repository, create a directory structure: `.github/workflows/`
3. Create a file named `generate-snake.yml` inside that folder and paste the following content:

```yaml
name: Generate Snake

on:
  # run automatically every 24 hours
  schedule:
    - cron: "0 */24 * * *" 
  
  # allows to manually run the job at any time
  workflow_dispatch:
  
  # run on every push on the main branch
  push:
    branches:
    - main

jobs:
  generate:
    permissions: 
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      # generates a snake game from a github user (<github_user_name>) contributions graph, output a svg animation at <svg_out_path>
      - name: generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
      # push the content of <build_dir> to a branch
      # the content will be available at https://raw.githubusercontent.com/<github_user>/<repository>/<target_branch>/<file> , or as github page
      - name: push github-contribution-grid-snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

4. Commit and push this file. The workflow will run automatically, create a new branch named `output`, and push the animated SVG files there.
5. In your README.md, make sure the `img src` URLs match your username (replace `Xhinzu` with your actual username if different).
