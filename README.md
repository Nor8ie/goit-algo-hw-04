# goit-algo-hw-04 - Measuring the performance of the 3 sorting methods: Insertion Sorting, Merge Sorting and Timsort.

The assumptions used for testing the 3 algorithms (Insertion, Merge and Timsort) take into consideration a number
of 5 repetitions, each with 100 iterations per runtime.

The dataset generation code was included in the test_code section for all 3 methods to ensure that every single
iteration within each repeat generates a fresh dataset, leading to a more precise measurement.

1. Execution Time Comparison:
   Insertion Sort: 0.2895991000114009 seconds
   Merge Sort: 0.06126829993445426 seconds
   Timsort: 0.014927800046280026 seconds

2. Theoretical Complexity:
   Insertion Sort: O(n²)
   Insertion sort is simple but inefficient for large datasets. It performs well on small or nearly sorted datasets.

   Merge Sort: O(n log n)
   Merge sort is a divide-and-conquer algorithm with guaranteed O(n log n) performance.
   It is efficient for larger datasets but requires additional space for merging.

   Timsort: O(n log n)
   Timsort combines merge sort and insertion sort to optimize performance. It starts with insertion sort on small
   chunks (runs) and then merges them. This hybrid approach allows it to handle real-world data more efficiently,
   especially datasets with existing order.

3. Empirical Verification:
   The provided execution times empirically verify the theoretical complexity:
   Insertion Sort takes the longest time, which aligns with its O(n²) complexity.
   Merge Sort is significantly faster than insertion sort, consistent with its O(n log n) complexity.
   Timsort outperforms both, demonstrating the effectiveness of combining merge sort and insertion sort.

4. Effectiveness of Timsort:
   Timsort is the most efficient algorithm among the three for the given datasets. Its combination of insertion sort
   for small segments and merge sort for larger ones allows it to leverage the strengths of both algorithms.

   Insertion Sort is less efficient for larger datasets but might be useful for small or nearly sorted data.
   Merge Sort offers a consistent O(n log n) performance, but Timsort’s optimizations make it faster in practice.
   Conclusion:
   For the given case, Timsort is the most effective sorting algorithm. The empirical results support the theoretical
   estimates of the algorithms’ complexities. Timsort's design, which integrates insertion sort and merge sort, provides
   superior performance, especially for real-world data where existing order can be leveraged.

Summary:
Insertion Sort: Best for small or nearly sorted datasets.
Merge Sort: Reliable O(n log n) performance, suitable for large datasets.
Timsort: Superior overall performance, combining both insertion and merge sort, making it the most effective for diverse datasets.
