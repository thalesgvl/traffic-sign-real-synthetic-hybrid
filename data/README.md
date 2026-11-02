# Data

The images are not stored in this git repository. This folder documents where each
part of the data is hosted, under which license, and which files were used.

| Part | Origin | Hosted at | License | Status |
|---|---|---|---|---|
| Real training/validation: Mapillary Traffic Sign Dataset | Ertler et al., ECCV 2020 | provider only (not redistributed) | provider's terms | pending |
| Real training/validation: Roboflow Universe "Self-Driving Cars" | Roboflow Universe | provider only (not redistributed) | provider's terms | pending |
| Real test benchmark | recorded and annotated by the authors (Gama, Brasília, Aug. 2025) | Zenodo (DOI pending) | pending | pending (faces and license plates are blurred before release) |
| Synthetic training/validation | rendered by the authors in VI-grade VI-WorldSim and CARLA | Zenodo (DOI pending) | pending | pending |
| Synthetic test benchmark | rendered by the authors | Zenodo (DOI pending) | pending | pending |

## Manifests

[`manifests/`](manifests/) will list, for every split of every regime, the file names
and SHA-256 checksums of the images and labels that were used. For the public real
sources, these lists are what allows the exact training set to be rebuilt from the
provider's download.

## Expected local layout

The `data.yaml` files in [`../configs/data/`](../configs/data/) assume the archives are
extracted under `datasets/` at the repository root (ignored by git):

```
datasets/
  real/        images/{train,val}  labels/{train,val}
  synthetic/   images/{train,val}  labels/{train,val}
  hybrid/      (built from real/ and synthetic/ by a script in ../scripts/)
  bench_real/  images/test  labels/test
  bench_synth/ images/test  labels/test
```

*Pending:* this layout will be confirmed when the configuration files are added.
