### **P3**

| step | $N^{'}$ | D(t),p(t) | D(u),p(u) | D(v),p(v) | D(w),p(w) | D(y),p(y) | D(z),p(z) |
| ---- | ------- | --------- | --------- | --------- | --------- | --------- | --------- |
| 0    | x       | $\infty$  | $\infty$  | 3,x       | 6,x       | 6,x       | 8,x       |
| 1    | xv      | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |
| 2    | xvu     | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |
| 3    | xvuw    | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |
| 4    | xvuwy   | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |
| 5    | xvuwyt  | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |
| 6    | xvuwytz | 7,v       | 6,v       | 3,x       | 6,x       | 6,x       | 8,x       |

### **P5**

初始

|      |      |          | 值       |          |          |          |
| ---- | ---- | -------- | -------- | -------- | -------- | -------- |
|      |      | u        | v        | x        | y        | z        |
|      | v    | $\infty$ | $\infty$ | $\infty$ | $\infty$ | $\infty$ |
| 从   | x    | $\infty$ | $\infty$ | $\infty$ | $\infty$ | $\infty$ |
|      | z    | $\infty$ | 6        | 2        | $\infty$ | 0        |

第一次迭代

|      |      |          | 值   |      |          |      |
| ---- | ---- | -------- | ---- | ---- | -------- | ---- |
|      |      | u        | v    | x    | y        | z    |
|      | v    | 1        | 0    | 3    | $\infty$ | 6    |
| 从   | x    | $\infty$ | 3    | 0    | 3        | 2    |
|      | z    | 7        | 5    | 2    | 5        | 0    |

第二次迭代

|      |      |      | 值   |      |      |      |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|      |      | u    | v    | x    | y    | z    |
|      | v    | 1    | 0    | 3    | 3    | 5    |
| 从   | x    | 4    | 3    | 0    | 3    | 2    |
|      | z    | 6    | 5    | 2    | 5    | 0    |

第三次迭代

|      |      |      | 值   |      |      |      |
| ---- | ---- | ---- | ---- | ---- | ---- | ---- |
|      |      | u    | v    | x    | y    | z    |
|      | v    | 1    | 0    | 3    | 3    | 5    |
| 从   | x    | 4    | 3    | 0    | 3    | 2    |
|      | z    | 6    | 5    | 2    | 5    | 0    |

### **P6**

意思是，“第一次运行算法时的迭代次数”(也就是说，假设节点最初拥有的唯一信息是其最近的邻居的成本)。我们假设该算法是同步运行的(即，在一个步骤中，所有节点同时计算它们的距离表，然后交换表)。在每次迭代时，节点与其邻居交换距离表。因此，如果您是节点A，而您的邻居是B，则B的所有邻居(它们都是您的一两跳)在一次迭代后(即B告诉他们它对您的成本后)将知道一到两个跳到您的最短代价路径。d是网络的“直径”--网络中任何两个节点之间最长的无环路路径的长度。使用上面的推理，经过d-1迭代后，所有节点都将知道d或更少跳到所有其他节点的最短路径代价。由于任何大于d跳的路径都会有循环(因此比去掉循环的路径花费更大)，该算法最多会在d-1迭代中收敛。

​                                                                                                  ***2017302580236 刘一婧***