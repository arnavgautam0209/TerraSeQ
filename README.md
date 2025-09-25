<div align="center">

# 🌊 TerraSeQ  
### AI-powered eDNA Biodiversity Analysis & Visualization

⚡ *Discover hidden biodiversity from environmental DNA with machine learning and interactive visualizations.*

![React](https://img.shields.io/badge/Frontend-React%20%2B%20Vite-blue?logo=react)
![TypeScript](https://img.shields.io/badge/Language-TypeScript-3178C6?logo=typescript)
![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?logo=fastapi)
![Hackathon](https://img.shields.io/badge/Project-Hackathon-success)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## ✨ Overview
**TerraSeQ** is an **end-to-end bioinformatics pipeline and dashboard** that processes environmental DNA (eDNA) samples to uncover marine biodiversity.  

🔬 From raw reads → to cleaned sequences → to embeddings → clustering → taxonomic classification → ecological insights — all visualized in a modern **React + Vite + TypeScript dashboard**, optionally powered by a **FastAPI backend**.

---

## 🚀 Features
- 🔬 **Preprocessing** – Trim adapters, filter low-quality reads, generate QC metrics  
- 🧬 **Sequence Embedding** – k-mer counts or transformer-based (DNA-BERT) embeddings  
- 🌀 **Clustering & Novelty Detection** – Find species-level groups and unknown taxa  
- 🐠 **Taxonomic Classification** – Hybrid alignment + ML classification with confidence scores  
- 📊 **Abundance & Diversity Metrics** – Shannon, Simpson, Chao1 indices  
- 🌱 **Functional Annotation** – Predict ecological roles (producers, predators, decomposers)  
- 🌍 **Depth/Spatial Profiles** – Explore biodiversity across depths or sample locations  
- 🎨 **Interactive Dashboard** – Real-time pipeline progress and visualizations  

---

## 🏗️ System Architecture

```mermaid
flowchart LR
    User[User Browser] -->|Upload DNA file| React[React + Vite Dashboard]
    React -->|API call| FastAPI[FastAPI Backend]
    FastAPI -->|Run ML Pipeline| ML[DNA-BERT + Clustering + Classifier]
    ML --> Results[JSON Results]
    FastAPI --> React
    React -->|Visualize| Charts[Interactive Visuals]
