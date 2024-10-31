# Lab 1 - Set cover problem

## Repository overview
The official notebook is [tsp.ipynb](tsp.ipynb).

## Official solution
The official solution has the following characteristics:
- **single mutation tweak**: a multiple mutation could be more suitable, but it would prevent to speed up the algorithm;
- **data structure** (called *covering* in the tweak function) keeping track of the number of collected sets each element is covered by: in this way, the algorithm is sped up since the computation of the cost is performed only in the universe dimension;
- **heuristic** to avoid the algorithm searching invalid solutions: given a negative tweak (a set is removed by the current solution), if an element results to be uncovered by the current solution, the modification is rolled back, blocking the path of the algorithm in that region of the fitness landscape;
- **random start**: since the cost is computed using the coverage of the universe by the sets collected in the current solution, the algorithm can start from a random solution, without any specific constraint.

It also contains a code snippet with a **greedy optimization** algorithm, which is able to find an approximate solution of the problem, with a factor proportional to *log(n)* with respect to the optimal one, where *n* is the size of the universe. It is possible to check the results by simply running the notebook.

## Collaborations
The following parts:
- tweak function
- snippet of code for plotting history

have been done in collaboration with [Vincenzo Avantaggiato](https://github.com/VincenzoAvantaggiato). 

## Results
The results are summarized in the following table:

|Instance name|Greedy cost|Greedy calls|EA cost|EA calls|
|:-----:|:--:  |:--: |:--:|:--: |
|Vanuatu|100   |10   |0.2 |20   |
|Italy  |1000  |100  |0.2 |115  |
|Russia |10000 |1000 |0.2 |4889 |
|US     |100000|10000|0.1 |51355|
|China  |100000|10000|0.2 |59199|

**Notes**: the columns:
-  *Greedy/EA calls*: displays the number of steps necessary to the algorithm to find the (local) optimal solution;
-  *Greedy/EA cost*: displays the cost of the solution found, as absolute value (opposite of fitness, conceptually).