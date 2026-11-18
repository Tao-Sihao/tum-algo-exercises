# TUM Algo – Exercises

Exercise submissions of Tao-Sihao. Each exercise lives in its own folder `exN/`.

| Exercise | Topic | Files |
|---|---|---|
| [ex4](ex4/) | NetworkX tutorial: graph basics, layouts, degree distributions, IMDB co-star graph | [`networkx-tutorial.ipynb`](ex4/networkx-tutorial.ipynb) |
| [ex5](ex5/) | PageRank from scratch (dense + sparse power iteration) on EPL 2024/25 and Wiki-Vote | [`ex10.ipynb`](ex5/ex10.ipynb) |

## Running

```bash
pip install networkx pandas matplotlib scipy jupyter
jupyter notebook ex4/networkx-tutorial.ipynb
jupyter notebook ex5/ex10.ipynb
```

## Notes on ex4

- `sierpinski.txt` (Task 2) was not part of the provided material. The notebook generates a level-4 Sierpinski gasket edge list in the same `u v` format when the file is missing. Drop in the original file to use it instead.
- Task 3 uses `imdb_top100.csv`, which is the file that was provided (the task text mentions `imdb_top250.csv`).
- The saved co-star graph (k = 1, num_stars = 10) is `imdb_costar_k1_s10.gml` / `.graphml`.

## Notes on ex5

- The notebook is called `ex10.ipynb` (title "EX10: Implement PageRank") as provided; it lives in `ex5/`.
- EPL graph: edge A → B if B beat A in 2024/25 (350 matches in the file). Repeated wins over the same opponent collapse into one edge (simple `DiGraph`).
- `pagerank_step` uses `float64` instead of the starter's `float32`, so the L1 tolerance of 1e-6 is reached reliably.
- The 3.5 check converts the `nx.pagerank` dict to an array in node order before comparing (the starter compared a dict to an array).
- Wiki-Vote is only run with the sparse implementation (a dense 7115 × 7115 matrix would be ~0.4 GB).
