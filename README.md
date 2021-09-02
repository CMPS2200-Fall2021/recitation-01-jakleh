# CMPS 2200  Recitation 01

**Name (Team Member 1):** Jake Lehner  

- [Done!] 1. In `main.py`, the implementation of `linear_search` is already complete. Your task is to implement `binary_search`. Implement a recursive solution using the helper function `_binary_search`. 

- [Done!] 2. Test that your function is correct by calling from the command-line `pytest main.py::test_binary_search`

- [Done!] 3. Write at least two additional test cases in `test_binary_search` and confirm they pass.

- [Done!] 4. Describe the worst case input value of `key` for `linear_search`? for `binary_search`? 

**TODO: The worst-case input value for key for both search functions is a value that is not contained in the list. However, a near-worst-case key for binary search would be a number that is at either the very beginning or the very end of the list, whereas there is only one type of near-worst-case key for linear search (i.e., a number at the end of the list).**

- [Done!] 5. Describe the best case input value of `key` for `linear_search`? for `binary_search`? 

**The best case for binary search is a key that matches the number in the middle of the list (i.e., the number positioned at the index of (right + left) // 2), whereas the best case for linear search is a key that matches the number at the start of the list.**

- [Done!] 6. Complete the `time_search` function to compute the running time of a search function. Note that this is an example of a "higher order" function, since one of its parameters is another function.

- [Done!] 7. Complete the `compare_search` function to compare the running times of linear search and binary search. Confirm the implementation by running `pytest main.py::test_compare_search`, which contains some simple checks.

- [Done!] 8. Call `print_results(compare_search())` and paste the results here:

**TODO:[(10, 0.023193359375, 0.003173828125), (100, 0.0048828125, 0.005126953125)]**

- [Done!] 9. The theoretical worst-case running time of linear search is $O(n)$ and binary search is $O(log_2(n))$. Do these theoretical running times match your empirical results? Why or why not?

**TODO: No. If they did, then binary search would consistently take less time than linear search for large n. However, the opposite is true: Binary search consistently beats linear for n=10 [by a large margin] while they take turns for n=100.**

- [Done!] 10. Binary search assumes the input list is already sorted. Assume it takes $\Theta(n^2)$ time to sort a list of length $n$. Suppose you know ahead of time that you will search the same list $k$ times. 
  + What is worst-case complexity of searching a list of $n$ elements $k$ times using linear search? **TODO: O(n^2 + k * n)**
  + For binary search? **TODO: O(n^2 + k * log_2(n))**
  + For what values of $k$ is it more efficient to first sort and then use binary search versus just using linear search without sorting? **TODO: The values of k for which (n^2)/(n-log_2(n)) - k < 0. So, k must be greater than (n^2)/(n-log_2(n)).**
