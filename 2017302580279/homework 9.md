

##### homework 9

###### P3

| 步骤 | N'      | D(t),p(t) | D(u),p(u) | D(v),p(v) | D(w),p(w) | D(y),p(y) | D(z),p(z) |
| ---- | ------- | --------- | --------- | --------- | --------- | --------- | --------- |
| 0    | x       | ∞         | ∞         | 3,x       | 6,x       | 6,x       | 8,x       |
| 1    | xv      | 7,v       | 3,v       |           | 6,x       | 6,x       | 8,x       |
| 2    | xvu     | 7,v       |           |           | 6,x       | 6,x       | 8,x       |
| 3    | xvuy    | 7,v       |           |           | 6,x       |           | 8,x       |
| 4    | xvuyw   | 7,v       |           |           |           |           | 8,x       |
| 5    | xvuywt  |           |           |           |           |           | 8,x       |
| 6    | xvuywtz |           |           |           |           |           |           |

| 源节点 | 目的节点 | 链路   | 最低开销 |
| ------ | -------- | ------ | -------- |
| x      | t        | (x, t) | 7        |
| x      | u        | (x, u) | 3        |
| x      | v        | (x, v) | 3        |
| x      | w        | (x, w) | 6        |
| x      | y        | (x, y) | 6        |
| x      | z        | (x, z) | 8        |

x到y最短为6，x到z最短为8，x到w最短为6，x到v最短为3，x到u(xvu)最短为6，x到t(xvuywt)最短为6

###### P5

| u    | v    | x    | y    | z    |      |
| ---- | ---- | ---- | ---- | ---- | ---- |
| v    | ∞    | ∞    | ∞    | ∞    | ∞    |
| x    | ∞    | ∞    | ∞    | ∞    | ∞    |
| z    | ∞    | 6    | 2    | ∞    | 0    |

|      | u    | v    | x    | y    | z    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| v    | 1    | 0    | 3    | ∞    | 6    |
| x    | ∞    | 3    | 0    | 3    | 2    |
| z    | 7    | 5    | 2    | 5    | 0    |

|      | u    | v    | x    | y    | z    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| v    | 1    | 0    | 3    | 3    | 5    |
| x    | 4    | 3    | 0    | 3    | 2    |
| z    | 6    | 5    | 2    | 5    | 0    |

###### P9

不会，因为降低链路开销不会导致循环。

如果将没有链路的两个节点连接起来，相当于将链路开销从无穷大降低到了有限大。