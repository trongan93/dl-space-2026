# Deep Learning in Space Technology Applications — 115-1 (Fall 2026)

Course notebooks for **338688 深度學習與太空科技應用**, National Taipei University of Technology, Dr. Trong-An Bui (ASV Lab).
Every notebook runs in Google Colab with one click; nothing needs to be installed locally.

| Week | Notebook | Open |
|---|---|---|
| 2 | Lab 0 — a Sentinel-2 scene of Taipei: open, decode, look, measure | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week2_Lab0_Sentinel2_GeoTIFF.ipynb) |
| 3 | **Demo** — satellite image processing on a real scene (in-class) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week3_Demo_Satellite_Image_Processing.ipynb) |
| 3 | Lab 1 — the dataset contract: chip, split, baseline, document | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week3_Lab1_Dataset_Contract.ipynb) |
| 4 | **Lab 1** — train your first CNN: ships in satellite images (PyTorch, 25 min) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week4_Lab1_Ship_CNN_Training.ipynb) |
| 4 | Lab 2 — detection and tracking of ships and vehicles (TA workshop) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week4_Lab2_Detection_Tracking.ipynb) |
| — | Instructor: prepare the bundled sample scene (run once) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/trongan93/dl-space-2026/blob/main/notebooks/Week0_Prepare_Sample_Data.ipynb) |

## How the data works
Notebooks fetch a live Sentinel-2 L2A window over Taipei from [Earth Search](https://earth-search.aws.element84.com/v1) (STAC, cloud-optimised GeoTIFFs).
If that fails they fall back to `data/taipei_s2_sample.tif` + `data/taipei_s2_sample_scl.tif` — one real Sentinel-2 window bundled here — and, as a last resort, to a clearly labelled synthetic scene.
Students who have their own Lab 0 output (`lab0_cube.tif`, `lab0_scl.npy`) can upload it to a session; the Week 3 demo prefers it.

## Layout
```
notebooks/   the Colab notebooks (open from the table above)
data/        bundled sample scene (created with Week0_Prepare_Sample_Data.ipynb)
data/shipsnet/  4 000 Planet chips (80 x 80, ship / not-ship, with scene ids) + two full scenes, for Week 4 Lab 1
```

Sentinel-2 data: *Copernicus Sentinel data 2026*. Landsat: USGS. Ship chips: 'Ships in Satellite Imagery' (Planet, CC-BY-SA 4.0), repackaged. Course slides and handouts are distributed on i-School Plus and MS Teams.
