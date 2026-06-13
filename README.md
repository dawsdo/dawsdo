<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,40:1B2330,100:415A77&height=200&section=header&text=Dawson%20Do&fontColor=F4F1DE&fontSize=56&fontAlignY=38&desc=CS%20%E2%80%A2%20University%20of%20Alabama%20at%20Birmingham&descAlignY=62&descSize=16&descAlign=50" width="100%" alt="header banner" />

<br>

<a href="https://github.com/dawsdo">
  <img src="https://readme-typing-svg.demolab.com/?lines=Software+engineer+in+training;Computer+vision+%26+full-stack;Building+honest%2C+defensible+work&font=JetBrains+Mono&color=F4F1DE&size=18&center=true&vCenter=true&width=520&height=42&pause=1200" alt="typing animation" />
</a>

<br>

<a href="https://dawsdo-portfolio.vercel.app">
  <img src="https://img.shields.io/badge/Portfolio-415A77?style=for-the-badge&logo=vercel&logoColor=F4F1DE" alt="portfolio" />
</a>
<a href="https://www.linkedin.com/in/dsdo/">
  <img src="https://img.shields.io/badge/LinkedIn-415A77?style=for-the-badge&logo=linkedin&logoColor=F4F1DE" alt="linkedin" />
</a>
<a href="mailto:dsdoapps@gmail.com">
  <img src="https://img.shields.io/badge/Email-415A77?style=for-the-badge&logo=gmail&logoColor=F4F1DE" alt="email" />
</a>

<br><br>

</div>

<br>

## About

CS undergraduate at the University of Alabama at Birmingham, focused on full-stack engineering and computer vision. I build real things end to end and try to keep my work honest — every claim defensible in a ten-minute interview.

What I care about: code that works under pressure, decisions I can explain, and projects where the engineering tradeoffs are the interesting part.

Currently looking for **Summer 2026 internships.**

<br>

## Currently

```yaml
learning:
  - "Real-time CV pipelines and WebSocket backpressure"
  - "Production-grade frontend systems (Next.js, Vite, Framer Motion)"
  - "ML deployment patterns on constrained hardware"

building:
  - "Collision CV Web — real-time YOLO detection over web"
  - "Personal portfolio — honest engineering case studies"

exploring:
  - "Design systems and visual product engineering"
  - "Computer vision for safety and perception"

open_to:
  - "Summer 2026 internships (SWE, ML, full-stack)"
  - "Conversations about ML systems and product engineering"
```

<br>

## Tech

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=python,typescript,javascript,java&theme=dark" alt="languages" />

<sub>Python · TypeScript · JavaScript · Java</sub>

<br><br>

**Frontend**

<img src="https://skillicons.dev/icons?i=react,nextjs,vite,tailwind,html,css&theme=dark" alt="frontend" />

<sub>React · Next.js · Vite · Tailwind · HTML · CSS</sub>

<br><br>

**Backend & ML**

<img src="https://skillicons.dev/icons?i=flask,nodejs,pytorch,opencv&theme=dark" alt="backend and ml" />

<sub>Flask · Node.js · PyTorch · OpenCV</sub>

<br><br>

**Tools**

<img src="https://skillicons.dev/icons?i=git,github,vscode,powershell,vercel&theme=dark" alt="tools" />

<sub>Git · GitHub · VS Code · PowerShell · Vercel</sub>

</div>

<br>

## Featured project

<details open>
<summary><b>Collision CV Web</b> — real-time computer vision over the browser</summary>

<br>

A full-stack web application that runs YOLOv8 object detection on uploaded images, video, and live webcam feeds in real time. Built deliberately to demonstrate honest engineering tradeoffs — every decision in this repo is one I can defend.

| | |
|---|---|
| **Stack** | Python · Flask · Flask-SocketIO · YOLOv8 (Ultralytics) · PyTorch · OpenCV · React · TypeScript · Vite · Framer Motion |
| **Detection** | Person, bicycle, car, motorcycle, bus, truck (COCO classes 0–7, conf ≥ 0.4) |
| **Throughput** | ~5 FPS sustained inference on CPU · 3 FPS sampling for video uploads |
| **Live mode** | WebSocket streaming with skip-if-busy backpressure to keep latency bounded |
| **Repository** | [github.com/dawsdo/collision-cv-web](https://github.com/dawsdo/collision-cv-web) |

**Engineering choices worth talking about:**

- Singleton model loading — the YOLO model is cached at module level so we avoid the 2–5 second load on every inference
- Frame backpressure — capture runs at 10 FPS but the backend processes ~5 FPS, so the frontend drops frames when the previous detection hasn't returned yet. End-to-end latency stays bounded at ~200ms instead of growing unbounded under load
- 3 FPS video sampling — chosen as a deliberate tradeoff between temporal coverage and processing time. 60 seconds of video processes in ~10 seconds
- SVG overlay with viewBox scaling — bounding boxes stay aligned with the underlying image at any display size
- Shared `BoundingBoxLayer` component — single source of truth for box rendering across image, video, and live modes

</details>

<br>

## GitHub

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=dawsdo&hide_border=true&background=0D1117&stroke=415A77&ring=415A77&fire=F4F1DE&currStreakLabel=F4F1DE&currStreakNum=F4F1DE&sideNums=F4F1DE&dates=cbd5e1&sideLabels=cbd5e1" alt="streak" />

<br><br>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=dawsdo&layout=compact&hide_border=true&bg_color=0D1117&title_color=F4F1DE&text_color=cbd5e1&langs_count=8" alt="top languages" />

</div>

<br>

## Approach

A few principles I try to actually practice:

- **Defensible over impressive.** I'd rather have one project I can walk through in detail than five I can't justify.
- **Name what you traded.** Every choice has a cost. Saying "I picked X because of Y, knowing I gave up Z" beats hand-waving.
- **Verify what you ship.** Read the diff before the push. Catch the bug in `git status`, not in production.
- **Use what the industry already solved.** Standard tools exist for a reason. Rolling your own is a luxury, not a default.

<br>

## Connect

<div align="center">

<a href="mailto:dsdoapps@gmail.com"><img src="https://img.shields.io/badge/Email-415A77?style=flat-square&logo=gmail&logoColor=F4F1DE" alt="email" /></a>
<a href="https://www.linkedin.com/in/dsdo/"><img src="https://img.shields.io/badge/LinkedIn-415A77?style=flat-square&logo=linkedin&logoColor=F4F1DE" alt="linkedin" /></a>
<a href="https://dawsdo-portfolio.vercel.app"><img src="https://img.shields.io/badge/Portfolio-415A77?style=flat-square&logo=vercel&logoColor=F4F1DE" alt="portfolio" /></a>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:415A77,60:1B2330,100:0D1117&height=120&section=footer" width="100%" alt="footer banner" />

</div>
