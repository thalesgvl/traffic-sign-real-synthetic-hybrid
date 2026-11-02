# Traffic Sign Detection with Real, Synthetic, and Hybrid Data

Code, configurations, results, and data pointers for the paper

> T. Germano, P. Sampaio, V. Pereira, R. Rodrigues da Silva, and E. L. Silva Teixeira,
> "Cross-Domain Evaluation of Traffic Sign Detection Using Real, Synthetic, and Hybrid Data,"
> Special Session on Safe and Secure Vehicles (SSV 2026),
> XVI Brazilian Symposium on Computing Systems Engineering (SBESC 2026), Salvador, Brazil, 2026.

Automotive Research Center, Universidade de Brasília.

> **Status:** the repository is being populated for the final version of the paper
> (November 2026). Sections marked *pending* are not available yet.

## What the study does

A YOLO26s detector is trained under three regimes (real, synthetic, and a 1:1 hybrid
of both) and each model is evaluated on a held-out real benchmark and a held-out
synthetic benchmark, giving a 3×2 evaluation matrix. All metrics are computed at one
fixed operating point.

## Repository layout

| Path | Contents | Status |
|---|---|---|
| [`configs/train/`](configs/train/) | `args.yaml` of each training run | pending |
| [`configs/data/`](configs/data/) | `data.yaml` files with relative paths and the class order | pending |
| [`scripts/`](scripts/) | evaluation at a fixed confidence threshold, dataset counts, figure scripts | pending |
| [`results/`](results/) | CSV files behind every table of the paper | pending |
| [`weights/`](weights/) | how to download the trained weights and their SHA-256 checksums | pending |
| [`data/`](data/) | where each part of the data is hosted, licenses, and file manifests | pending |

Large files are **not** stored in this git repository:

- trained weights are attached to a [GitHub Release](../../releases);
- the synthetic dataset and the real benchmark are archived on Zenodo (DOI pending);
- the public real training sources are obtained from their providers (see [`data/`](data/)).

## Environment

The experiments used Python 3.12, Ultralytics 8.4.4, and PyTorch 2.6.0 (CUDA 12.4)
on an NVIDIA GeForce RTX 4080 SUPER.

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

## Reproducing the results

*Pending.* This section will list the commands that rebuild every table of the
paper from the released weights and benchmarks.

## Citation

See [`CITATION.cff`](CITATION.cff), or use the "Cite this repository" button on GitHub.
The IEEE Xplore DOI will be added after publication.

## License

*Pending.* Code and data licenses will be added before the data release.
