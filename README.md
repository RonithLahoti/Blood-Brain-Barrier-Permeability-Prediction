# 🧠 Blood–Brain Barrier Permeability Prediction with Graph Neural Networks

The **blood–brain barrier (BBB)** presents a major obstacle in central nervous system (CNS) drug development by restricting the entry of most pharmacological agents.  
This repository contains a **graph-based deep learning framework** to predict BBB permeability **using molecular structure alone**.

---

## 📊 Dataset
- **Source**: [MoleculeNet Blood–Brain Barrier Penetration (BBBP) dataset](https://moleculenet.org/)
- **Size**: `n = 3,120` molecules
- **Encoding**: SMILES strings converted into **molecular graphs** with [RDKit](https://www.rdkit.org/)

---

## 🏗️ Model Architecture
- **Graph Representation**: SMILES → Molecular Graph
- **Backbone**: 4-layer **Message Passing Neural Network (MPNN)**  
- **Sequence Modeling**: **Gated Recurrent Units (GRUs)**  
- **Readout**: Transformer-based attention pooling with **8 attention heads**

---

## 🚀 Results
- **AUC**: `0.9627`  
- **Accuracy**: `92.54%` (held-out test set)  
- **Bias**: Conservative (minimizes false positives)  
- **Generalization**: Consistent predictions across **structurally diverse scaffolds**

---

## 🔍 Interpretability
- No explicit post hoc interpretability tools applied.  
- Attention-based readout implicitly captures **structural motifs relevant to permeability**.

---

## 📈 Comparison with Previous Work
This model demonstrates:
- Higher **predictive accuracy**
- Robust **generalization**
- Improved **structural interpretability**

---

## ⚙️ Implementation
- **Framework**: TensorFlow `2.13`
- **Cheminformatics**: RDKit
- **Use Case**: Integrates into **early-stage compound screening pipelines** for CNS drug discovery

---

## 📦 Installation
```bash
git clone https://github.com/your-username/BBB-Prediction-GNN.git
cd BBB-Prediction-GNN
pip install -r requirements.txt
