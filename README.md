[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12577629&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  - Ignoring Lower order Terms: Asymtotic analysis focuses on the dominant term as the input sizes increases.
    Example - if an algerith has a time complexity of $\ 2n^2 + 3n + 1$

  - Algorithms may have different behaviors for best-case, average-case, and worst-case scenarios. Asymptotic analysis often focuses on the worst-case scenario, but in practice, the distribution of input data may lead to different average-case behavior.

   - Reason: Asymptotic analysis often focuses on the worst-case time complexity. While worst-case analysis provides an upper bound on the running time, it may not accurately represent the typical or average-case performance.
Example: Consider a sorting algorithm that is $\ O(n^2)$ in the worst case but performs much better $\ O(nlogn)$ on average due to optimizations for common input distributions. Asymptotic analysis might overlook these optimizations.


- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  - We know it takes 5 seconds to find a particular element in a BST with 1,000 elements in it.
  - Assuming the asymtotic complexity of the BST operation is $\ O(logn)$ , and the n represents the number of elements in the tree.
    
  - We can use the ratio of logarithms we can estimate the time it takes to fine that same elemant in a BST with 10,000 elements in it.

    Let $\ T_1$ be the time for 1,000 elements, and $\ T_2$ be the time for 10,000 elements. 
    Let $\ T_1 = 5$ seconds.

    - This gives us the ratio $\frac{log_2\left(10,000\right)}{log_2\left(1,000\right)}$.
   
    - Now we need to scale the runtime of $\ T_1$.
   
    - This gives us and estimate of $\ T_2 = 5 * \frac{log_2\left(10,000\right)}{log_2\left(1,000\right)}$.
   
    - So, using a calculator $\ T_2 = 5 * \frac{13.2877}{9.966} = 6.6665$ seconds.
    
    
- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  - The analysis gives a trend in the algorithms performance as the inpit size increases. The actual data being processed can
    significantly impact the actual runtime. So, if you have an input that is already sorted or nearly sort it might perform much
    faster than the expected average time.
  - The performance of the algorithm can be affected by the underlying hardware. Things such as memory limitations could cause slowdown
    for large inputs.
  - Inproper implementation of the algorithm could have significant affects on the runtime. Things like using certain programming
    languauges could have an impact on the runtime. 

Add your answers to this markdown file.

Reviewed repositories from theory-vs-practice-JamesOzzyburn, theory-vs-practice-Dhruv8806

Recieved help from the TA. 

Reviewed material from: 
https://stackoverflow.com/questions/41054981/what-is-the-time-complexity-of-searching-in-a-binary-search-tree-if-the-tree-is#:~:text=The%20Time%20complexity%20of%20a,similar%20to%20a%20linear%20search.

https://www.upgrad.com/blog/binary-search-algorithm/
