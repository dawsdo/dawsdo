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

<br>

## Currently

```yaml
learning:
  - "Real-time inference pipelines and WebSocket systems"
  - "ML deployment on constrained hardware"

building:
  - "Collision CV Web — real-time YOLO detection over web"
  - "Personal portfolio — honest engineering case studies"

exploring:
  - "Computer vision for safety and perception"
  - "Design systems and visual product engineering"
```

<br>

## Tech

| | |
|---|---|
| **Languages** | Python · TypeScript · Java · C++ · Go · SQL |
| **Frontend** | React · Next.js · Vite · Tailwind · Framer Motion |
| **Backend** | Flask · Node.js · Prisma · PostgreSQL · AWS |
| **ML / CV** | PyTorch · YOLOv8 · OpenCV · NumPy · Pandas |
| **Tools** | Git · GitHub Actions · Docker · Vercel · VS Code |

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

## Approach

A few principles I try to actually practice:

- **Defensible over impressive.** I'd rather have one project I can walk through in detail than five I can't justify.
- **Name what you traded.** Every choice has a cost. Saying "I picked X because of Y, knowing I gave up Z" beats hand-waving.
- **Verify what you ship.** Read the diff before the push. Catch the bug in `git status`, not in production.
- **Use what the industry already solved.** Standard tools exist for a reason. Rolling your own is a luxury, not a default.

<br>

<div align="center">

<sub><i>UAB Honors Program · CS w/ Math & Chemistry minors · 4.0 GPA · Open to research opportunities and internships</i></sub>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:415A77,60:1B2330,100:0D1117&height=120&section=footer" width="100%" alt="footer banner" />

</div>
