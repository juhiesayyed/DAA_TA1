# DAA_TA1
Travelling Salesman Problem using Dynamic Programming in which sets of nodes are given and we have to find 
1) Best Distance
2) Best Time
3) And the combination of both

## Explanation:
In the traveling salesman Problem, a salesman must visits n cities. visiting each city exactly once and finishing at the city he starts from. There is a non-negative cost c (i, j) to travel from the city i to city j. The goal is to find a tour of minimum cost. We assume that every two cities are connected. Such problems are called Traveling-salesman problem (TSP).

There are two important things to be consider in this problem statement
<li> Visit every city exactly once</li>
<li>Cover the shortest path</li>

## What is the need of Dynamic Programming ?
If we look into the <b>brute force</b> approach for solving this problem, we can see that due to recursion call, a lot of cases are repeating themselves and that's the reason of a bigger runtime.
the time complexity is O(n!) and the space complexity is O(n^2).

By using dynamic programming we can save the repeated cases when they are calculated for the first time, and next time when we need the result we can directly use them from our storage(in terms of data structures).

##
Let us consider a graph G = (V, E), where V is a set of cities and E is a set of weighted edges. An edge e(u, v) represents that vertices u and v are connected. Distance between vertex u and v is d(u, v), which should be non-negative.<br>

Suppose we have started at city 1 and after visiting some cities now we are in city j. Hence, this is a partial tour. We certainly need to know j, since this will determine which cities are most convenient to visit next. We also need to know all the cities visited so far, so that we don't repeat any of them. Hence, this is an appropriate sub-problem.


## Test Case-1

```
double[][][] matrix = 
{{ { 0, 0 }, { 9, 15 }, { 4, 3 }, { 7, 9 }},
{{ 7, 7 }, { 0, 0 }, { 3, 2 }, { 2, 1.5 }},
{{ 10, 8.3 }, { 6, 8 }, { 0, 0 }, { 9, 16 }},
{{ 12, 10.2 }, { 15, 11 }, { 6, 16 }, { 0, 0 }}};
```


![image](https://user-images.githubusercontent.com/86836506/194308192-ceda1c9c-f0a1-4d1a-b8db-a4f866143aa3.png)


## Test Case-2
```
double[][][] matrix =
{ { { 0, 0 }, { 2, 12 }, { 15, 6 }, { 13, 10 } },
{ { 12, 8 }, { 0, 0 }, { 4, 3 }, { 16, 7} },
{ { 16, 5 }, { 8, 20 }, { 0, 0 }, { 7, 4 } },
{ { 18, 15 }, { 6, 13 }, { 22, 17 }, { 0, 0 } } };
```
![image](https://user-images.githubusercontent.com/86836506/194312078-38d37247-02fc-4620-ac35-9b318ae91f9c.png)


