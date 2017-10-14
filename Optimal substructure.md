## Optimal substructure

* In computer science, a problem is said to have optimal substructure if an optimal solution can be constructed from optimal solutions of its subproblems.

* This property is used to determine the usefulness of dynamic programming and greedy algorithms for a problem.

<p style="text-align: center;"><img src="https://user-images.githubusercontent.com/20622980/31573738-772f9a72-b0df-11e7-900e-79d2ff73a979.png"></p>

### Example

 *Consider finding a shortest path for travelling between two cities by car, as illustrated in Figure 1. Such an example is likely to exhibit optimal substructure. That is, if the shortest route from Seattle to Los Angeles passes through Portland and then Sacramento, then the shortest route from Portland to Los Angeles must pass through Sacramento too. That is, the problem of how to get from Portland to Los Angeles is nested inside the problem of how to get from Seattle to Los Angeles. (The wavy lines in the graph represent solutions to the subproblems.)*

  *As an example of a problem that is unlikely to exhibit optimal substructure, consider the problem of finding the cheapest airline ticket from Buenos Aires to Kyiv. Even if that ticket involves stops in Miami and then London, we can't conclude that the cheapest ticket from Miami to Kyiv stops in London, because the price at which an airline sells a multi-flight trip is usually not the sum of the prices at which it would sell the individual flights in the trip.*
  
### Definition

  *A slightly more formal definition of optimal substructure can be given. Let a "problem" be a collection of "alternatives", and let each alternative have an associated cost, c(a). The task is to find a set of alternatives that minimizes c(a). Suppose that the alternatives can be partitioned into subsets, i.e. each alternative belongs to only one subset. Suppose each subset has its own cost function. The minima of each of these cost functions can be found, as can the minima of the global cost function, restricted to the same subsets. If these minima match for each subset, then it's almost obvious that a global minimum can be picked not out of the full set of alternatives, but out of only the set that consists of the minima of the smaller, local cost functions we have defined. If minimizing the local functions is a problem of "lower order", and (specifically) if, after a finite number of these reductions, the problem becomes trivial, then the problem has an optimal substructure.*  

### Problems with optimal substructure
1. [Longest common subsequence problem](https://en.wikipedia.org/wiki/Longest_common_subsequence_problem)
2. [Longest increasing subsequence](https://en.wikipedia.org/wiki/Longest_increasing_subsequence)
3. [Longest palindromic substring](https://en.wikipedia.org/wiki/Longest_palindromic_substring)
4. [All-Pairs Shortest Path](https://en.wikipedia.org/wiki/Shortest_path_problem#All-pairs_shortest_paths)
5. Any problem that can be solved by [dynamic programming](https://en.wikipedia.org/wiki/Dynamic_programming).

### Problems without optimal substructure
1. [Longest path problem](https://en.wikipedia.org/wiki/Longest_path_problem)
2. **Least-cost airline fare.** (Using on online flight search, we will frequently find that the cheapest flight from airport A to airport B involves a single connection through airport C, but the cheapest flight from airport A to airport C involves a connection through some other airport D.)

***Article from :*** [Optimal substructure](https://en.wikipedia.org/wiki/Optimal_substructure)
