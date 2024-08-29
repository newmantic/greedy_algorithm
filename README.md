# greedy_algorithm

Greedy algorithms are a class of algorithms that make a series of choices, each of which looks best at the moment (locally optimal), with the hope that this will lead to a globally optimal solution. The greedy approach is often simple and efficient, but it only works for certain types of problems where local optimality leads to global optimality.


Greedy Choice Property:
A problem exhibits the greedy choice property if a globally optimal solution can be arrived at by making a locally optimal choice. This means that you can build the solution incrementally, choosing the best option at each step.

Greedy choice: Choose the best option available at each step.

Optimal Substructure:
A problem has an optimal substructure if an optimal solution to the problem contains optimal solutions to its subproblems. This is crucial for greedy algorithms because it ensures that solving subproblems optimally will help in solving the overall problem.
If S = optimal solution to problem P,
Then S can be composed of optimal solutions to subproblems P1, P2, ..., Pn.


Initialization:
Start with an empty solution.
Initialize the problem data (e.g., list of items, activities, etc.).

Selection:
At each step, make a greedy choice by selecting the option that seems best according to a certain criterion.
This criterion often involves sorting the data or choosing the maximum/minimum available value.

Feasibility Check:
After making each greedy choice, check if the current solution is still feasible. If not, discard the choice and possibly try another.

Repeat:
Repeat the selection and feasibility steps until the entire problem is solved or all options have been considered.

Solution Construction:
The final solution is constructed from the choices made at each step.


Example: You have a knapsack with a capacity W, and you are given n items, each with a weight w_i and a value v_i. The goal is to maximize the total value in the knapsack by selecting fractions of items if necessary.

Greedy Choice: Select items based on their value-to-weight ratio (v_i / w_i).
Optimal Substructure: The problem can be broken down into smaller subproblems where each subproblem involves solving the knapsack problem for a smaller capacity.
Algorithm Steps:

Sort: Sort the items by their value-to-weight ratio in descending order.
Sort items by v_i / w_i in descending order.

Select: Start selecting items in order, taking as much as possible of each item.
While the knapsack is not full:
    Take as much as possible of the item with the highest ratio.
    Reduce the remaining capacity of the knapsack.
    
Stop: Stop when the knapsack is full or all items have been considered.

The time complexity of a greedy algorithm typically depends on the sorting step, which is O(n log n) for n items, followed by a linear scan of the items, making the overall complexity O(n log n).


Example: the Activity Selection Problem, where you aim to select the maximum number of non-overlapping activities.

Greedy Choice: Always select the activity with the earliest finishing time.
Optimal Substructure: Once an activity is selected, the remaining problem is to select activities from those that start after the selected activity ends.

