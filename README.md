<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/header-light.svg">
  <img alt="Igor Kotlarz — foundation models × satellite data × earth observation" src="./assets/header-dark.svg" width="100%">
</picture>

<p align="center">
  <a href="https://www.linkedin.com/in/igorkotlarz"><img src="https://img.shields.io/badge/LinkedIn-igorkotlarz-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Focus-Earth_Observation_×_ML-2dd4bf?style=for-the-badge&logo=satellite&logoColor=white" alt="Focus">
  <img src="https://img.shields.io/badge/Based_in-Silesia,_PL-f0a35e?style=for-the-badge" alt="Location">
</p>

```text
$ whoami
igor — CS engineering student @ Silesian University of Technology (Politechnika Śląska)
       I teach models trained on one sensor to see through another.

$ cat mission.log
[ NOW  ] final semester · engineering thesis: foundation models compressed for on-board satellite hardware
[ NOW  ] FieldEye — drone-borne crop anomaly detection (RPi + FPGA + camera)
[ NEXT ] thesis defense · 02/2027
[ NEXT ] MSc in ML / computer vision / Earth observation
[ ALWAYS ] hackathons — as many as the calendar physically allows
```

## 🛰️ Current mission

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/mission-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/mission-light.svg">
  <img alt="Pipeline: foundation model → compression → INT8 model → Vitis AI → KP Labs Leopard" src="./assets/mission-dark.svg" width="100%">
</picture>

**Foundation Models in Orbit: Quantization, Pruning and Knowledge Distillation for FPGA-Based Space Hardware** *(working title)*

Geospatial foundation models like **TerraMind** and **Prithvi-EO-2.0** are trained on the ground with hundreds of millions of parameters. Satellites have watts and an FPGA. My thesis compresses both models and runs them on the **KP Labs Leopard**, a space-grade computer built on a Zynq UltraScale+ with a Vitis AI DPU, for flood segmentation on Sen1Floods11:

| Method | Idea |
|---|---|
| **Post-training quantization** | convert the trained model to INT8 with a small calibration set |
| **Quantization-aware training** | fine-tune with simulated INT8 so the model adapts to it |
| **Pruning** | remove the weights, channels and heads that contribute least |
| **Knowledge distillation** | train a small student to reproduce the large teacher |

Each variant is measured for water IoU, size, latency, memory and power on the same Leopard unit. Target: IEEE IGARSS 2027.

[→ igorkotlarz1/fm-4-eo-thesis](https://github.com/igorkotlarz1/fm-4-eo-thesis)

## 🚀 Flight log

<table>
<tr>
<td width="50%" valign="top">

### 🌾 FieldEye
**Crop anomaly detection from drone flights.** A custom payload with a camera, Raspberry Pi, sensors and an FPGA for on-board image processing. Team PBL project at university.

`Python` `Computer Vision` `Raspberry Pi` `FPGA`

[→ Kodies-Dev/Fieldeye](https://github.com/Kodies-Dev/Fieldeye)

</td>
<td width="50%" valign="top">

### 🛰️ HYPERVIEW Challenge
**Soil chemistry from 150 spectral bands.** P, K, Mg and pH estimated from hyperspectral field patches (ESA Φ-lab challenge). The pipeline uses mask-aware smoothing, spectral derivatives, per-target feature selection and leak-free repeated CV.

`Python` `scikit-learn` `XGBoost` `Remote Sensing`

[→ igorkotlarz1/io-hyperview-challenge](https://github.com/igorkotlarz1/io-hyperview-challenge)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### ☀️ SolarSight
**Solar PV production forecasting, hackathon-built** at ETHSilesia 2026 (Tauron AI Challenge). I built the Flask backend, the weather-API orchestration and a *what-if* simulation endpoint.

`Python` `Flask` `Forecasting` `REST`

[→ Kodies-Dev/Solar-Sight](https://github.com/Kodies-Dev/Solar-Sight)

</td>
<td width="50%" valign="top">

### ✋ Gesture LED Control
**Lights that follow your hand.** A webcam and MediaPipe track 21 hand landmarks, a gesture state machine turns pinches and raised fingers into brightness and RGB colour, and MQTT carries the result to an ESP32 driving the LEDs.

`Computer Vision` `MediaPipe` `MQTT` `ESP32`

[→ igorkotlarz1/gesture-led-control](https://github.com/igorkotlarz1/gesture-led-control)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📦 Olist Review Risk
**Spotting 1–3★ reviews before they are written.** 91k Brazilian e-commerce orders run through a PostgreSQL feature view, then an XGBoost + Optuna model with a Streamlit SHAP dashboard. A leakage audit cut a flattering F1 of 0.46 down to an honest score, then time-aware seller-reputation features won part of it back.

`Python` `PostgreSQL` `XGBoost` `SHAP`

[→ igorkotlarz1/olist-bad-review-risk](https://github.com/igorkotlarz1/olist-bad-review-risk)

</td>
<td width="50%" valign="top">

### 🐷 Skarbonka
**Local-first AI for settling household expenses.** Import a bank CSV, and rules, ML and a local LLM categorise the spending, then turn it into a settlement report. No transaction ever reaches a cloud AI.

`FastAPI` `PostgreSQL + pgvector` `Ollama` `React`

[→ igorkotlarz1/skarbonka](https://github.com/igorkotlarz1/skarbonka)

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🚶 Walk Cycle EDA
**Does cognitive load erase gait differences?** Motion-capture data from autistic and control walkers, analysed with non-parametric tests and effect sizes. Under a Stroop task the differences mostly disappear.

`R` `tidyverse` `Mann–Whitney U` `Cohen's d`

[→ igorkotlarz1/Walk-cycle-EDA](https://github.com/igorkotlarz1/Walk-cycle-EDA)

</td>
<td width="50%" valign="top">

### ⚡ Sobel SIMD
**Edge detection in hand-written x64 assembly.** The Sobel operator written twice, as scalar C++ and as SSE assembly that computes 8 pixels per instruction, behind a C# app that benchmarks the two. The assembly runs about 4× faster than plain C++ and comes with a test harness that checks it pixel by pixel and verifies the Windows calling convention.

`x64 ASM` `SSE` `C++` `C#`

[→ igorkotlarz1/Sobel-edge-detection](https://github.com/igorkotlarz1/Sobel-edge-detection)

</td>
</tr>
</table>

## 🧰 Payload

<p>
  <img src="https://skillicons.dev/icons?i=py,pytorch,sklearn,c,cpp,java,spring,flask,postgres,docker,linux,raspberrypi,opengl,git&perline=14" alt="Tech stack">
</p>

<p>
  <img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white" alt="CUDA">
  <img src="https://img.shields.io/badge/MPI-parallel_computing-555?style=flat-square" alt="MPI">
  <img src="https://img.shields.io/badge/Neo4j-4581C3?style=flat-square&logo=neo4j&logoColor=white" alt="Neo4j">
  <img src="https://img.shields.io/badge/PostGIS-336791?style=flat-square&logo=postgresql&logoColor=white" alt="PostGIS">
  <img src="https://img.shields.io/badge/Sentinel--2-remote_sensing-2dd4bf?style=flat-square" alt="Sentinel-2">
  <img src="https://img.shields.io/badge/Hyperspectral-imaging-f0a35e?style=flat-square" alt="Hyperspectral imaging">
</p>

**ML / EO:** foundation models, transfer learning, hyperspectral imaging, remote sensing · **Data:** ETL, data warehousing, SQL, graph and spatial databases · **Systems:** parallel computing (CUDA, MPI), systems programming in C/C++, computer graphics

📜 Corporate Readiness Certificate: *Data Science in Practice* (2025) · *Data & AI Fundamentals* (2026)

## 🏔️ Off-orbit

```text
climbing  ██████████  10 years on the rock, still falling off it
sailing   ██████▒▒▒▒  reading wind is just feature engineering
running   ████▒▒▒▒▒▒  half-marathon build, Feb 2027
guitar    ███████▒▒▒  metalhead, unapologetically
```

## 📫 Ground station

Up for **hackathon teams, research collaborations and Earth-observation side quests**. The fastest way to reach me is [LinkedIn](https://www.linkedin.com/in/igorkotlarz).

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/footer-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="./assets/footer-light.svg">
  <img alt="ground station signing off" src="./assets/footer-dark.svg" width="100%">
</picture>
