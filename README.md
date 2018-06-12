# py-metazelda
Python-based level generation, inspired by MetaZelda - https://github.com/tcoxon/metazelda
```
Some example usage below.
>>> g = Map()
>>> a = MapGenerator()  # defaults to 3x3x1 map.
>>> a.view(g)
+---+---+---+
|   |       |
+   +   +   +
|   | O |   |
+   +---+   +
|           |
+---+---+---+

Example of manual carving. autocarve set to False
>>> g2 = Map(rows=10, columns=10, levels=2, autocarve=False)
>>> a.view(g2)
+---+---+---+---+---+---+---+---+---+---+
| O | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "s")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
| O | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "s")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
| O | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "east")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|     O | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "east")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|         O | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "east")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|             O | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.dig(g2, "s")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|               | # | # | # | # | # | # |
+---+---+---+   +---+---+---+---+---+---+
| # | # | # | O | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

Reset to original state, all cells uncarved.
>>> a.reset(g2)
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | O | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

>>> a.random_position(g2)
>>> a.view(g2)
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | O | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+
| # | # | # | # | # | # | # | # | # | # |
+---+---+---+---+---+---+---+---+---+---+

Auto digging, normally defaults to the 100% usage of space but can be specified.
Seed support, a map with the same settings and seed can then be reproduced.
a = Map(seed=2100, rows=10, columns=10, levels=1, autocarve=True, random_start=True, keys=4, max_carved_nodes_percent=75)
b.view(a)
+---+---+---+---+---+---+---+---+---+---+
|           | # | # | # | # | # | # | # |
+   +---+   +---+---+---+---+---+---+---+
|       |       | # | # | # | # | # | # |
+   +   +---+   +---+---+---+---+---+---+
|   |   | # |       | # | # | # | # | # |
+   +.__+---+---+   +---+---+---+---+---+
|   |       | # |               | # | # |
+---+---+   +---+---+---+---+   +---+---+
|           | # |           |       !   |
+   +---+---+---+   +---+   +---+---+   +
|   |               |           |   |   |
+   +   +---+---+---+   +---+   +   +   +
|   |   |     O | # |   |           |   |
+   +   +   +---+---+.__+---+---+---+   +
|   |       | # |   |                   |
+   +---+---+---+   +   +---+---+---+---+
|           |       |       |           |
+   +---+   +   +---+---+   +---+---+   +
|       |       |   !                   |
+---+---+---+---+---+---+---+---+---+---+

Now a key level view of each cell.
Each cell's interior is marked with its key level.
b.view(a, key_levels=True)
+---+---+---+---+---+---+---+---+---+---+
| 1   1   1 | # | # | # | # | # | # | # |
+   +---+   +---+---+---+---+---+---+---+
| 1   1 | 1   1 | # | # | # | # | # | # |
+   +   +---+   +---+---+---+---+---+---+
| 1 | 1 | # | 1   1 | # | # | # | # | # |
+   +.__+---+---+   +---+---+---+---+---+
| 1 | 0   0 | # | 1   1   1   1 | # | # |
+---+---+   +---+---+---+---+   +---+---+
| 0   0   0 | # | 3   3   3 | 1   1 ! 2 |
+   +---+---+---+   +---+   +---+---+   +
| 0 | 3   3   3   3 | 3   3   3 | 3 | 2 |
+   +   +---+---+---+   +---+   +   +   +
| 0 | 3 | 3   O | # | 3 | 3   3   3 | 2 |
+   +   +   +---+---+.__+---+---+---+   +
| 0 | 3   3 | # | 0 | 2   2   2   2   2 |
+   +---+---+---+   +   +---+---+---+---+
| 0   0   0 | 0   0 | 2   2 | 2   2   2 |
+   +---+   +   +---+---+   +---+---+   +
| 0   0 | 0   0 | 3 ! 2   2   2   2   2 |
+---+---+---+---+---+---+---+---+---+---+


```
