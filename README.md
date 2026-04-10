This `README.md` is designed to showcase the **BDC-Favelas Explorer** as a professional Research Infrastructure (RI). It highlights the contribution of the neuro-symbolic methodology and provides clear instructions for reproducibility.

-----

# BDC-Favelas Explorer: HNSA Infrastructure 🛰️

[](https://opensource.org/licenses/MIT)
[](https://www.go-fair.org/fair-principles/)

**HNSA (Hybrid Neuro-Symbolic Architecture)** is the core engine for the BDC-Favelas Explorer, a platform dedicated to mapping innovation ecosystems in informal urban settlements (favelas) in Brazil. By combining deep learning (GCN) with semantic reasoning (GeoSPARQL), we provide a verifiable, FAIR-compliant pipeline for socio-economic data.

## 🌟 Key Contributions

This repository contains the implementation of the HNSA framework, which addresses three critical challenges in the Semantic Web:

1.  **FAIRification of Informal Data:** Standardizing drone missions and territorial data using **STAC** (SpatioTemporal Asset Catalog) and **GeoSPARQL**.
2.  **Hallucination Mitigation:** Implementation of a **Symbolic Verification Gate** that reduces neural "hallucinations" (parametric drift) by **70.2%**.
3.  **Neuro-Symbolic Integration:** A hybrid pipeline where Graph Convolutional Networks (GCN) discover latent synergies, while SPARQL logic ensures ontological integrity.

## 🏗️ Architecture Overview

The HNSA infrastructure operates in three distinct stages:

  * **Ingestion:** Raw drone telemetry and census data are "lifted" into RDF via the STAC-to-RDF mapper.
  * **Projection:** A multi-layer GCN aligns informal territorial nodes with formal academic research programs in a shared latent manifold.
  * **Validation:** A Symbolic Gate executes GeoSPARQL `ASK` queries to verify if predicted entities fall within valid territorial boundaries (Rio de Janeiro Knowledge Base).

## 🚀 Getting Started

### Prerequisites

  - Python 3.9+
  - See `requirements.txt` for specific library versions.

### Installation

```bash
git clone https://github.com/your-username/bdc-favelas-explorer.git
cd bdc-favelas-explorer
pip install -r requirements.txt
```

### Running the Infrastructure Demo

The interactive Streamlit dashboard allows you to stress-test the Symbolic Gate and visualize hallucination suppression in real-time:

```bash
streamlit run app.py
```

## 📊 Experimental Results

Our experiments demonstrate that unconstrained neural models (Pure GCN) lose factual consistency as data noise increases. HNSA maintains **\>96% consistency** by rejecting out-of-bound spatial triples.

| Framework | Interoperability | Fact Consistency | Hallucination Rate |
| :--- | :--- | :--- | :--- |
| Pure Neural | Low (GeoJSON) | 75.5% | 24.5% |
| **HNSA (Ours)** | **High (GeoSPARQL)** | **96.8%** | **3.2%** |

## 📚 Citation

If you use this infrastructure in your research, please cite our  2026 paper:

```bibtex
@inproceedings{hnsa2026,
  title={HNSA: A FAIR-Compliant Neuro-Symbolic Infrastructure for Spatiotemporal Knowledge Graphs},
  author={Andre Valdestilhas},
  booktitle={TBA},
  year={2026}
}
```

-----

**Would you like me to generate a specific `LICENSE` file or a `CONTRIBUTING.md` guide to go along with this?**
