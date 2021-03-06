Below are four graphs, each of which is defined by the sets of nodes,
initial nodes, final nodes, edges, and defs and uses. Each graph also
contains some test paths. Answer the following questions about each
graph.

(a) Draw the graph.

(b) List all of the du-paths with respect to x. (Note: Include all du-
paths, even those that are subpaths of some other du-path).

(c) Determine which du-paths each test path tours. Write them in a
table with test paths in the first column and the du-paths they
cover in the second column. For this part of the exercise, you
should consider both direct touring and sidetrips.

(d) List a minimal test set that satisfies all defs coverage with
respect to x. (Direct tours only.) If possible, use the given test
paths. If not, provide additional test paths to satisfy the criterion.

(e) List a minimal test set that satisfies all uses coverage with
respect to x. (Direct tours only.) If possible, use the given test
paths. If not, provide additional test paths to satisfy the criterion.

(f) List a minimal test set that satisfies all du-paths coverage with
respect to x. (Direct tours only.) If possible, use the given test
paths. If not, provide additional test paths to satisfy the criterion.

(a) Graph I


(b) 

du(1, 5, x): (1, 2, 3, 5), (1, 2, 3, 4, 5)

du(1, 6, x): (1, 2, 6)

du(5, 6, x): (5, 2, 6)

du(5, 5, x): (5, 2, 3, 4, 5), (5, 2, 3, 5)

(c) 

|Test Path|Du-path|
|:--------|:------|
|t1       |(1, 2, 6)|
|t2       |(1, 2, 3, 5), (1, 2, 3, 4, 5), (5, 2, 3, 5), (5, 2, 6)|
|t3       |(1, 2, 3, 5), (5, 2, 3, 5), (5, 2, 3, 4, 5), (5, 2, 6)|

(d)

|du         |du-path|covers|
|:----------|:------|:-----|
|du(1, 5, x)|(1, 2, 3, 5)|t3|
|           |(1, 2, 3, 4, 5)|t2|
|du(1, 6, x)|(1, 2, 6)|t1|
|du(5, 6, x)|(5, 2, 6)|t2&t3|
|du(5, 5, x)|(5, 2, 3, 5)|t2|
|           |(5, 2, 3, 4, 5)|t3|

(e) 

|du         |du-path|covers|
|:----------|:------|:-----|
|du(1, 5, x)|(1, 2, 3, 5)|t1|
|           |(1, 2, 3, 4, 5)|t3|
|du(1, 6, x)|(1, 2, 6)|t3|
|du(5, 6, x)|(5, 2, 6)|t1&t2|
|du(5, 5, x)|(5, 2, 3, 5)|t1|
|           |(5, 2, 3, 4, 5)|t2|