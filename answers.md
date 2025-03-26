# CMPS 2200 Reciation 5
## Answers

**Name:**____Noelle and Mohini_______


Place all written answers from `recitation-05.md` here for easier grading.


|      n |   qsort-fixed-pivot |   qsort-random-pivot |
|--------|---------------------|----------------------|
|    100 |               0.076 |                0.103 |
|    200 |               0.164 |                0.226 |
|    500 |               0.542 |                0.601 |
|   1000 |               1.008 |                1.258 |
|   2000 |               2.433 |                2.744 |
|   5000 |               5.723 |                8.967 |
|  10000 |              13.391 |               17.914 |
|  20000 |              28.606 |               33.900 |
|  50000 |              77.983 |               92.519 |
| 100000 |             170.614 |              198.042 |




- **We are comparing the running times of two variants of Quicksort and selection sort. The comparesort function gives different benchmarks of each algorithm based on input lists which have various sizes. Selection sort has a best case running time of O(n^2) and a worst case sorting time of O(n^2). Quicksort with a fixed pivot has a best case running time of O(n log n) and a worst case running time of O(n^2). Quicksort with random pivot, additionally, has a best case running time of O(n log n) and a worst case running time of o(n^2). We found that for selection sort, it follows its quadratic asosymptatic bounds very closely, for smaller values of n, it works fine, but for larger values of n, the runtime increases very quickly. This trend does not differ when analyzing the sorting type- whether or not it is random or sorted. For quicksort with random pivot, it also matches the behavior of its expected asymototamtic bounds, it works efficiently for both random and sorted inputs, which matches its average case, O(n log n) behavior very well. Finally, for the Quicksort with a fixed pivot, we found that it performed well on random inputs, however on a sorted input the performance time typically downgrades significantly because it tends to select the first element which can make the algorithm unbalanced. **


|      n |   qsort-fixed-pivot |   qsort-random-pivot |   tim_sort |
|--------|---------------------|----------------------|------------|
|    100 |               0.083 |                0.109 |      0.009 |
|    200 |               0.162 |                0.203 |      0.013 |
|    500 |               0.613 |                0.596 |      0.041 |
|   1000 |               1.079 |                1.282 |      0.087 |
|   2000 |               2.106 |                2.670 |      0.179 |
|   5000 |               6.160 |                7.382 |      0.526 |
|  10000 |              12.420 |               20.739 |      1.534 |
|  20000 |              26.455 |               30.750 |      2.672 |
|  50000 |              76.171 |               88.683 |      6.999 |
| 100000 |             158.684 |              183.809 |     15.207 |


- **While the random-pivot Quicksort was performing well on a random set of data, the python's built-in sorted function does outperform it, significantly in inputs which are already sorted. Timsort is built specifically to use a pre-existing data structure which allows it to implement better when compared to random-pivot Quicksort. Timsort is faster on sorted or nearly sorted data and also has delivered more consistency within edge cases, however quicksort is slower on sorted data because it is unable to detect order.  **
