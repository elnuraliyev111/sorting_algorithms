# sorting_algorithms

# Bubble Search

Bubble Sort: Optimized
As you were writing Bubble Sort, you may have realized that we were doing some unnecessary iterations.

Consider the first pass through the outer loop. We’re making n-1 comparisons.

nums = [5, 4, 3, 2, 1]
# 5 element list: N is 5
bubble_sort(nums)
# 5 > 4
# [4, 5, 3, 2, 1]
# 5 > 3
# [4, 3, 5, 2, 1]
# 5 > 2
# [4, 3, 2, 5, 1]
# 5 > 1
# [4, 3, 2, 1, 5]
# four comparisons total
We know the last value in the list is in its correct position, so we never need to consider it again. The second time through the loop, we only need n-2 comparisons.

As we correctly place more values, fewer elements need to be compared. An optimized version doesn’t make n^2-n comparisons, it does (n-1) + (n-2) + ... + 2 + 1 comparisons, which can be simplified to (n^2-n) / 2 comparisons.

This is fewer than n^2-n comparisons but the algorithm still has a big O runtime of O(N^2).

As the input, N, grows larger, the division by two has less significance. Big O considers inputs as they reach infinity so the higher order term N^2 completely dominates.

We can’t make Bubble Sort better than O(N^2), but let’s take a look at the optimized code and compare iterations between implementations!

We’re also taking advantage of parallel assignment in Python and abstracting away the swap() function!

