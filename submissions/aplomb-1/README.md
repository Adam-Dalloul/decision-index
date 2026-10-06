# Aplomb 1

[empiriolabsai/aplomb-1](https://huggingface.co/empiriolabsai/aplomb-1) is a 5.3B decision model from EmpirioLabs, with
open weights under the EmpirioLabs Model License.

| | |
|---|---|
| Decision Index 0.2.1 | **44.86** |
| Area skill | knowledge 29.7 · language 48.3 · retrieval 49.5 · tools 62.4 · arts 33.9 |
| Requests | 150,759, all `ok`, none unsupported, no errors |
| Results | [empiriolabsai/decision-index-results-aplomb-1](https://huggingface.co/datasets/empiriolabsai/decision-index-results-aplomb-1/tree/ceb1bab8587e404fb88c21781aa8264c90f25ee6/runs/aplomb-1) (`--compact`, no suite text) |

## Running it

The hosted API serves the same model with the same settings on `/v1/systemone`:

```sh
DECISION_INDEX_API_KEY=... python -m decision_index run --engine http \
    --option base_url=https://api.empiriolabs.ai --option model=aplomb-1 ...
```

We can send an evaluation key privately. The weights and a reference script (`run_aplomb.py`) are on the model page.

## Training data

Training data included the public train splits of WinoGrande and ContractNLI, two of the suite's benchmarks. We could
not fully verify that suite items were excluded from the earliest training data.
