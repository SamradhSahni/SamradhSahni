<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=6366F1&center=true&vCenter=true&multiline=true&width=700&height=100&lines=Hey+there%2C+I'm+Samradh+Sahni+%F0%9F%91%8B;Full-Stack+%26+AI+Engineer)](https://git.io/typing-svg)

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=180&section=header&text=Building%20the%20Future%2C%20One%20Commit%20at%20a%20Time&fontSize=28&fontColor=ffffff&animation=twinkling&fontAlignY=40" width="100%"/>

</div>

---

## 🧠 About Me

```typescript
const samradh: Developer = {
  name        : "Samradh Sahni",
  role        : "Full-Stack & AI Engineer",
  focus       : ["Backend Systems", "AI/ML Integration", "Automation"],
  languages   : ["TypeScript", "JavaScript", "Python", "Java"],
  stack       : {
    frontend  : ["React", "Next.js", "React Native", "TailwindCSS"],
    backend   : ["Node.js", "Express", "FastAPI", "Django", "Flask"],
    cloud     : ["AWS", "Firebase", "Vercel", "Render", "Netlify"],
    databases : ["PostgreSQL", "MongoDB", "Redis", "DynamoDB", "Elasticsearch"],
    ml        : ["PyTorch", "TensorFlow", "scikit-learn", "OpenCV", "CLIP", "mT5", "ViT"],
    devops    : ["Docker", "GitHub Actions", "Git"],
  },
  experience  : "Backend Engineer Intern @ Coding Blocks",
  currentlyBuilding : "AI-first products — from CLIP-based visual search to Hindi NLP advisory systems",
  contact     : "samradhsahni@gmail.com",
};
```

- 🔭 Building AI-powered full-stack products with ML microservices and deep learning pipelines
- 🌱 Deep-diving into **LLMs, vector embeddings, RAG, and Vision Transformers**
- 💼 Interned at **Coding Blocks** — built production REST APIs, JWT auth systems, and optimized MongoDB pipelines
- ⚡ Passionate about **clean architecture, backend performance, and automation**
- 💬 Ask me about **Node.js, React, Python, FastAPI, AWS, or anything AI/ML**
- 📫 Reach me at **samradhsahni@gmail.com**

---

## 🌐 Connect

<div align="left">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/samradhsahni/)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/u/Samradh/)
[![GitHub](https://img.shields.io/badge/GitHub-121011?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SamradhSahni)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:samradhsahni@gmail.com)

</div>

---

## 💼 Work Experience

<table>
<tr>
<td width="60px" align="center">
  <img src="https://img.shields.io/badge/CB-FF6B35?style=for-the-badge" alt="Coding Blocks"/>
</td>
<td>

### 🏢 Web Developer Intern — [Coding Blocks](https://codingblocks.com)
`Node.js` `Express.js` `MongoDB` `JWT` `REST API` `MVC`

- Engineered and shipped production-grade **RESTful APIs** following strict **MVC architecture**, ensuring clean separation of concerns and maintainable codebase across multiple service modules
- Implemented **JWT-based authentication** with **role-based access control (RBAC)** — securing protected routes and enforcing granular permission layers for different user roles
- Diagnosed and resolved **database performance bottlenecks** in MongoDB — applied selective indexing, query projection, and aggregation pipeline refactoring to significantly reduce response latency on high-traffic endpoints
- Collaborated in an **agile team environment**, participating in code reviews, sprint planning, and cross-functional API design discussions

</td>
</tr>
</table>

---

## 🚀 Featured Projects

### 🌿 KisanMitra AI — Hindi Agricultural Advisory Chatbot
> *Fine-tuned mT5 + RAG system trained on 2.7M Kisan Call Centre records for 500M Hindi-speaking farmers*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github)](https://github.com/SamradhSahni/KisanMitra_AI)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232a?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazon-aws&logoColor=white)

**What it does:** A production-grade Hindi agricultural advisory chatbot built on 2.7M query-answer pairs from India's Kisan Call Centre — serving crop disease, pest management, fertilizer, government scheme, and MSP price queries entirely in Hindi with sub-2-second responses.

**Key Engineering:**
- Solved a **fundamental data alignment problem**: the 2.7M KCC records had English queries and Hindi answers — unusable for Hindi NLP directly. Built a 7-phase pipeline: raw collection → 9-step cleaning → **MinHash LSH deduplication** (72.7% reduction to 525K unique records) → intent discovery → **IndicTrans2 translation** (100% Devanagari output) → instruction formatting → stratified split
- **Fine-tuned Google mT5-base (580M params) with QLoRA** — 4-bit NF4 quantization via bitsandbytes reducing memory from 2.2GB to ~600MB; only 6.7M of 580M params trained (1.15%). Hardware: NVIDIA RTX 4050 (6GB VRAM)
- **RAG pipeline:** 50K records indexed in **Elasticsearch 8.x** with hybrid BM25 + KNN retrieval, fused via **Reciprocal Rank Fusion (RRF)**. Embedding: `multilingual-e5-small` (384-dim). Retrieval latency: avg **62ms**
- **BLEU-4: 26.56** (+12.5 pts over best prompt-engineered Mistral-7B baseline); **ROUGE-1: 9.12** (+197% with RAG); **100% Hindi output, 0% language mismatch**
- **Backend:** FastAPI with `/chat`, `/msp`, `/feedback` endpoints; PostgreSQL for sessions/messages; Redis for MSP price caching (24h TTL)
- **Frontend:** React + TypeScript WhatsApp-style chat with Hindi voice input (Web Speech API, hi-IN locale), RAG source attribution panel, intent badges, and mobile-responsive layout
- **AWS deployment architecture:** SageMaker Async Inference (T4 GPU) → OpenSearch → RDS PostgreSQL → ElastiCache Redis → Lambda + Mangum → API Gateway → Amplify

| Metric | Zero-Shot | Prompt-Eng | **Fine-tuned + RAG** |
|--------|-----------|------------|----------------------|
| BLEU-4 | 14.06 | 15.68 | **26.56** |
| chrF | 21.52 | 23.66 | **29.77** |
| ROUGE-1 | 2.78 | 5.75 | **8.94** |
| Repetition | 54.0% | 47.5% | **0.0%** |

---

### 🌾 AgriSense — TRMS-ViT Crop Disease Classifier
> *State-of-the-art Vision Transformer hybrid for 38-class plant disease detection*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github)](https://github.com/SamradhSahni/AgriSense)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)

**What it does:** An automated crop disease detection system for 38 crop–disease classes (Apple, Tomato, Potato, Grape, Corn, and more) built on a custom hybrid deep learning architecture — **TRMS-ViT (Token-Refined Multi-Scale Vision Transformer)**.

**Key Engineering:**
- **Designed TRMS-ViT from scratch** — a novel hybrid that fuses a pretrained `vit_base_patch16_224` backbone (global feature understanding) with a custom CNN Multi-Scale Token Extractor (local lesion/texture detection), connected via a **Cross-Attention Refinement** block
- The cross-attention mechanism learns interactions between CNN tokens and ViT tokens, producing richer representations than either architecture alone
- **Classification Head:** LayerNorm → Dense → GELU → Dropout → Softmax over 38 classes
- **Training pipeline:** AdamW + CosineAnnealingLR + Label Smoothing + Gradient Clipping + Early Stopping; augmented dataset with RandomResizedCrop, Flip, Rotation, Brightness/Contrast, Translation
- **Dataset:** 70/15/15 train/val/test split across 38 classes from publicly available agricultural image sources
- **Deployed** as a **Streamlit web app** — upload a leaf image, get instant disease prediction with confidence score

---

### 🔍 Visual Product Search Platform
> *AI-powered e-commerce with multimodal search — find products by image or text*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github)](https://github.com/SamradhSahni/visual-product-search-platform)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232a?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)

**What it does:** End-to-end AI-powered e-commerce platform where users can search products by uploading an image or typing a query — powered by **CLIP embeddings** (OpenAI's Contrastive Language-Image Pretraining) that map both image and text into a shared semantic vector space.

**Key Engineering:**
- Built a **Python ML microservice** exposing CLIP-powered vector similarity endpoints, decoupled from the main Node.js backend via REST
- Implemented **image upload search** — user uploads any photo, system finds visually similar products using cosine similarity over CLIP embeddings
- Delivered **personalized recommendation engine** (collaborative + content-based) and trending product analytics
- Architected full **vendor/customer dual-role workflow** — product listings, inventory management, order flows, and admin dashboards
- **React frontend** with responsive UI; **MongoDB** for product catalog and user data; **Node.js/Express** for API orchestration

---
### ⚽ Football Player Tracking & Performance Analytics
> *End-to-end CV pipeline: raw match footage → broadcast-grade tactical intelligence*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github)](https://github.com/SamradhSahni/Football-Analysis-Using-YOLO)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

**What it does:** An open-source, GPU-accelerated football analysis system that ingests raw MP4 match footage and automatically produces per-player distance, speed, sprint counts, fatigue scores, team formations, possession stats, Voronoi pitch control diagrams, pass maps, offside line overlays, and a PDF match report — all through a 6-tab Streamlit dashboard.

**Key Engineering:**
- **Detection:** Custom **YOLOv8** trained on ~18GB SoccerNet MOT dataset — dual-model strategy: primary 4-class model (player/goalkeeper/referee/ball) + dedicated ball-only nano model at 1280×1280px with MixUp/CopyPaste augmentation. Achieved **mAP@50: 0.662**, Precision: 0.806
- **Tracking:** **ByteTrack** with 30-frame loss buffer (1.2s occlusion recovery), IoU Kalman filter matching, ghost track filter (MIN_TRACK_FRAMES=15) — maintains consistent IDs across 90+ minutes of footage
- **Coordinate Mapping:** **Perspective homography** (cv2.findHomography + RANSAC) maps pixel positions to a FIFA-standard 105m×68m pitch by parsing SoccerNet camera calibration JSONs (20+ semantic line correspondences). Recomputes every 300 frames to handle pans/zooms
- **Team Classification:** Unsupervised **K-Means on HSV jersey color histograms** with 20-frame sliding voting window — locks team assignment after 8 consistent votes, EMA centroid updates (α=0.04) adapt to lighting changes
- **Analytics engines:** EWMA-smoothed speed (physics-capped at 12 m/s), KDE heatmaps, Voronoi territory with Sutherland-Hodgman polygon clipping, pressing intensity scores, formation labeling via K-Means on player positions, pass/interception event detection
- **17 pytest test modules** covering every pipeline component; YAML-driven configuration; PDF reports via ReportLab

**Pipeline:**
```
Raw Video → YOLOv8 Detection → ByteTrack → Homography → K-Means Teams → 10+ Analytics Engines → Streamlit Dashboard + PDF Report
```

---

### 📈 MarketLens — AI Financial Analytics Platform
> *Full-stack ML platform for Nifty-50 stock analysis, LSTM forecasting & portfolio optimization*

[![Repo](https://img.shields.io/badge/GitHub-Repo-181717?style=flat-square&logo=github)](https://github.com/SamradhSahni/MarketLens)
![React](https://img.shields.io/badge/React-20232a?style=flat-square&logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)

**What it does:** A production-style AI financial intelligence platform analyzing 10+ years of Nifty-50 historical data — combining LSTM price forecasting, portfolio optimization, correlation network analysis, and sector analytics through an interactive full-stack dashboard.

**Key Engineering:**
- **Microservice architecture:** Node.js/Express handles auth, routing, and API orchestration; **Python FastAPI** runs the compute-heavy ML service (model inference, portfolio math, graph generation) — clean separation enables independent scaling
- **LSTM forecasting pipeline:** TensorFlow/Keras LSTM trained on time-series OHLCV data with MinMax scaling, sequence window generation, recursive multi-step forecasting, and inverse-transform for human-readable output
- **Portfolio optimization:** Modern Portfolio Theory — covariance matrix analysis, expected return estimation, Markowitz-style efficient frontier with multi-stock allocation recommendations and pie-chart diversification visualization
- **Correlation Network Analysis** using **NetworkX** + graph theory: constructs weighted correlation graphs between Nifty-50 stocks, computes Degree, Betweenness, Eigenvector Centrality, and PageRank — surfaces diversification opportunities and influential market nodes
- **Data engineering pipeline:** Missing value handling, normalization, rolling averages, volatility calculations, log-return generation, feature engineering, and LSTM tensor formatting for 10+ years of market data
- **Auth system:** Passport.js + session-based authentication with MongoDB session storage and protected routes
- **6 feature modules:** Nifty Index Dashboard (7 time-range filters), Individual Stock Analysis, LSTM Forecasting, Portfolio Optimizer, Correlation Network, Sector-Wise Analytics

---

## 🧩 LeetCode Stats

<div align="center">

[![LeetCode Stats](https://leetcard.jacoblin.cool/Samradh?theme=dark&font=Fira%20Code&ext=heatmap)](https://leetcode.com/u/Samradh/)

</div>

---

## 💻 Tech Stack

### 🖥 Languages
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)

### ⚛️ Frontend
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Next JS](https://img.shields.io/badge/Next-black?style=for-the-badge&logo=next.js&logoColor=white)
![React Native](https://img.shields.io/badge/react_native-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=for-the-badge&logo=Flutter&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-%23FE4B4B.svg?style=for-the-badge&logo=streamlit&logoColor=white)

### 🔧 Backend
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Django](https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)

### ☁️ Cloud & Deployment
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-%23039BE5.svg?style=for-the-badge&logo=firebase)
![Vercel](https://img.shields.io/badge/vercel-%23000000.svg?style=for-the-badge&logo=vercel&logoColor=white)
![Netlify](https://img.shields.io/badge/netlify-%23000000.svg?style=for-the-badge&logo=netlify&logoColor=#00C7B7)
![Render](https://img.shields.io/badge/Render-%46E3B7.svg?style=for-the-badge&logo=render&logoColor=white)

### 🗄 Databases
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![AmazonDynamoDB](https://img.shields.io/badge/Amazon%20DynamoDB-4053D6?style=for-the-badge&logo=Amazon%20DynamoDB&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/elasticsearch-%23037CC.svg?style=for-the-badge&logo=elasticsearch&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)

### 🤖 AI / ML
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)
![PyTorch](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=white)

### 🛠 DevOps & Tools
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitLab](https://img.shields.io/badge/gitlab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Figma](https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white)
![Power Bi](https://img.shields.io/badge/power_bi-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![NPM](https://img.shields.io/badge/NPM-%23CB3837.svg?style=for-the-badge&logo=npm&logoColor=white)

---

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.shion.dev/api?username=SamradhSahni&theme=tokyonight&hide_border=false&include_all_commits=false&count_private=false" height="170" />
<img src="https://github-readme-stats.shion.dev/api/top-langs/?username=SamradhSahni&theme=tokyonight&hide_border=false&include_all_commits=false&count_private=false&layout=compact" height="170" />

</div>

<div align="center">

[![GitHub Streak](https://streak-stats.demolab.com/?user=SamradhSahni&theme=tokyonight&hide_border=false)](https://git.io/streak-stats)

</div>

---

## 🏆 GitHub Trophies

<div align="center">

![](https://github-profile-trophy.vercel.app/?username=SamradhSahni&theme=tokyonight&no-frame=false&no-bg=false&margin-w=4)

</div>

---

## 📈 Contribution Graph

<div align="center">

[![Samradh's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=SamradhSahni&theme=tokyo-night&hide_border=true)](https://github.com/ashutosh00710/github-readme-activity-graph)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=120&section=footer&animation=twinkling" width="100%"/>

![Profile Views](https://komarev.com/ghpvc/?username=SamradhSahni&color=6366f1&style=for-the-badge&label=PROFILE+VIEWS)

**Thanks for stopping by! Let's build something amazing together. 🚀**

</div>
