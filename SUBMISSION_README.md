# Sorting Algorithms Benchmarking - Submission Guide

This package contains the source code and benchmarking tools used for the CS-253 Practical Assignment.

## Project Structure
- `sorting_algorithms/`: C implementations of all 7 sorting algorithms and Quick Sort variants.
- `benchmark.py`: The main Python script that automates compilation, execution, and data analysis.
- `generate_test_data.py`: Script used to generate the random, sorted, and reverse-sorted datasets.
- `test_data/`: Directory containing the pre-generated input files.
- `graphs/`: (Generated after running) Contains the CSV results and visualization plots.

## Prerequisites
- **C Compiler**: `gcc` (MinGW for Windows or standard GCC for Linux/macOS).
- **Python 3.x**: With the following libraries installed:
  ```bash
  pip install matplotlib pandas numpy scipy
  ```

## How to Run the Benchmarks
1. **Navigate to the project directory**:
   ```bash
   cd Sorting-algorithms-benchmark
   ```
2. **Generate Test Data** (Optional, if not already present):
   ```bash
   python generate_test_data.py
   ```
3. **Run the Benchmark**:
   ```bash
   python benchmark.py
   ```
   *Note: The script will automatically compile the C files into an `executables/` folder and run them against the data in `test_data/`.*

4. **View Results**:
   - Numerical data will be saved in `graphs/csv_data/`.
   - Visualization plots will be available in `graphs/7_sorting_algo_comparisons/` and `graphs/quick_sort_analysis/`.

## Authors
- Srikara Nikhil (241CS158)
- Anikethana Rudresh (241CS108)

---

### Terminal Output

```
PS C:\Users\nikhi\OneDrive\Documents\Desktop\sorting-algorithms-benchmark> python .\benchmark.py
Compiling sorting_algorithms\bubble_sort.c...
Successfully compiled sorting_algorithms\bubble_sort.c to executables\bubble_sort
Compiling sorting_algorithms\heap_sort.c...
Successfully compiled sorting_algorithms\heap_sort.c to executables\heap_sort
Compiling sorting_algorithms\insertion_sort.c...
Successfully compiled sorting_algorithms\insertion_sort.c to executables\insertion_sort
Compiling sorting_algorithms\merge_sort.c...
Successfully compiled sorting_algorithms\merge_sort.c to executables\merge_sort
Compiling sorting_algorithms\quick_sort_median_of_three_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_median_of_three_pivot.c to executables\quick_sort_median_of_three_pivot
Compiling sorting_algorithms\radix_sort.c...
Successfully compiled sorting_algorithms\radix_sort.c to executables\radix_sort
Compiling sorting_algorithms\selection_sort.c...
Successfully compiled sorting_algorithms\selection_sort.c to executables\selection_sort
Compiling sorting_algorithms\quick_sort_first_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_first_pivot.c to executables\quick_sort_first_pivot
Compiling sorting_algorithms\quick_sort_median_of_three_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_median_of_three_pivot.c to executables\quick_sort_median_of_three_pivot
Compiling sorting_algorithms\quick_sort_random_pivot.c...
Successfully compiled sorting_algorithms\quick_sort_random_pivot.c to executables\quick_sort_random_pivot

Starting benchmarking...
Benchmarking N=100, Type=random...
  bubble_sort: Time = 0.000000 s, Comparisons = 4947
  heap_sort: Time = 0.000000 s, Comparisons = 1021
  insertion_sort: Time = 0.000000 s, Comparisons = 2586
  merge_sort: Time = 0.000000 s, Comparisons = 541
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 709
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 701
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 709
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 680
Benchmarking N=100, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4950
  heap_sort: Time = 0.000000 s, Comparisons = 944
  insertion_sort: Time = 0.000000 s, Comparisons = 4950
  merge_sort: Time = 0.000000 s, Comparisons = 316
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 620
Benchmarking N=100, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99
  heap_sort: Time = 0.000000 s, Comparisons = 1081
  insertion_sort: Time = 0.000000 s, Comparisons = 99
  merge_sort: Time = 0.000000 s, Comparisons = 356
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 594
Benchmarking N=500, Type=random...
  bubble_sort: Time = 0.000286 s, Comparisons = 124222
  heap_sort: Time = 0.000000 s, Comparisons = 7423
  insertion_sort: Time = 0.000000 s, Comparisons = 64428
  merge_sort: Time = 0.000000 s, Comparisons = 3867
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5060
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 5211
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5060
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4754
Benchmarking N=500, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 124750
  heap_sort: Time = 0.000000 s, Comparisons = 7010
  insertion_sort: Time = 0.000143 s, Comparisons = 124750
  merge_sort: Time = 0.000000 s, Comparisons = 2216
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000286 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4710
Benchmarking N=500, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 499
  heap_sort: Time = 0.000000 s, Comparisons = 7756
  insertion_sort: Time = 0.000000 s, Comparisons = 499
  merge_sort: Time = 0.000143 s, Comparisons = 2272
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000143 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 5124
Benchmarking N=1000, Type=random...
  bubble_sort: Time = 0.001000 s, Comparisons = 498275
  heap_sort: Time = 0.000000 s, Comparisons = 16854
  insertion_sort: Time = 0.000286 s, Comparisons = 245329
  merge_sort: Time = 0.000000 s, Comparisons = 8688
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11364
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000143 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 10830
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11364
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10490
Benchmarking N=1000, Type=reverse_sorted...
  bubble_sort: Time = 0.001000 s, Comparisons = 499500
  heap_sort: Time = 0.000286 s, Comparisons = 15965
  insertion_sort: Time = 0.000286 s, Comparisons = 499500
  merge_sort: Time = 0.000000 s, Comparisons = 4932
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  radix_sort: Time = 0.000143 s, Comparisons = 999
  selection_sort: Time = 0.000143 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000429 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 10786
Benchmarking N=1000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 999
  heap_sort: Time = 0.000000 s, Comparisons = 17583
  insertion_sort: Time = 0.000000 s, Comparisons = 999
  merge_sort: Time = 0.000000 s, Comparisons = 5044
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 9520
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000000 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000143 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 10142
Benchmarking N=5000, Type=random...
  bubble_sort: Time = 0.026143 s, Comparisons = 12492247
  heap_sort: Time = 0.000571 s, Comparisons = 107688
  insertion_sort: Time = 0.008857 s, Comparisons = 6258733
  merge_sort: Time = 0.001143 s, Comparisons = 55219
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 70510
  radix_sort: Time = 0.000571 s, Comparisons = 4999
  selection_sort: Time = 0.011429 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.000571 s, Comparisons = 75096
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 70510
  quick_sort_random_pivot: Time = 0.000571 s, Comparisons = 69575
Benchmarking N=5000, Type=reverse_sorted...
  bubble_sort: Time = 0.029000 s, Comparisons = 12497500
  heap_sort: Time = 0.000571 s, Comparisons = 103227
  insertion_sort: Time = 0.016714 s, Comparisons = 12497500
  merge_sort: Time = 0.001000 s, Comparisons = 29804
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  radix_sort: Time = 0.000143 s, Comparisons = 4999
  selection_sort: Time = 0.011571 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.020000 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  quick_sort_random_pivot: Time = 0.000286 s, Comparisons = 74709
Benchmarking N=5000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4999
  heap_sort: Time = 0.000429 s, Comparisons = 112126
  insertion_sort: Time = 0.000000 s, Comparisons = 4999
  merge_sort: Time = 0.000571 s, Comparisons = 32004
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.011286 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.008857 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 60678
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 74092
Benchmarking N=10000, Type=random...
  bubble_sort: Time = 0.130429 s, Comparisons = 49994724
  heap_sort: Time = 0.001286 s, Comparisons = 235469
  insertion_sort: Time = 0.031571 s, Comparisons = 24732511
  merge_sort: Time = 0.002429 s, Comparisons = 120440
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 155985
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.045143 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.000286 s, Comparisons = 160166
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 155985
  quick_sort_random_pivot: Time = 0.000857 s, Comparisons = 154889
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.112714 s, Comparisons = 49995000
  heap_sort: Time = 0.001000 s, Comparisons = 226682
  insertion_sort: Time = 0.064143 s, Comparisons = 49995000
  merge_sort: Time = 0.001143 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  radix_sort: Time = 0.000571 s, Comparisons = 9999
  selection_sort: Time = 0.046000 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.083857 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.000286 s, Comparisons = 147826
Benchmarking N=10000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 9999
  heap_sort: Time = 0.001143 s, Comparisons = 244460
  insertion_sort: Time = 0.000143 s, Comparisons = 9999
  merge_sort: Time = 0.002000 s, Comparisons = 69008
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 131343
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.045857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.036571 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000429 s, Comparisons = 131343
  quick_sort_random_pivot: Time = 0.000286 s, Comparisons = 153466
Benchmarking N=25000, Type=random...
  bubble_sort: Time = 1.037429 s, Comparisons = 312474297
  heap_sort: Time = 0.003857 s, Comparisons = 654825
  insertion_sort: Time = 0.200714 s, Comparisons = 156820214
  merge_sort: Time = 0.004857 s, Comparisons = 334319
  quick_sort_median_of_three_pivot: Time = 0.002000 s, Comparisons = 414903
  radix_sort: Time = 0.000429 s, Comparisons = 24999
  selection_sort: Time = 0.294286 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.002143 s, Comparisons = 445028
  quick_sort_median_of_three_pivot: Time = 0.002286 s, Comparisons = 414903
  quick_sort_random_pivot: Time = 0.002143 s, Comparisons = 414049
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 0.755143 s, Comparisons = 312487500
  heap_sort: Time = 0.004000 s, Comparisons = 633719
  insertion_sort: Time = 0.415429 s, Comparisons = 312487500
  merge_sort: Time = 0.003857 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.001571 s, Comparisons = 660758
  radix_sort: Time = 0.001143 s, Comparisons = 24999
  selection_sort: Time = 0.301000 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.549714 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.001429 s, Comparisons = 452786
Benchmarking N=25000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 24999
  heap_sort: Time = 0.003000 s, Comparisons = 677688
  insertion_sort: Time = 0.000286 s, Comparisons = 24999
  merge_sort: Time = 0.004000 s, Comparisons = 188476
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 366397
  radix_sort: Time = 0.000429 s, Comparisons = 24999
  selection_sort: Time = 0.295857 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.259286 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 366397
  quick_sort_random_pivot: Time = 0.001429 s, Comparisons = 470501
Benchmarking N=50000, Type=random...
  bubble_sort: Time = 4.536000 s, Comparisons = 1249952845
  heap_sort: Time = 0.009000 s, Comparisons = 1409656
  insertion_sort: Time = 0.843714 s, Comparisons = 626019787
  merge_sort: Time = 0.011000 s, Comparisons = 718076
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 886476
  radix_sort: Time = 0.001571 s, Comparisons = 49999
  selection_sort: Time = 1.208429 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.004286 s, Comparisons = 907299
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 886476
  quick_sort_random_pivot: Time = 0.004571 s, Comparisons = 916108
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 2.995571 s, Comparisons = 1249975000
  heap_sort: Time = 0.006143 s, Comparisons = 1366047
  insertion_sort: Time = 1.622714 s, Comparisons = 1249975000
  merge_sort: Time = 0.006857 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  radix_sort: Time = 0.001571 s, Comparisons = 49999
  selection_sort: Time = 1.190857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 2.246429 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002714 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.002571 s, Comparisons = 930143
Benchmarking N=50000, Type=sorted...
  bubble_sort: Time = 0.000286 s, Comparisons = 49999
  heap_sort: Time = 0.007429 s, Comparisons = 1455438
  insertion_sort: Time = 0.000143 s, Comparisons = 49999
  merge_sort: Time = 0.006714 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 782782
  radix_sort: Time = 0.001429 s, Comparisons = 49999
  selection_sort: Time = 1.165571 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 1.077857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.001857 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.002571 s, Comparisons = 901560
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 10.747000 s, Comparisons = 2812436165
  heap_sort: Time = 0.014000 s, Comparisons = 2199901
  insertion_sort: Time = 1.898429 s, Comparisons = 1408462710
  merge_sort: Time = 0.016143 s, Comparisons = 1121269
  quick_sort_median_of_three_pivot: Time = 0.007286 s, Comparisons = 1414347
  radix_sort: Time = 0.003143 s, Comparisons = 74999
  selection_sort: Time = 2.739571 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 0.006857 s, Comparisons = 1478697
  quick_sort_median_of_three_pivot: Time = 0.006714 s, Comparisons = 1414347
  quick_sort_random_pivot: Time = 0.007286 s, Comparisons = 1430202
Benchmarking N=75000, Type=reverse_sorted...
  bubble_sort: Time = 6.675714 s, Comparisons = 2812462500
  heap_sort: Time = 0.010286 s, Comparisons = 2138650
  insertion_sort: Time = 3.787429 s, Comparisons = 2812462500
  merge_sort: Time = 0.010571 s, Comparisons = 594612
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 2272487
  radix_sort: Time = 0.002286 s, Comparisons = 74999
  selection_sort: Time = 2.674429 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 5.310143 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 2272487
  quick_sort_random_pivot: Time = 0.004143 s, Comparisons = 1411439
Benchmarking N=75000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 74999
  heap_sort: Time = 0.011143 s, Comparisons = 2268087
  insertion_sort: Time = 0.000286 s, Comparisons = 74999
  merge_sort: Time = 0.010571 s, Comparisons = 624316
  quick_sort_median_of_three_pivot: Time = 0.002571 s, Comparisons = 1195642
  radix_sort: Time = 0.002857 s, Comparisons = 74999
  selection_sort: Time = 2.616286 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 2.374857 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.002429 s, Comparisons = 1195642
  quick_sort_random_pivot: Time = 0.003714 s, Comparisons = 1450907
Benchmarking N=100000, Type=random...
  bubble_sort: Time = 19.864714 s, Comparisons = 4999817130
  heap_sort: Time = 0.019857 s, Comparisons = 3019257
  insertion_sort: Time = 3.362429 s, Comparisons = 2496007172
  merge_sort: Time = 0.022857 s, Comparisons = 1536758
  quick_sort_median_of_three_pivot: Time = 0.009429 s, Comparisons = 1889583
  radix_sort: Time = 0.003857 s, Comparisons = 99999
  selection_sort: Time = 4.869857 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 0.009429 s, Comparisons = 1978523
  quick_sort_median_of_three_pivot: Time = 0.009571 s, Comparisons = 1889583
  quick_sort_random_pivot: Time = 0.009714 s, Comparisons = 2252882
Benchmarking N=100000, Type=reverse_sorted...
  bubble_sort: Time = 12.020143 s, Comparisons = 4999950000
  heap_sort: Time = 0.014143 s, Comparisons = 2926640
  insertion_sort: Time = 6.714714 s, Comparisons = 4999950000
  merge_sort: Time = 0.015714 s, Comparisons = 815024
  quick_sort_median_of_three_pivot: Time = 0.006429 s, Comparisons = 3107283
  radix_sort: Time = 0.003429 s, Comparisons = 99999
  selection_sort: Time = 4.964143 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 9.024571 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.006571 s, Comparisons = 3107283
  quick_sort_random_pivot: Time = 0.005571 s, Comparisons = 2025594
Benchmarking N=100000, Type=sorted...
  bubble_sort: Time = 0.000286 s, Comparisons = 99999
  heap_sort: Time = 0.014429 s, Comparisons = 3112517
  insertion_sort: Time = 0.000286 s, Comparisons = 99999
  merge_sort: Time = 0.014857 s, Comparisons = 853904
  quick_sort_median_of_three_pivot: Time = 0.003429 s, Comparisons = 1665551
  radix_sort: Time = 0.003143 s, Comparisons = 99999
  selection_sort: Time = 4.556429 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 4.108429 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.003429 s, Comparisons = 1665551
  quick_sort_random_pivot: Time = 0.005286 s, Comparisons = 2075979

Benchmarking complete. Generating plots...
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_time.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_time_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_average_case_(random_input)_case_comparisons_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons_log_scale.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_comparisons.png
Generated plot: graphs\7_sorting_algo_comparisons\sorting_algorithms_best_case_(sorted_input)_case_comparisons_log_scale.png
Generated correlation plot: graphs\7_sorting_algo_comparisons\time_vs_comparisons_correlation.png

Generating QuickSort variant plots...
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_time.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_time_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_average_case_(random_input)_case_comparisons_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_worst_case_(reverse_sorted_input)_case_comparisons_log_scale.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_comparisons.png
Generated plot: graphs\quick_sort_analysis\sorting_algorithms_best_case_(sorted_input)_case_comparisons_log_scale.png
Generated correlation plot: graphs\quick_sort_analysis\time_vs_comparisons_correlation.png

All plots generated successfully.
Results are in the 'graphs' directory.
  - 7 sorting algorithm comparisons: 'graphs\7_sorting_algo_comparisons'
  - Quick sort analysis: 'graphs\quick_sort_analysis'
  - CSV data: 'graphs\csv_data'

--- Benchmarking Methodology ---
Each experiment was repeated 7 times, and the average execution time is reported.
Timing mechanism: C's `clock()` function from <time.h> is used to measure algorithm execution time.
Comparison counting: Instrumented C code tracks all element comparisons.
Input selection: Pre-generated test data from the 'test_data/' directory was used.
Same inputs were used for all sorting algorithms to ensure a fair comparison.

Note on Best/Worst Case Definitions:
  - Average Case: Represented by 'random' input data.
  - Worst Case: Represented by 'reverse_sorted' input data.
  - Best Case: Represented by 'sorted' input data.

Correlation Analysis:
  The correlation plots show the relationship between the number of comparisons
  and execution time. A high correlation (close to 1.0) indicates that comparisons
  are a strong predictor of execution time for that algorithm.

--- Benchmarking Results Table ---
                   Algorithm     Input Type  Input Size (N) Average Time (s) Average Comparisons
                 Bubble Sort         Random             100         0.000000                4947
                   Heap Sort         Random             100         0.000000                1021
              Insertion Sort         Random             100         0.000000                2586
                  Merge Sort         Random             100         0.000000                 541
Quick Sort (Median of Three)         Random             100         0.000000                 709
                  Radix Sort         Random             100         0.000000                  99
              Selection Sort         Random             100         0.000000                4950
                 Bubble Sort Reverse Sorted             100         0.000000                4950
                   Heap Sort Reverse Sorted             100         0.000000                 944
              Insertion Sort Reverse Sorted             100         0.000000                4950
                  Merge Sort Reverse Sorted             100         0.000000                 316
Quick Sort (Median of Three) Reverse Sorted             100         0.000000                 868
                  Radix Sort Reverse Sorted             100         0.000000                  99
              Selection Sort Reverse Sorted             100         0.000000                4950
                 Bubble Sort         Sorted             100         0.000000                  99
                   Heap Sort         Sorted             100         0.000000                1081
              Insertion Sort         Sorted             100         0.000000                  99
                  Merge Sort         Sorted             100         0.000000                 356
Quick Sort (Median of Three)         Sorted             100         0.000000                 669
                  Radix Sort         Sorted             100         0.000000                  99
              Selection Sort         Sorted             100         0.000000                4950
                 Bubble Sort         Random             500         0.000286              124222
                   Heap Sort         Random             500         0.000000                7423
              Insertion Sort         Random             500         0.000000               64428
                  Merge Sort         Random             500         0.000000                3867
Quick Sort (Median of Three)         Random             500         0.000000                5060
                  Radix Sort         Random             500         0.000000                 499
              Selection Sort         Random             500         0.000000              124750
                 Bubble Sort Reverse Sorted             500         0.000000              124750
                   Heap Sort Reverse Sorted             500         0.000000                7010
              Insertion Sort Reverse Sorted             500         0.000143              124750
                  Merge Sort Reverse Sorted             500         0.000000                2216
Quick Sort (Median of Three) Reverse Sorted             500         0.000000                6790
                  Radix Sort Reverse Sorted             500         0.000000                 499
              Selection Sort Reverse Sorted             500         0.000286              124750
                 Bubble Sort         Sorted             500         0.000000                 499
                   Heap Sort         Sorted             500         0.000000                7756
              Insertion Sort         Sorted             500         0.000000                 499
                  Merge Sort         Sorted             500         0.000143                2272
Quick Sort (Median of Three)         Sorted             500         0.000000                4263
                  Radix Sort         Sorted             500         0.000000                 499
              Selection Sort         Sorted             500         0.000143              124750
                 Bubble Sort         Random            1000         0.001000              498275
                   Heap Sort         Random            1000         0.000000               16854
              Insertion Sort         Random            1000         0.000286              245329
                  Merge Sort         Random            1000         0.000000                8688
Quick Sort (Median of Three)         Random            1000         0.000000               11364
                  Radix Sort         Random            1000         0.000000                 999
              Selection Sort         Random            1000         0.000143              499500
                 Bubble Sort Reverse Sorted            1000         0.001000              499500
                   Heap Sort Reverse Sorted            1000         0.000286               15965
              Insertion Sort Reverse Sorted            1000         0.000286              499500
                  Merge Sort Reverse Sorted            1000         0.000000                4932
Quick Sort (Median of Three) Reverse Sorted            1000         0.000000               15849
                  Radix Sort Reverse Sorted            1000         0.000143                 999
              Selection Sort Reverse Sorted            1000         0.000143              499500
                 Bubble Sort         Sorted            1000         0.000000                 999
                   Heap Sort         Sorted            1000         0.000000               17583
              Insertion Sort         Sorted            1000         0.000000                 999
                  Merge Sort         Sorted            1000         0.000000                5044
Quick Sort (Median of Three)         Sorted            1000         0.000143                9520
                  Radix Sort         Sorted            1000         0.000000                 999
              Selection Sort         Sorted            1000         0.000000              499500
                 Bubble Sort         Random            5000         0.026143            12492247
                   Heap Sort         Random            5000         0.000571              107688
              Insertion Sort         Random            5000         0.008857             6258733
                  Merge Sort         Random            5000         0.001143               55219
Quick Sort (Median of Three)         Random            5000         0.000714               70510
                  Radix Sort         Random            5000         0.000571                4999
              Selection Sort         Random            5000         0.011429            12497500
                 Bubble Sort Reverse Sorted            5000         0.029000            12497500
                   Heap Sort Reverse Sorted            5000         0.000571              103227
              Insertion Sort Reverse Sorted            5000         0.016714            12497500
                  Merge Sort Reverse Sorted            5000         0.001000               29804
Quick Sort (Median of Three) Reverse Sorted            5000         0.000000              106182
                  Radix Sort Reverse Sorted            5000         0.000143                4999
              Selection Sort Reverse Sorted            5000         0.011571            12497500
                 Bubble Sort         Sorted            5000         0.000000                4999
                   Heap Sort         Sorted            5000         0.000429              112126
              Insertion Sort         Sorted            5000         0.000000                4999
                  Merge Sort         Sorted            5000         0.000571               32004
Quick Sort (Median of Three)         Sorted            5000         0.000000               60678
                  Radix Sort         Sorted            5000         0.000000                4999
              Selection Sort         Sorted            5000         0.011286            12497500
                 Bubble Sort         Random           10000         0.130429            49994724
                   Heap Sort         Random           10000         0.001286              235469
              Insertion Sort         Random           10000         0.031571            24732511
                  Merge Sort         Random           10000         0.002429              120440
Quick Sort (Median of Three)         Random           10000         0.000714              155985
                  Radix Sort         Random           10000         0.000429                9999
              Selection Sort         Random           10000         0.045143            49995000
                 Bubble Sort Reverse Sorted           10000         0.112714            49995000
                   Heap Sort Reverse Sorted           10000         0.001000              226682
              Insertion Sort Reverse Sorted           10000         0.064143            49995000
                  Merge Sort Reverse Sorted           10000         0.001143               64608
Quick Sort (Median of Three) Reverse Sorted           10000         0.000571              234923
                  Radix Sort Reverse Sorted           10000         0.000571                9999
              Selection Sort Reverse Sorted           10000         0.046000            49995000
                 Bubble Sort         Sorted           10000         0.000000                9999
                   Heap Sort         Sorted           10000         0.001143              244460
              Insertion Sort         Sorted           10000         0.000143                9999
                  Merge Sort         Sorted           10000         0.002000               69008
Quick Sort (Median of Three)         Sorted           10000         0.000143              131343
                  Radix Sort         Sorted           10000         0.000429                9999
              Selection Sort         Sorted           10000         0.045857            49995000
                 Bubble Sort         Random           25000         1.037429           312474297
                   Heap Sort         Random           25000         0.003857              654825
              Insertion Sort         Random           25000         0.200714           156820214
                  Merge Sort         Random           25000         0.004857              334319
Quick Sort (Median of Three)         Random           25000         0.002000              414903
                  Radix Sort         Random           25000         0.000429               24999
              Selection Sort         Random           25000         0.294286           312487500
                 Bubble Sort Reverse Sorted           25000         0.755143           312487500
                   Heap Sort Reverse Sorted           25000         0.004000              633719
              Insertion Sort Reverse Sorted           25000         0.415429           312487500
                  Merge Sort Reverse Sorted           25000         0.003857              178756
Quick Sort (Median of Three) Reverse Sorted           25000         0.001571              660758
                  Radix Sort Reverse Sorted           25000         0.001143               24999
              Selection Sort Reverse Sorted           25000         0.301000           312487500
                 Bubble Sort         Sorted           25000         0.000000               24999
                   Heap Sort         Sorted           25000         0.003000              677688
              Insertion Sort         Sorted           25000         0.000286               24999
                  Merge Sort         Sorted           25000         0.004000              188476
Quick Sort (Median of Three)         Sorted           25000         0.000714              366397
                  Radix Sort         Sorted           25000         0.000429               24999
              Selection Sort         Sorted           25000         0.295857           312487500
                 Bubble Sort         Random           50000         4.536000          1249952845
                   Heap Sort         Random           50000         0.009000             1409656
              Insertion Sort         Random           50000         0.843714           626019787
                  Merge Sort         Random           50000         0.011000              718076
Quick Sort (Median of Three)         Random           50000         0.004571              886476
                  Radix Sort         Random           50000         0.001571               49999
              Selection Sort         Random           50000         1.208429          1249975000
                 Bubble Sort Reverse Sorted           50000         2.995571          1249975000
                   Heap Sort Reverse Sorted           50000         0.006143             1366047
              Insertion Sort Reverse Sorted           50000         1.622714          1249975000
                  Merge Sort Reverse Sorted           50000         0.006857              382512
Quick Sort (Median of Three) Reverse Sorted           50000         0.003143             1433133
                  Radix Sort Reverse Sorted           50000         0.001571               49999
              Selection Sort Reverse Sorted           50000         1.190857          1249975000
                 Bubble Sort         Sorted           50000         0.000286               49999
                   Heap Sort         Sorted           50000         0.007429             1455438
              Insertion Sort         Sorted           50000         0.000143               49999
                  Merge Sort         Sorted           50000         0.006714              401952
Quick Sort (Median of Three)         Sorted           50000         0.001286              782782
                  Radix Sort         Sorted           50000         0.001429               49999
              Selection Sort         Sorted           50000         1.165571          1249975000
                 Bubble Sort         Random           75000        10.747000          2812436165
                   Heap Sort         Random           75000         0.014000             2199901
              Insertion Sort         Random           75000         1.898429          1408462710
                  Merge Sort         Random           75000         0.016143             1121269
Quick Sort (Median of Three)         Random           75000         0.007286             1414347
                  Radix Sort         Random           75000         0.003143               74999
              Selection Sort         Random           75000         2.739571          2812462500
                 Bubble Sort Reverse Sorted           75000         6.675714          2812462500
                   Heap Sort Reverse Sorted           75000         0.010286             2138650
              Insertion Sort Reverse Sorted           75000         3.787429          2812462500
                  Merge Sort Reverse Sorted           75000         0.010571              594612
Quick Sort (Median of Three) Reverse Sorted           75000         0.004571             2272487
                  Radix Sort Reverse Sorted           75000         0.002286               74999
              Selection Sort Reverse Sorted           75000         2.674429          2812462500
                 Bubble Sort         Sorted           75000         0.000000               74999
                   Heap Sort         Sorted           75000         0.011143             2268087
              Insertion Sort         Sorted           75000         0.000286               74999
                  Merge Sort         Sorted           75000         0.010571              624316
Quick Sort (Median of Three)         Sorted           75000         0.002571             1195642
                  Radix Sort         Sorted           75000         0.002857               74999
              Selection Sort         Sorted           75000         2.616286          2812462500
                 Bubble Sort         Random          100000        19.864714          4999817130
                   Heap Sort         Random          100000         0.019857             3019257
              Insertion Sort         Random          100000         3.362429          2496007172
                  Merge Sort         Random          100000         0.022857             1536758
Quick Sort (Median of Three)         Random          100000         0.009429             1889583
                  Radix Sort         Random          100000         0.003857               99999
              Selection Sort         Random          100000         4.869857          4999950000
                 Bubble Sort Reverse Sorted          100000        12.020143          4999950000
                   Heap Sort Reverse Sorted          100000         0.014143             2926640
              Insertion Sort Reverse Sorted          100000         6.714714          4999950000
                  Merge Sort Reverse Sorted          100000         0.015714              815024
Quick Sort (Median of Three) Reverse Sorted          100000         0.006429             3107283
                  Radix Sort Reverse Sorted          100000         0.003429               99999
              Selection Sort Reverse Sorted          100000         4.964143          4999950000
                 Bubble Sort         Sorted          100000         0.000286               99999
                   Heap Sort         Sorted          100000         0.014429             3112517
              Insertion Sort         Sorted          100000         0.000286               99999
                  Merge Sort         Sorted          100000         0.014857              853904
Quick Sort (Median of Three)         Sorted          100000         0.003429             1665551
                  Radix Sort         Sorted          100000         0.003143               99999
              Selection Sort         Sorted          100000         4.556429          4999950000

Full results table saved to graphs\csv_data\all_sorting_benchmark_results.csv

--- Correlation Analysis Summary ---
Algorithm                           | Correlation (r) | P-value
----------------------------------------------------------------------
Bubble Sort                         |          0.9658 | 3.6058e-16
Heap Sort                           |          0.9814 | 2.0022e-19
Insertion Sort                      |          1.0000 | 6.3367e-55
Merge Sort                          |          0.9912 | 1.6694e-23
Quick Sort (Median of Three)        |          0.8590 | 9.7489e-09
Radix Sort                          |          0.9806 | 3.3426e-19
Selection Sort                      |          0.9993 | 6.8275e-37

Interpretation:
  r close to 1.0: Strong positive correlation (more comparisons → more time)
  r close to 0.0: Weak/no correlation
  p-value < 0.05: Statistically significant correlation

================================================================================
IMPORTANT NOTES ON RESULTS
================================================================================

⚠️  TIMING MEASUREMENT:
  - Timing is measured INSIDE C code using clock() from <time.h>
  - The clock() function measures CPU time used by the program
  - Python is only used to run the executable and collect results
  - This avoids Python subprocess overhead affecting algorithm timing

⚠️  RADIX SORT 'COMPARISONS' NOTE:
  - Radix sort is a NON-COMPARATIVE sorting algorithm
  - It does NOT use element comparisons (like other algorithms)
  - The 'comparisons' count represents operations in getMax() function
  - This value (~n) is NOT comparable to other algorithms' comparisons
  - Use TIME metric, not COMPARISONS, to evaluate radix sort performance

✓ EXPECTED BEHAVIOR:
  - O(n²) algorithms: Bubble, Insertion, Selection Sort
  - O(n log n) algorithms: Heap, Merge, Quick Sort
  - O(n+k) algorithm: Radix Sort (where k is key range)
  - Best case optimized: Bubble & Insertion sort show O(n) for sorted input
================================================================================