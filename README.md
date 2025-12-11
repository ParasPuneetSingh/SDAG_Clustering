# README.md
# SDAG — Silhouette-Driven Adaptive Density Growth
Official anonymous implementation for the ECML PKDD 2026 submission.

## One-line usage
```python
from sdag import SDAG
from sklearn.datasets import make_moons

X, y = make_moons(n_samples=1500, noise=0.08, random_state=42)
sdag = SDAG(random_state=42)
sdag.fit(X)
print("ARI:", adjusted_rand_score(y, sdag.labels_))
