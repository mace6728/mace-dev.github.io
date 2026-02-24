+++
draft = false
date = 2026-02-23T18:45:00+08:00
title = "Projects"
slug = "projects"
+++

Here's a collection of my technical projects spanning hardware acceleration, networking systems, and deep learning applications.

---

## Networking & Systems

### DPU-Accelerated Scitags Marking System

High-energy physics experiments like the Large Hadron Collider generate massive amounts of data that need to be transferred across global research networks. Traditional approaches using CPU-based software marking struggle to keep up with modern 400Gbps networks, creating a significant bottleneck.

I developed a hardware-accelerated solution using **NVIDIA BlueField-3 DPU** to offload packet marking entirely from the host CPU. By leveraging **DOCA Flow**, the system performs IPv6 Flow Label modifications directly in hardware at line rate.

**Key Results:**
- Achieved full **400Gbps line-rate processing** (compared to ~300Gbps with traditional eBPF)
- Reduced host CPU overhead to essentially zero
- Implemented dynamic flow rule management and real-time traffic visualization

**Tech Stack:** `C`, `DOCA`, `DPDK`, `eBPF/XDP`, `Prometheus`, `Grafana`
    
---

## Artificial Intelligence & ML

### Tainan-Walker: AI-Powered Pedestrian Route Ranking

Walking in tropical cities can be uncomfortable due to heat and poor infrastructure. I built an AI system that recommends walking routes based not just on distance, but on pedestrian comfort factors like shade coverage, sidewalk quality, and street conditions.

The system processes extensive GIS data and uses a **Multi-Layer Perceptron** to rank potential routes. I integrated **SHAP (SHapley Additive exPlanations)** to make the model's decisions interpretable, showing exactly how factors like tree coverage influence each recommendation.

**Key Features:**
- Handles complex multi-modal urban data (satellite imagery, street networks, environmental sensors)
- Provides explainable rankings with feature importance visualization
- Designed for real-world deployment in urban planning contexts

**Tech Stack:** `Python`, `PyTorch`, `SHAP`, `Pandas`, `GIS Tools`

---

## Ongoing Research

I'm currently exploring:

- **Hardware-Accelerated Security**: Building DPU-based firewalls and intrusion detection systems that operate at network line rate
- **Programmable Networks**: Investigating how P4-programmable switches can work alongside DPUs for smarter data center architectures
- **Scientific Computing Infrastructure**: Contributing to open-source tools for high-performance research networks

---

> **Open to collaborating on networking, systems performance, or ML infrastructure projects. Feel free to reach out!**