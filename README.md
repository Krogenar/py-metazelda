# py-metazelda
Python-based level generation, inspired by MetaZelda.


g = Map()
a = MapGenerator()
a.view(g)
+---+---+---+
|   |       |
+   +   +   +
|   | O |   |
+   +---+   +
|           |
+---+---+---+
g2 = Map(rows=10, columns=10, levels=2, autocarve=False)
a.view(g2)
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

a.dig(g2, "s")
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

a.dig(g2, "s")
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

a.dig(g2, "east")
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

a.dig(g2, "east")
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

a.dig(g2, "east")
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

a.dig(g2, "s")
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

a.dig(g2, "s")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|               | # | # | # | # | # | # |
+---+---+---+   +---+---+---+---+---+---+
| # | # | # |   | # | # | # | # | # | # |
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

a.dig(g2, "east")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|               | # | # | # | # | # | # |
+---+---+---+   +---+---+---+---+---+---+
| # | # | # |   | # | # | # | # | # | # |
+---+---+---+   +---+---+---+---+---+---+
| # | # | # |     O | # | # | # | # | # |
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

a.dig(g2, "n")
+---+---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|   | # | # | # | # | # | # | # | # | # |
+   +---+---+---+---+---+---+---+---+---+
|               | # | # | # | # | # | # |
+---+---+---+   +---+---+---+---+---+---+
| # | # | # |   | O | # | # | # | # | # |
+---+---+---+   +   +---+---+---+---+---+
| # | # | # |       | # | # | # | # | # |
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

a.reset(g2)
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

a.random_position(g2)
a.view(g2)
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

a.auto_dig(g2)
a.view(g2)
+---+---+---+---+---+---+---+---+---+---+
| ^   ^ | ^ |   | ^ | ^ | ^ | ^ |     ^ |
+---+---+   +   +   +   +   +---+   +---+
| ^ |       | ^ |   |       | ^     |   |
+   +   +---+   +   +---+   +---+---+   +
|   |   |   |   |           | ^ | ^ | ^ |
+---+   +   +   +---+---+---+   +   +   +
| ^ | ^ |   | ^ | ^   ^ | ^ |   |       |
+   +---+   +---+---+   +---+   +---+---+
|     ^ |               | ^ | ^ |     ^ |
+---+---+---+---+---+---+   +---+   +---+
|                     ^ |       | ^ | ^ |
+---+   +---+---+---+---+---+   +---+   +
| ^     | ^     | ^       ^ |       |   |
+---+   +---+   +---+---+---+   +---+   +
| ^ |   | ^ |   | ^     | ^     | ^ | ^ |
+   +   +   +   +---+   +---+---+   +   +
|       |   |   |   |           | ^ | ^ |
+---+---+   +   +   +---+---+   +---+---+
| ^         | ^ | ^ | ^   ^ |     ^ | O |
+---+---+---+---+---+---+---+---+---+---+
