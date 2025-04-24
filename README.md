# time-series-clustering
This project performs time series clustering on the `Trace` dataset using two methods: **K-means (Euclidean distance)** and **Hierarchical Clustering (Dynamic Time Warping)**. The goal is to compare their performance in grouping time series with temporal distortions.

---

## 📊 Results

### Clustering Performance Metrics
| **Metric**               | **K-means (Euclidean)** | **Hierarchical (DTW)** |
|--------------------------|-------------------------|------------------------|
| Adjusted Rand Index (ARI) | 0.327                   | 0.411                  |
| Normalized Mutual Info (NMI) | 0.502               | 0.548                  |

### Key Observations
1. **Hierarchical Clustering with DTW** outperformed K-means, but both methods scored below expected benchmarks (ARI ≈ 0.75–0.92 for DTW in ideal setups).
2. Potential reasons for suboptimal performance:
   - Label misalignment (original labels were `[1, 2, 3, 4]` instead of `[0, 1, 2, 3]`).
   - Lack of DTW constraints (e.g., Sakoe-Chiba band).
   - Library version mismatches.
## How to Run
 **Google Colab**: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1kqWTPy4__HFrniPsTGXewcKCR2N8Oswd#scrollTo=aZ9ggbVrWt-X)

