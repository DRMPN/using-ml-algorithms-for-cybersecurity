# using-ml-algorithms-for-cybersecurity

[![OSA-improved](https://img.shields.io/badge/improved%20by-OSA-yellow)](https://github.com/aimclub/OSA)

Built with:

![numpy](https://img.shields.io/badge/NumPy-013243?logo=NumPy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![scipy](https://img.shields.io/badge/SciPy-8CAAE6?logo=SciPy&logoColor=white)
![tqdm](https://img.shields.io/badge/tqdm-FFC107?logo=tqdm&logoColor=black)

---

## Overview

The project offers a unified resource that turns raw network data and related artifacts into actionable threat insights, enabling accurate identification of malicious traffic, domains, and commands. It streamlines model tuning and provides hands-on learning materials, giving security teams and learners a practical edge in modern cyber defense.

---

## Table of Contents

- [Overview](#overview)
- [Core features](#core-features)
- [Installation](#installation)
- [Contributing](#contributing)
- [Citation](#citation)

---

## Core features

1. **Comprehensive Packet Flow Feature Engineering**: Generates raw, statistical and merged packet features (e.g., `tcp_len_*`, entropy, client/server ratios) via dedicated helpers like `process_flow` and `extract_statistical_features` to describe each network flow in 30-packet windows.  
2. **Automated Hyper-parameter Optimization with LightGBM**: Uses `RandomizedSearchCV` to tune a multi-class LightGBM classifier over dozens of parameters (estimators, leaves, depth, bagging, etc.) for accurate application-service identification.  
3. **HTTP Malware Detection Pipeline**: Extracts TF-IDF character n-gram vectors from HTTP request/response fields plus handcrafted URL features (length, entropy, hex-flags) and feeds them into an XGBoost classifier with file-level feature aggregation.

---

## Installation

Build from source:

```sh
git clone https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity
cd using-ml-algorithms-for-cybersecurity
pip install -r requirements.txt
```

---

## Contributing

- **[Report Issues](https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity/issues)** — submit bugs or feature requests.  
- **[Submit Pull Requests](https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity/tree/main/.github/CONTRIBUTING.md)** — see contribution guidelines.

---

## Citation

If you use this software, please cite it as below.

### APA

DRMPN (2025). using-ml-algorithms-for-cybersecurity repository [Computer software]. https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity

### BibTeX

```bibtex
@misc{using-ml-algorithms-for-cybersecurity,
  author       = {DRMPN},
  title        = {using-ml-algorithms-for-cybersecurity repository},
  year         = {2025},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity}},
  url          = {https://github.com/DRMPN/using-ml-algorithms-for-cybersecurity}
}
```

---
