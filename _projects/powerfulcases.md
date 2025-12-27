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

```bash
pip install powerfulcases
```

```python
from powerfulcases import load

case = load("ieee14")
print(case.raw)  # Path to RAW file
print(case.dyr)  # Path to DYR file
```

---

<div class="row justify-content-center mt-4">
    <a href="https://github.com/cuihantao/PowerfulCases" class="btn btn-dark btn-lg" target="_blank">
        <i class="fab fa-github"></i> View on GitHub
    </a>
    <a href="https://pypi.org/project/powerfulcases/" class="btn btn-success btn-lg ms-2" target="_blank">
        <i class="fab fa-python"></i> PyPI
    </a>
</div>
