a nand b = not (a and b)
a and a = a
a nand a = not(a)
a and b = not (not (a and b)) = not (a nand b)
a or b = not(a) nand not(b) = not (not(a) and not(b)) = not(not(a)) or not(not(b)) = a or b
a mux b sel = (a and (not sel)) or (b and sel)

a b  nand
0 0  1
0 1  1
1 0  1
1 1  0

a b  and
0 0  0
0 1  0
1 0  0
1 1  1

a b  or
0 0  0
0 1  1
1 0  1
1 1  1

a b  Xor   a not(b) and    not(a)  b  and
0 0  0       0  1       0        1         0  0
0 1  1       0  0       0        1         1  1
1 0  1       1  1       1         0        0  0
1 1  0       1  0       0         0        1  0


| a | b |sel|out|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

|in |sel| a | b |
| 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 |
