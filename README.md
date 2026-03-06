# 🧠 Explainable Neural Network Builder

> **Build transparent, interpretable neural networks — no black boxes allowed.**

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![XAI](https://img.shields.io/badge/XAI-Explainable%20AI-7b61ff?style=flat)](https://en.wikipedia.org/wiki/Explainable_artificial_intelligence)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

## 🎯 What Is This?

The **Explainable Neural Network Builder** is an interactive, browser-based tool that lets you design, train, and — most importantly — **understand** neural networks. Every decision the network makes is made transparent through multiple explainability techniques.

Traditional deep learning is a black box. This tool inverts that paradigm.

---

## ✨ Features

### 🏗️ Network Architecture Builder
- **Drag-and-drop layer creation** — add Input, Dense, Attention, and Output layers
- **Configurable neurons** (1–64) and **activation functions** (ReLU, Sigmoid, Tanh, Linear, Softmax)
- **Live parameter count** — see how complex your network is in real time
- **Interpretability complexity indicator** 🟢 Low / 🟡 Medium / 🔴 High

### 🔭 Live Network Visualization
- **Animated canvas rendering** of the network architecture
- **Weight-thickness encoding** — thicker connections = higher weights
- **Activation-brightness encoding** — brighter nodes = higher activations
- **Per-neuron activation values** shown during forward pass

### 📊 Four Real Datasets
| Dataset | Features | Classes | Use Case |
|---|---|---|---|
| 🌸 Iris Flowers | 4 | 3 | Classic ML benchmark |
| 🩺 Diabetes Risk | 8 | 2 | Healthcare prediction |
| 💳 Credit Score | 6 | 2 | Financial decision |
| 💬 Text Sentiment | 5 | 2 | NLP classification |

### 🔍 Three Explainability Views

#### 1. SHAP Values (SHapley Additive exPlanations)
- Per-feature contribution bars (positive = pushes toward prediction, negative = pushes against)
- Switch between 5 sample inputs to compare explanations
- Real-time prediction with confidence bar

#### 2. Attention Heatmap
- Visual matrix showing how much the network "attends" to each feature per class
- Color-coded intensity (purple = high attention, blue = medium, dark = low)
- Ranked feature importance bars

#### 3. Decision Rules
- Human-readable `IF ... THEN ...` rules extracted from weight patterns
- Per-rule confidence scores
- Color-coded importance (green = high confidence, orange = medium, red = low)

### 🛤️ Full Decision Path Tracing
Every prediction includes a step-by-step trace through each layer:
- What each layer received as input
- How many neurons were activated (and by how much)
- Final prediction with confidence percentage

### 📈 Interpretability Score Dashboard
Four ring charts measuring:
- **Transparency** — how visible the decision process is
- **Fidelity** — how accurately explanations reflect the model
- **Stability** — consistency of explanations across inputs
- **Completeness** — coverage of decision factors

---

## 🚀 Getting Started

### Option 1: Run Locally
```bash
git clone https://github.com/PranayMahendrakar/explainable-neural-network-builder.git
cd explainable-neural-network-builder
# Open index.html in your browser
open index.html
```

### Option 2: GitHub Pages
Visit the live demo at:
`https://pranayMahendrakar.github.io/explainable-neural-network-builder`

---

## 🧪 How to Use

1. **Choose a dataset** from the left panel (Iris, Diabetes, Credit, or Sentiment)
2. **Build your network** — click layer type buttons to add layers
3. **Configure training** — set learning rate and number of epochs
4. **Click "▶ Train & Explain"** — watch real-time training and explanations
5. **Explore the right panel** — switch between SHAP, Attention, and Rules tabs
6. **Click different samples** (S1–S5) to see per-sample explanations
7. **Trace the decision path** — see exactly how each layer processed the input

---

## 🔬 XAI Techniques Implemented

| Technique | Description | Implementation |
|---|---|---|
| **SHAP** | Feature contribution via marginal attribution | Perturbation-based approximation |
| **Attention Weights** | What the model focuses on | First-layer weight magnitudes |
| **Rule Extraction** | IF-THEN rules from weights | Weight-threshold rule mining |
| **Decision Path** | Layer-by-layer trace | Full forward pass logging |
| **Activation Visualization** | Neuron-level firing patterns | Forward pass activations |
| **Weight Transparency** | Weight values on layer cards | Direct weight inspection |

---

## 🧠 Why Explainable AI Matters

> *"If you can't explain it simply, you don't understand it well enough."* — attributed to Einstein

**Explainable AI (XAI)** is critical in:
- **Healthcare** — doctors need to understand why a model flagged a diagnosis
- **Finance** — regulators require models to justify credit decisions (GDPR Art. 22)
- **Legal** — algorithmic decisions affecting people must be contestable
- **Science** — research demands reproducibility and interpretability
- **Safety** — autonomous systems must have auditable decision logic

This tool demonstrates that neural networks **don't have to be black boxes**. With the right design choices and post-hoc analysis, every weight, every activation, and every decision can be made transparent.

---

## 🛠️ Technical Architecture

```
index.html
├── CSS Styles (embedded)
│   ├── Dark space-themed UI
│   ├── Responsive 3-panel layout
│   └── Animated components
├── HTML Structure
│   ├── Left Panel: Network Builder
│   ├── Center Panel: Visualization
│   └── Right Panel: Explanations
└── JavaScript (embedded)
    ├── Network State Management
    ├── Layer CRUD Operations
    ├── Forward Pass (pure JS)
    ├── Backpropagation (simplified)
    ├── Canvas Rendering (2D API)
    ├── SHAP Value Computation
    ├── Attention Heatmap Generation
    ├── Rule Extraction Engine
    └── Decision Path Tracer
```

**Zero dependencies** — no frameworks, no libraries, pure HTML/CSS/JS.

---

## 📚 Research Context

This project draws inspiration from:
- **LIME** (Local Interpretable Model-agnostic Explanations) — Ribeiro et al., 2016
- **SHAP** (SHapley Additive exPlanations) — Lundberg & Lee, 2017
- **Attention is All You Need** — Vaswani et al., 2017
- **Grad-CAM** — Selvaraju et al., 2017
- **Network Dissection** — Bau et al., 2017

---

## 🤝 Contributing

Contributions are welcome! Ideas for future additions:
- [ ] Grad-CAM for image classification
- [ ] Counterfactual explanations ("What would need to change?")
- [ ] LIME local approximations
- [ ] Export explanations as PDF reports
- [ ] Compare multiple model explanations side-by-side
- [ ] Adversarial example generation

---

## 👨‍💻 Author

**Pranay M Mahendrakar**
- Dynamic AI Specialist & Published Author
- [ORCID: 0009-0003-7224-029X](https://orcid.org/0009-0003-7224-029X)
- [sonytech.in/pranay](https://sonytech.in/pranay)

---

## 📄 License

MIT License — free for research, education, and commercial use.

---

*Part of the XAI Research Series — making AI understandable, one network at a time.* 🧠
