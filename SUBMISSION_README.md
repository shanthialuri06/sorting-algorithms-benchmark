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
- Lagudu Pranathi(241CS130)
- Bandi Jyothsna(241CS116)

---

### Terminal Output

```
PS C:\Users\hp\Desktop\daa practical assignment\sorting-algorithms-benchmark> python benchmark.py
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
  bubble_sort: Time = 0.000000 s, Comparisons = 4940
  heap_sort: Time = 0.000000 s, Comparisons = 1037
  insertion_sort: Time = 0.000000 s, Comparisons = 2565
  merge_sort: Time = 0.000000 s, Comparisons = 542
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 718
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 653
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 718
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 684
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
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 694
Benchmarking N=100, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99
  heap_sort: Time = 0.000000 s, Comparisons = 1081
  insertion_sort: Time = 0.000000 s, Comparisons = 99
  merge_sort: Time = 0.000000 s, Comparisons = 356
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.001286 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 585
Benchmarking N=500, Type=random...
  bubble_sort: Time = 0.000714 s, Comparisons = 124344
  heap_sort: Time = 0.000000 s, Comparisons = 7384
  insertion_sort: Time = 0.000000 s, Comparisons = 61485
  merge_sort: Time = 0.000000 s, Comparisons = 3846
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5407
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4919
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5407
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 5283
Benchmarking N=500, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 124750
  heap_sort: Time = 0.000000 s, Comparisons = 7010
  insertion_sort: Time = 0.000000 s, Comparisons = 124750
  merge_sort: Time = 0.000000 s, Comparisons = 2216
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000143 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000429 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4991
Benchmarking N=500, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 499
  heap_sort: Time = 0.000000 s, Comparisons = 7756
  insertion_sort: Time = 0.000000 s, Comparisons = 499
  merge_sort: Time = 0.000000 s, Comparisons = 2272
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000000 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 4857
Benchmarking N=1000, Type=random...
  bubble_sort: Time = 0.001714 s, Comparisons = 499122
  heap_sort: Time = 0.000000 s, Comparisons = 16826
  insertion_sort: Time = 0.000143 s, Comparisons = 262256
  merge_sort: Time = 0.002429 s, Comparisons = 8704
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11247
  radix_sort: Time = 0.000571 s, Comparisons = 999
  selection_sort: Time = 0.002000 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000286 s, Comparisons = 11604
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 11247
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 11223
Benchmarking N=1000, Type=reverse_sorted...
  bubble_sort: Time = 0.002143 s, Comparisons = 499500
  heap_sort: Time = 0.000000 s, Comparisons = 15965
  insertion_sort: Time = 0.000429 s, Comparisons = 499500
  merge_sort: Time = 0.000429 s, Comparisons = 4932
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.003429 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.004286 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  quick_sort_random_pivot: Time = 0.000286 s, Comparisons = 11251
Benchmarking N=1000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 999
  heap_sort: Time = 0.000000 s, Comparisons = 17583
  insertion_sort: Time = 0.000000 s, Comparisons = 999
  merge_sort: Time = 0.001286 s, Comparisons = 5044
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.001714 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  quick_sort_random_pivot: Time = 0.000857 s, Comparisons = 11218
Benchmarking N=5000, Type=random...
  bubble_sort: Time = 0.066286 s, Comparisons = 12496939
  heap_sort: Time = 0.000000 s, Comparisons = 107711
  insertion_sort: Time = 0.026429 s, Comparisons = 6105032
  merge_sort: Time = 0.002857 s, Comparisons = 55269
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 70736
  radix_sort: Time = 0.000571 s, Comparisons = 4999
  selection_sort: Time = 0.035286 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 68925
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 70736
  quick_sort_random_pivot: Time = 0.002571 s, Comparisons = 70619
Benchmarking N=5000, Type=reverse_sorted...
  bubble_sort: Time = 0.064000 s, Comparisons = 12497500
  heap_sort: Time = 0.001143 s, Comparisons = 103227
  insertion_sort: Time = 0.036571 s, Comparisons = 12497500
  merge_sort: Time = 0.001286 s, Comparisons = 29804
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 106182
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.029429 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.045143 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 106182
  quick_sort_random_pivot: Time = 0.000429 s, Comparisons = 73399
Benchmarking N=5000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4999
  heap_sort: Time = 0.000714 s, Comparisons = 112126
  insertion_sort: Time = 0.000000 s, Comparisons = 4999
  merge_sort: Time = 0.001286 s, Comparisons = 32004
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  radix_sort: Time = 0.000000 s, Comparisons = 4999
  selection_sort: Time = 0.039571 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.042000 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 60678
  quick_sort_random_pivot: Time = 0.002143 s, Comparisons = 70518
Benchmarking N=10000, Type=random...
  bubble_sort: Time = 0.253000 s, Comparisons = 49989540
  heap_sort: Time = 0.002286 s, Comparisons = 235355
  insertion_sort: Time = 0.075571 s, Comparisons = 25103885
  merge_sort: Time = 0.002000 s, Comparisons = 120538
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 151905
  radix_sort: Time = 0.000000 s, Comparisons = 9999
  selection_sort: Time = 0.141143 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.001429 s, Comparisons = 167688
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 151905
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 166452
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.245286 s, Comparisons = 49995000
  heap_sort: Time = 0.000000 s, Comparisons = 226682
  insertion_sort: Time = 0.154286 s, Comparisons = 49995000
  merge_sort: Time = 0.003857 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 234923
  radix_sort: Time = 0.001429 s, Comparisons = 9999
  selection_sort: Time = 0.127714 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.224429 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.003429 s, Comparisons = 160531
Benchmarking N=10000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 9999
  heap_sort: Time = 0.001714 s, Comparisons = 244460
  insertion_sort: Time = 0.000000 s, Comparisons = 9999
  merge_sort: Time = 0.000571 s, Comparisons = 69008
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 131343
  radix_sort: Time = 0.000857 s, Comparisons = 9999
  selection_sort: Time = 0.137000 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.122857 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 131343
  quick_sort_random_pivot: Time = 0.001000 s, Comparisons = 164699
Benchmarking N=25000, Type=random...
  bubble_sort: Time = 2.004429 s, Comparisons = 312486554
  heap_sort: Time = 0.007286 s, Comparisons = 654939
  insertion_sort: Time = 0.516286 s, Comparisons = 155385138
  merge_sort: Time = 0.011714 s, Comparisons = 334294
  quick_sort_median_of_three_pivot: Time = 0.005429 s, Comparisons = 418267
  radix_sort: Time = 0.000000 s, Comparisons = 24999
  selection_sort: Time = 0.891429 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.003429 s, Comparisons = 433110
  quick_sort_median_of_three_pivot: Time = 0.005857 s, Comparisons = 418267
  quick_sort_random_pivot: Time = 0.004714 s, Comparisons = 439755
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 1.879000 s, Comparisons = 312487500
  heap_sort: Time = 0.003429 s, Comparisons = 633719
  insertion_sort: Time = 0.938000 s, Comparisons = 312487500
  merge_sort: Time = 0.009571 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.003286 s, Comparisons = 660758
  radix_sort: Time = 0.003143 s, Comparisons = 24999
  selection_sort: Time = 0.858000 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 1.329857 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.005714 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.002143 s, Comparisons = 426642
Benchmarking N=25000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 24999
  heap_sort: Time = 0.007286 s, Comparisons = 677688
  insertion_sort: Time = 0.000000 s, Comparisons = 24999
  merge_sort: Time = 0.006571 s, Comparisons = 188476
  quick_sort_median_of_three_pivot: Time = 0.002000 s, Comparisons = 366397
  radix_sort: Time = 0.000286 s, Comparisons = 24999
  selection_sort: Time = 0.896857 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.812143 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.000286 s, Comparisons = 366397
  quick_sort_random_pivot: Time = 0.002714 s, Comparisons = 420305
Benchmarking N=50000, Type=random...
  bubble_sort: Time = 8.418857 s, Comparisons = 1249958710
  heap_sort: Time = 0.012857 s, Comparisons = 1409503
  insertion_sort: Time = 1.920857 s, Comparisons = 627403873
  merge_sort: Time = 0.020857 s, Comparisons = 718279
  quick_sort_median_of_three_pivot: Time = 0.006286 s, Comparisons = 904304
  radix_sort: Time = 0.008714 s, Comparisons = 49999
  selection_sort: Time = 3.629571 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.008143 s, Comparisons = 909232
  quick_sort_median_of_three_pivot: Time = 0.007000 s, Comparisons = 904304
  quick_sort_random_pivot: Time = 0.006143 s, Comparisons = 911873
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 7.210286 s, Comparisons = 1249975000
  heap_sort: Time = 0.011143 s, Comparisons = 1366047
  insertion_sort: Time = 3.993429 s, Comparisons = 1249975000
  merge_sort: Time = 0.013143 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.008571 s, Comparisons = 1433133
  radix_sort: Time = 0.000429 s, Comparisons = 49999
  selection_sort: Time = 3.510857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 5.411000 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  quick_sort_median_of_three_pivot: Time = 0.006286 s, Comparisons = 904304
  radix_sort: Time = 0.008714 s, Comparisons = 49999
  selection_sort: Time = 3.629571 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.008143 s, Comparisons = 909232
  quick_sort_median_of_three_pivot: Time = 0.007000 s, Comparisons = 904304
  quick_sort_random_pivot: Time = 0.006143 s, Comparisons = 911873
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 7.210286 s, Comparisons = 1249975000
  heap_sort: Time = 0.011143 s, Comparisons = 1366047
  insertion_sort: Time = 3.993429 s, Comparisons = 1249975000
  merge_sort: Time = 0.013143 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.008571 s, Comparisons = 1433133
  radix_sort: Time = 0.000429 s, Comparisons = 49999
  selection_sort: Time = 3.510857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 5.411000 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.006429 s, Comparisons = 912322
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 7.210286 s, Comparisons = 1249975000
  heap_sort: Time = 0.011143 s, Comparisons = 1366047
  insertion_sort: Time = 3.993429 s, Comparisons = 1249975000
  merge_sort: Time = 0.013143 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.008571 s, Comparisons = 1433133
  radix_sort: Time = 0.000429 s, Comparisons = 49999
  selection_sort: Time = 3.510857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 5.411000 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.006429 s, Comparisons = 912322
  merge_sort: Time = 0.013143 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.008571 s, Comparisons = 1433133
  radix_sort: Time = 0.000429 s, Comparisons = 49999
  selection_sort: Time = 3.510857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 5.411000 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.006429 s, Comparisons = 912322
  quick_sort_first_pivot: Time = 5.411000 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.003143 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.006429 s, Comparisons = 912322
  quick_sort_random_pivot: Time = 0.006429 s, Comparisons = 912322
Benchmarking N=50000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 49999
  heap_sort: Time = 0.014000 s, Comparisons = 1455438
  insertion_sort: Time = 0.000000 s, Comparisons = 49999
  merge_sort: Time = 0.016714 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.002714 s, Comparisons = 782782
  radix_sort: Time = 0.004286 s, Comparisons = 49999
  selection_sort: Time = 3.685286 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 3.423857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.011143 s, Comparisons = 948082
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 20.187571 s, Comparisons = 2812274922
  merge_sort: Time = 0.016714 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.002714 s, Comparisons = 782782
  radix_sort: Time = 0.004286 s, Comparisons = 49999
  selection_sort: Time = 3.685286 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 3.423857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.011143 s, Comparisons = 948082
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 20.187571 s, Comparisons = 2812274922
  quick_sort_first_pivot: Time = 3.423857 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.011143 s, Comparisons = 948082
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 20.187571 s, Comparisons = 2812274922
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 20.187571 s, Comparisons = 2812274922
  bubble_sort: Time = 20.187571 s, Comparisons = 2812274922
  heap_sort: Time = 0.020000 s, Comparisons = 2200261
  insertion_sort: Time = 4.764571 s, Comparisons = 1405670266
  merge_sort: Time = 0.030143 s, Comparisons = 1121273
  quick_sort_median_of_three_pivot: Time = 0.016143 s, Comparisons = 1408373
  radix_sort: Time = 0.012429 s, Comparisons = 74999
  selection_sort: Time = 9.120286 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 0.009571 s, Comparisons = 1459740
  quick_sort_median_of_three_pivot: Time = 0.013000 s, Comparisons = 1408373
  quick_sort_random_pivot: Time = 0.014571 s, Comparisons = 1438184
Benchmarking N=75000, Type=reverse_sorted...
  bubble_sort: Time = 19.568143 s, Comparisons = 2812462500
  heap_sort: Time = 0.019857 s, Comparisons = 2138650
  insertion_sort: Time = 10.490714 s, Comparisons = 2812462500
  merge_sort: Time = 0.022857 s, Comparisons = 594612
  quick_sort_median_of_three_pivot: Time = 0.007286 s, Comparisons = 2272487
  radix_sort: Time = 0.001143 s, Comparisons = 74999
  selection_sort: Time = 8.153429 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 22.884000 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.011143 s, Comparisons = 2272487
  quick_sort_random_pivot: Time = 0.008000 s, Comparisons = 1464630
Benchmarking N=75000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 74999
  heap_sort: Time = 0.016571 s, Comparisons = 2268087
  insertion_sort: Time = 0.000000 s, Comparisons = 74999
  merge_sort: Time = 0.027571 s, Comparisons = 624316
  quick_sort_median_of_three_pivot: Time = 0.007143 s, Comparisons = 1195642
  radix_sort: Time = 0.003714 s, Comparisons = 74999
  selection_sort: Time = 13.026143 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 8.247143 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.003571 s, Comparisons = 1195642
  quick_sort_random_pivot: Time = 0.009143 s, Comparisons = 1457487
Benchmarking N=100000, Type=random...
  bubble_sort: Time = 35.243429 s, Comparisons = 4999931085
  heap_sort: Time = 0.029714 s, Comparisons = 3019624
  insertion_sort: Time = 7.490429 s, Comparisons = 2500780850
  merge_sort: Time = 0.039143 s, Comparisons = 1536387
  quick_sort_median_of_three_pivot: Time = 0.016000 s, Comparisons = 1879008
  radix_sort: Time = 0.011714 s, Comparisons = 99999
  selection_sort: Time = 14.855857 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 0.015857 s, Comparisons = 2031159
  quick_sort_median_of_three_pivot: Time = 0.013857 s, Comparisons = 1879008
  quick_sort_random_pivot: Time = 0.016857 s, Comparisons = 2102663
Benchmarking N=100000, Type=reverse_sorted...
  bubble_sort: Time = 114.610000 s, Comparisons = 4999950000
  heap_sort: Time = 0.013571 s, Comparisons = 2926640
  insertion_sort: Time = 9.748857 s, Comparisons = 4999950000
  merge_sort: Time = 0.016714 s, Comparisons = 815024
  quick_sort_median_of_three_pivot: Time = 0.006857 s, Comparisons = 3107283
  radix_sort: Time = 0.003714 s, Comparisons = 99999
  selection_sort: Time = 8.665286 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 12.925000 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.008143 s, Comparisons = 3107283
  quick_sort_random_pivot: Time = 0.009000 s, Comparisons = 1948031
Benchmarking N=100000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99999
  heap_sort: Time = 0.016857 s, Comparisons = 3112517
  insertion_sort: Time = 0.000000 s, Comparisons = 99999
  merge_sort: Time = 0.020000 s, Comparisons = 853904
  quick_sort_median_of_three_pivot: Time = 0.003429 s, Comparisons = 1665551
  radix_sort: Time = 0.005857 s, Comparisons = 99999
  selection_sort: Time = 9.234714 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 8.019429 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.004429 s, Comparisons = 1665551
  quick_sort_random_pivot: Time = 0.008714 s, Comparisons = 1920921

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
                 Bubble Sort         Random             100         0.000000                4940
                   Heap Sort         Random             100         0.000000                1037
              Insertion Sort         Random             100         0.000000                2565
                  Merge Sort         Random             100         0.000000                 542
Quick Sort (Median of Three)         Random             100         0.000000                 718
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
              Selection Sort         Sorted             100         0.001286                4950
                 Bubble Sort         Random             500         0.000714              124344
                   Heap Sort         Random             500         0.000000                7384
              Insertion Sort         Random             500         0.000000               61485
                  Merge Sort         Random             500         0.000000                3846
Quick Sort (Median of Three)         Random             500         0.000000                5407
                  Radix Sort         Random             500         0.000000                 499
              Selection Sort         Random             500         0.000000              124750
                 Bubble Sort Reverse Sorted             500         0.000000              124750
                   Heap Sort Reverse Sorted             500         0.000000                7010
              Insertion Sort Reverse Sorted             500         0.000000              124750
                  Merge Sort Reverse Sorted             500         0.000000                2216
Quick Sort (Median of Three) Reverse Sorted             500         0.000000                6790
                  Radix Sort Reverse Sorted             500         0.000000                 499
              Selection Sort Reverse Sorted             500         0.000143              124750
                 Bubble Sort         Sorted             500         0.000000                 499
                   Heap Sort         Sorted             500         0.000000                7756
              Insertion Sort         Sorted             500         0.000000                 499
                  Merge Sort         Sorted             500         0.000000                2272
Quick Sort (Median of Three)         Sorted             500         0.000000                4263
                  Radix Sort         Sorted             500         0.000000                 499
              Selection Sort         Sorted             500         0.000000              124750
                 Bubble Sort         Random            1000         0.001714              499122
                   Heap Sort         Random            1000         0.000000               16826
              Insertion Sort         Random            1000         0.000143              262256
                  Merge Sort         Random            1000         0.002429                8704
Quick Sort (Median of Three)         Random            1000         0.000000               11247
                  Radix Sort         Random            1000         0.000571                 999
              Selection Sort         Random            1000         0.002000              499500
                 Bubble Sort Reverse Sorted            1000         0.002143              499500
                   Heap Sort Reverse Sorted            1000         0.000000               15965
              Insertion Sort Reverse Sorted            1000         0.000429              499500
                  Merge Sort Reverse Sorted            1000         0.000429                4932
Quick Sort (Median of Three) Reverse Sorted            1000         0.000000               15849
                  Radix Sort Reverse Sorted            1000         0.000000                 999
              Selection Sort Reverse Sorted            1000         0.003429              499500
                 Bubble Sort         Sorted            1000         0.000000                 999
                   Heap Sort         Sorted            1000         0.000000               17583
              Insertion Sort         Sorted            1000         0.000000                 999
                  Merge Sort         Sorted            1000         0.001286                5044
Quick Sort (Median of Three)         Sorted            1000         0.000000                9520
                  Radix Sort         Sorted            1000         0.000000                 999
              Selection Sort         Sorted            1000         0.001714              499500
                 Bubble Sort         Random            5000         0.066286            12496939
                   Heap Sort         Random            5000         0.000000              107711
              Insertion Sort         Random            5000         0.026429             6105032
                  Merge Sort         Random            5000         0.002857               55269
Quick Sort (Median of Three)         Random            5000         0.001286               70736
                  Radix Sort         Random            5000         0.000571                4999
              Selection Sort         Random            5000         0.035286            12497500
                 Bubble Sort Reverse Sorted            5000         0.064000            12497500
                   Heap Sort Reverse Sorted            5000         0.001143              103227
              Insertion Sort Reverse Sorted            5000         0.036571            12497500
                  Merge Sort Reverse Sorted            5000         0.001286               29804
Quick Sort (Median of Three) Reverse Sorted            5000         0.000000              106182
                  Radix Sort Reverse Sorted            5000         0.000000                4999
              Selection Sort Reverse Sorted            5000         0.029429            12497500
                 Bubble Sort         Sorted            5000         0.000000                4999
                   Heap Sort         Sorted            5000         0.000714              112126
              Insertion Sort         Sorted            5000         0.000000                4999
                  Merge Sort         Sorted            5000         0.001286               32004
Quick Sort (Median of Three)         Sorted            5000         0.000000               60678
                  Radix Sort         Sorted            5000         0.000000                4999
              Selection Sort         Sorted            5000         0.039571            12497500
                 Bubble Sort         Random           10000         0.253000            49989540
                   Heap Sort         Random           10000         0.002286              235355
              Insertion Sort         Random           10000         0.075571            25103885
                  Merge Sort         Random           10000         0.002000              120538
Quick Sort (Median of Three)         Random           10000         0.001429              151905
                  Radix Sort         Random           10000         0.000000                9999
              Selection Sort         Random           10000         0.141143            49995000
                 Bubble Sort Reverse Sorted           10000         0.245286            49995000
                   Heap Sort Reverse Sorted           10000         0.000000              226682
              Insertion Sort Reverse Sorted           10000         0.154286            49995000
                  Merge Sort Reverse Sorted           10000         0.003857               64608
Quick Sort (Median of Three) Reverse Sorted           10000         0.000857              234923
                  Radix Sort Reverse Sorted           10000         0.001429                9999
              Selection Sort Reverse Sorted           10000         0.127714            49995000
                 Bubble Sort         Sorted           10000         0.000000                9999
                   Heap Sort         Sorted           10000         0.001714              244460
              Insertion Sort         Sorted           10000         0.000000                9999
                  Merge Sort         Sorted           10000         0.000571               69008
Quick Sort (Median of Three)         Sorted           10000         0.000000              131343
                  Radix Sort         Sorted           10000         0.000857                9999
              Selection Sort         Sorted           10000         0.137000            49995000
                 Bubble Sort         Random           25000         2.004429           312486554
                   Heap Sort         Random           25000         0.007286              654939
              Insertion Sort         Random           25000         0.516286           155385138
                  Merge Sort         Random           25000         0.011714              334294
Quick Sort (Median of Three)         Random           25000         0.005429              418267
                  Radix Sort         Random           25000         0.000000               24999
              Selection Sort         Random           25000         0.891429           312487500
                 Bubble Sort Reverse Sorted           25000         1.879000           312487500
                   Heap Sort Reverse Sorted           25000         0.003429              633719
              Insertion Sort Reverse Sorted           25000         0.938000           312487500
                  Merge Sort Reverse Sorted           25000         0.009571              178756
Quick Sort (Median of Three) Reverse Sorted           25000         0.003286              660758
                  Radix Sort Reverse Sorted           25000         0.003143               24999
              Selection Sort Reverse Sorted           25000         0.858000           312487500
                 Bubble Sort         Sorted           25000         0.000000               24999
                   Heap Sort         Sorted           25000         0.007286              677688
              Insertion Sort         Sorted           25000         0.000000               24999
                  Merge Sort         Sorted           25000         0.006571              188476
Quick Sort (Median of Three)         Sorted           25000         0.002000              366397
                  Radix Sort         Sorted           25000         0.000286               24999
              Selection Sort         Sorted           25000         0.896857           312487500
                 Bubble Sort         Random           50000         8.418857          1249958710
                   Heap Sort         Random           50000         0.012857             1409503
              Insertion Sort         Random           50000         1.920857           627403873
                  Merge Sort         Random           50000         0.020857              718279
Quick Sort (Median of Three)         Random           50000         0.006286              904304
                  Radix Sort         Random           50000         0.008714               49999
              Selection Sort         Random           50000         3.629571          1249975000
                 Bubble Sort Reverse Sorted           50000         7.210286          1249975000
                   Heap Sort Reverse Sorted           50000         0.011143             1366047
              Insertion Sort Reverse Sorted           50000         3.993429          1249975000
                  Merge Sort Reverse Sorted           50000         0.013143              382512
Quick Sort (Median of Three) Reverse Sorted           50000         0.008571             1433133
                  Radix Sort Reverse Sorted           50000         0.000429               49999
              Selection Sort Reverse Sorted           50000         3.510857          1249975000
                 Bubble Sort         Sorted           50000         0.000000               49999
                   Heap Sort         Sorted           50000         0.014000             1455438
              Insertion Sort         Sorted           50000         0.000000               49999
                  Merge Sort         Sorted           50000         0.016714              401952
Quick Sort (Median of Three)         Sorted           50000         0.002714              782782
                  Radix Sort         Sorted           50000         0.004286               49999
              Selection Sort         Sorted           50000         3.685286          1249975000
                 Bubble Sort         Random           75000        20.187571          2812274922
                   Heap Sort         Random           75000         0.020000             2200261
              Insertion Sort         Random           75000         4.764571          1405670266
                  Merge Sort         Random           75000         0.030143             1121273
Quick Sort (Median of Three)         Random           75000         0.016143             1408373
                  Radix Sort         Random           75000         0.012429               74999
              Selection Sort         Random           75000         9.120286          2812462500
                 Bubble Sort Reverse Sorted           75000        19.568143          2812462500
                   Heap Sort Reverse Sorted           75000         0.019857             2138650
              Insertion Sort Reverse Sorted           75000        10.490714          2812462500
                  Merge Sort Reverse Sorted           75000         0.022857              594612
Quick Sort (Median of Three) Reverse Sorted           75000         0.007286             2272487
                  Radix Sort Reverse Sorted           75000         0.001143               74999
              Selection Sort Reverse Sorted           75000         8.153429          2812462500
                 Bubble Sort         Sorted           75000         0.000000               74999
                   Heap Sort         Sorted           75000         0.016571             2268087
              Insertion Sort         Sorted           75000         0.000000               74999
                  Merge Sort         Sorted           75000         0.027571              624316
Quick Sort (Median of Three)         Sorted           75000         0.007143             1195642
                  Radix Sort         Sorted           75000         0.003714               74999
              Selection Sort         Sorted           75000        13.026143          2812462500
                 Bubble Sort         Random          100000        35.243429          4999931085
                   Heap Sort         Random          100000         0.029714             3019624
              Insertion Sort         Random          100000         7.490429          2500780850
                  Merge Sort         Random          100000         0.039143             1536387
Quick Sort (Median of Three)         Random          100000         0.016000             1879008
                  Radix Sort         Random          100000         0.011714               99999
              Selection Sort         Random          100000        14.855857          4999950000
                 Bubble Sort Reverse Sorted          100000       114.610000          4999950000
                   Heap Sort Reverse Sorted          100000         0.013571             2926640
              Insertion Sort Reverse Sorted          100000         9.748857          4999950000
                  Merge Sort Reverse Sorted          100000         0.016714              815024
Quick Sort (Median of Three) Reverse Sorted          100000         0.006857             3107283
                  Radix Sort Reverse Sorted          100000         0.003714               99999
              Selection Sort Reverse Sorted          100000         8.665286          4999950000
                 Bubble Sort         Sorted          100000         0.000000               99999
                   Heap Sort         Sorted          100000         0.016857             3112517
              Insertion Sort         Sorted          100000         0.000000               99999
                  Merge Sort         Sorted          100000         0.020000              853904
Quick Sort (Median of Three)         Sorted          100000         0.003429             1665551
                  Radix Sort         Sorted          100000         0.005857               99999
              Selection Sort         Sorted          100000         9.234714          4999950000

Full results table saved to graphs\csv_data\all_sorting_benchmark_results.csv

--- Correlation Analysis Summary ---
Algorithm                           | Correlation (r) | P-value
----------------------------------------------------------------------
Bubble Sort                         |          0.8407 | 4.0455e-08
Heap Sort                           |          0.9390 | 4.3162e-13
Insertion Sort                      |          0.9525 | 2.0286e-14
Merge Sort                          |          0.9595 | 2.8808e-15
Quick Sort (Median of Three)        |          0.7443 | 8.5400e-06
Radix Sort                          |          0.7427 | 9.1664e-06
Selection Sort                      |          0.9288 | 2.8225e-12

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