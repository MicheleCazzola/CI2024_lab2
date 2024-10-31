# Lab 2 - Travel Salesman Problem (TSP)

## Repository overview
The official notebook is [tsp.ipynb](tsp.ipynb).

## Official solution


## Collaborations
The following parts:
- dvhsfvridf

have been done in collaboration with [Vincenzo Avantaggiato](https://github.com/VincenzoAvantaggiato). 

## Results
The results are summarized in the following table:

|Instance name  |Greedy cost    |Greedy calls|EA cost|EA calls|Best result|
|:-----:        |:--:           |:--: |:--:|:--: |:--:|
|Vanuatu        |1475.528       |8  |1345.545 |2   |1345.54|
|Italy          |4436.032       |46  |4209.181 |193  |4172.76|
|Russia         |40051.587      |167 |33648.848 |1012 |32722.5|
|US             |46244.333      |326|40599.885 |1983|39016.62|
|China          |62116.045      |1|52910.648 |4796|None|

**Notes**: the columns:
-  *Greedy/EA calls*: displays the number of generations necessary to the algorithm to find the (local) optimal solution;
-  *Greedy/EA cost*: displays the cost of the solution found, as absolute value (opposite of fitness, conceptually).