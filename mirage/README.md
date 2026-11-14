---
library_name: cactus-compute
pipeline_tag: image-text-to-text
license: apache-2.0
language:
  - en
  - de
  - fr
  - es
  - it
  - nl
  - pl
tags:
  - image-to-text
  - object-detection
  - zero-shot-object-detection
  - image-segmentation
  - image-classification
  - zero-shot-image-classification
  - visual-question-answering
  - document-question-answering
---

[![Mirage overview with scene descriptions, object detection, OCR, segmentation, spatial relations and decisions](https://huggingface.co/Cactus-Compute/mirage/resolve/main/assets/overview.png)](https://cactuscompute.com/blog/mirage#sandbox)

# Mirage

A vision model for image understanding and structured extraction.

## Get started

```sh
pip install -U cactus-compute
```

```python
import cactus

print(cactus.Mirage().describe("photo.png"))
```

The package downloads and caches the engine and weights on first use.
This repository provides `mirage.cact`, `mirage.safetensors` and the model config.

- [Model details and playground](https://cactuscompute.com/blog/mirage)
- [Python API](https://cactuscompute.com/blog/needle-python-docs)
- [Runtime binaries and supported platforms](https://huggingface.co/Cactus-Compute/cactus)
- [Source code](https://github.com/cactus-compute/cactus)
