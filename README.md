# 🧠 SpartanMetrics – Backend

### Computer Vision & AI Sports Evaluation Engine

## 🚀 Overview

SpartanMetrics Backend is a Python-based AI engine that analyzes sports training videos and extracts biomechanical metrics using computer vision and rule-based scoring.

It transforms raw video into structured performance insights.

---

## 🧠 Core Capabilities

### 🎥 Pose Detection

* MediaPipe Pose for landmark extraction
* Multi-player support
* Frame-level confidence filtering

### 📐 Biomechanical Metrics

Examples:

* Pad level (angle normalization)
* Drive forward progress
* Back curvature estimation
* Contact phase detection
* Throwing hip rotation timing

### 🧩 Skill Engine (YAML Driven)

Each skill is defined declaratively:

```yaml
skill: tackle
metrics:
  - pad_level
  - drive_forward_progress
rules:
  - if: pad_level < 35
    score: -10
```

This makes the system:

* Extensible
* Sport-agnostic
* Coach-customizable

---

## 🏗 Architecture

```
app/
 ├── api/
 │    └── routes/
 ├── services/
 │    ├── pose/
 │    ├── skills/
 │    ├── metrics/
 │    └── evaluation/
 ├── core/
 └── models/
```

---

## ⚙️ Tech Stack

* **Python 3.11**
* **FastAPI**
* **OpenCV**
* **MediaPipe**
* **NumPy**
* **YAML rule engine**
* **Docker-ready**

---

## 🔬 Example Processing Flow

```
1. Upload video
2. Extract frames
3. Detect pose landmarks
4. Calculate biomechanical metrics
5. Detect phase transitions
6. Apply skill scoring rules
7. Return structured JSON
```

Example output:

```json
{
  "skill": "tackle",
  "score": 78,
  "metrics": {
    "pad_level": 32,
    "forward_drive": 1.4,
    "contact_frame": 87
  }
}
```

---

## 🧪 Advanced CV Research Integration

Potential / Experimental Integrations:

* RF-DETR for person segmentation
* YOLO for object (ball/barbell) detection
* Line fitting logic for curvature mapping
* Back Roundness Map visualization

---

## 🛡 Design Philosophy

* No ML black-box scoring
* Transparent, rule-based evaluation
* Coach-adjustable weights
* Modular skill system

---

## 📈 Long-Term Vision

SpartanMetrics Backend is designed to evolve into:

* Real-time analysis engine
* Multi-sport biomechanics evaluator
* AI-powered coaching assistant

---
