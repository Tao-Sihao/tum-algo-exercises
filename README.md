# TUM Algo – Exercises

Exercise submissions of Tao-Sihao. Each exercise lives in its own folder `exN/`.

| Exercise | Topic | Files |
|---|---|---|
| [ex4](ex4/) | NetworkX tutorial: graph basics, layouts, degree distributions, IMDB co-star graph | [`networkx-tutorial.ipynb`](ex4/networkx-tutorial.ipynb) |

## Running

```bash
pip install networkx pandas matplotlib scipy jupyter
jupyter notebook ex4/networkx-tutorial.ipynb
```

## Notes on ex4

- `sierpinski.txt` (Task 2) was not part of the provided material. The notebook generates a level-4 Sierpinski gasket edge list in the same `u v` format when the file is missing. Drop in the original file to use it instead.
- Task 3 uses `imdb_top100.csv`, which is the file that was provided (the task text mentions `imdb_top250.csv`).
- The saved co-star graph (k = 1, num_stars = 10) is `imdb_costar_k1_s10.gml` / `.graphml`.
