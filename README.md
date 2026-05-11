# BAGEL

This repository contains the BAGEL core world-model code used by VLARLKit.

## Layout

```text
bagel/
  data/
  modeling/
train/
scripts/
```

- `bagel/` is the Python package imported by VLARLKit.
- `train/` and `scripts/` are repository-level entrypoints for data conversion and finetuning.
- Runtime world-model serving lives in VLARLKit under `env_clients/world_models/bagel`.

## Environment

This repository is intended to use an independent uv environment from the VLARLKit root environment.

```bash
cd third_party/BAGEL
uv sync
```

`flash-attn` is optional and is not installed by default:

```bash
uv sync --extra flash-attn
```

## Package Imports

Use the package prefix for core imports:

```python
from bagel.data.transforms import ImageTransform
from bagel.modeling.bagel import Bagel
```
