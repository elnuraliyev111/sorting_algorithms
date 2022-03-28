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


# Merge Sort

MERGE SORT: PYTHON
Testing the Sort
We’ve written our merge sort! The whole sort takes up two functions:

merge_sort() which is called recursively breaks down an input list to smaller, more manageable pieces. merge() which is a helper function built to help combine those broken-down lists into ordered combination lists.

merge_sort() continues to break down an input list until it only has one element and then it joins that with other single element lists to create sorted 2-element lists. Then it combines 2-element sorted lists into 4-element sorted lists. It continues that way until all the items of the lists are sorted!

Only one thing left to do, test it out!

Instructions
1.
In script.py we have placed three unordered lists: unordered_list1, unordered_list2, and unordered_list3.

Sort the three of them using merge_sort() and save them into the variables ordered_list1, ordered_list2 and ordered_list3.

Checkpoint 2 Passed
2.
Print out the ordered lists! How do they look?
