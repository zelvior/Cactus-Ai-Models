---
library_name: cactus-compute
pipeline_tag: text-generation
license: apache-2.0
tags:
  - tool-calling
  - function-calling
  - on-device
  - edge
  - quantization
  - webassembly
---

![Cactus Compute - Sub-50mb Super Intelligence For Consumer Devices](https://raw.githubusercontent.com/cactus-compute/cactus/main/assets/banner.svg)

# Needle 3

An on-device model for tool calling, structured extraction and text embeddings.
See the [Needle website](https://cactuscompute.com/needle) for model details, benchmarks and the browser demo.

## Get started

```sh
pip install -U cactus-compute
```

```python
import cactus

@cactus.tool
def get_weather(city: str):
    "Get the current weather for a city."
    return {"city": city, "temp_c": 27, "sky": "clear"}

with cactus.Cactus(tools=[get_weather]) as agent:
    print(agent.run("What's the weather in Lagos?")["results"])
```

The package downloads and caches the engine and weights on first use.
This repository provides `needle3.cact` and `checkpoints/needle3.safetensors`.
[Runtime binaries and supported platforms](https://huggingface.co/Cactus-Compute/cactus) live in the Cactus repository.

## Guides

- [Python API](https://cactuscompute.com/blog/needle-python-docs)
- [Designing tools](https://cactuscompute.com/blog/designing-tools-for-needle) and [structured extraction](https://cactuscompute.com/blog/structured-extraction-with-needle)
- [Fine-tuning](https://cactuscompute.com/blog/finetuning-needle)
- [Source code](https://github.com/cactus-compute/cactus)
