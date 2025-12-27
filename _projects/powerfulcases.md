---
layout: page
title: PowerfulCases
description: Test case data for power systems simulation - works with Julia and Python
img: /assets/img/proj_powerfulcases_icon.svg
importance: 1
category: applied
related_publications: false
giscus_comments: true
---

<div class="row justify-content-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="/assets/img/proj_powerfulcases_icon.svg" alt="PowerfulCases Logo" style="max-width: 200px;">
    </div>
</div>

## Stop Hunting for Test Cases

**PowerfulCases** provides ready-to-use power system test cases for simulation and research.
No more searching for IEEE test cases or dealing with inconsistent file formats.

<a href="https://github.com/cuihantao/PowerfulCases" class="btn btn-primary btn-lg" target="_blank">
    <i class="fab fa-github"></i> View on GitHub
</a>
<a href="https://pypi.org/project/powerfulcases/" class="btn btn-success btn-lg" target="_blank">
    <i class="fab fa-python"></i> Install from PyPI
</a>

---

## Quick Start

**Python:**
```bash
pip install powerfulcases
```

```python
import powerfulcases as pcase

case = pcase.load_case("ieee14")
print(case.raw)  # Path to RAW file
print(case.dyr)  # Path to DYR file
```

**Julia:**
```julia
using Pkg
Pkg.add(url="https://github.com/cuihantao/PowerfulCases")

using PowerfulCases
case = load_case("ieee14")
```

---

## Available Test Cases

| Case | Description |
|------|-------------|
| `ieee14` | IEEE 14-bus test system |
| `ieee39` | IEEE 39-bus (New England) system |
| `ieee118` | IEEE 118-bus system |
| `ACTIVSg2000` | ACTIVS 2000-bus synthetic grid |
| `ACTIVSg10k` | ACTIVS 10,000-bus synthetic grid |
| `ACTIVSg70k` | ACTIVS 70,000-bus synthetic grid |

---

## Key Features

- **Dual Language Support** - Same API for Julia and Python
- **Smart File Discovery** - Auto-detects RAW, DYR, and other formats
- **Multiple Variants** - Access different dynamic model variants (GENROU, GENSAL, etc.)
- **Large Case Handling** - Big cases downloaded on-demand, cached locally
- **Your Own Data** - Point to any directory with your proprietary cases

---

## CLI Tools

```bash
# List all cases
pcase list

# Pre-download large cases
pcase download ACTIVSg70k

# Check cache status
pcase cache-info

# Generate manifest for your own data
pcase create-manifest /path/to/your/case
```

---

<div class="row justify-content-center mt-4">
    <a href="https://github.com/cuihantao/PowerfulCases" class="btn btn-dark btn-lg" target="_blank">
        <i class="fab fa-github"></i> Get Started on GitHub
    </a>
</div>
