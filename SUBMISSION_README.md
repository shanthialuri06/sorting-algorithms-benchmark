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
- Aluri Shanthi(241CS206)
- Sornala Suhitha(241CS156)

---

### Terminal Output

```
PS C:\Users\shanthialuri\OneDrive\Desktop\DAA PRACTICAL ASSIGNMENT\sorting-algorithms-benchmark> python benchmark.py        
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
  bubble_sort: Time = 0.000000 s, Comparisons = 4859
  heap_sort: Time = 0.000000 s, Comparisons = 1016
  insertion_sort: Time = 0.000000 s, Comparisons = 2766
  merge_sort: Time = 0.000000 s, Comparisons = 547
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 711
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 672
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 711
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 667
Benchmarking N=100, Type=reverse_sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4950
  heap_sort: Time = 0.000000 s, Comparisons = 944
  insertion_sort: Time = 0.000000 s, Comparisons = 4950
  merge_sort: Time = 0.000143 s, Comparisons = 316
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 868
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 631
Benchmarking N=100, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 99
  heap_sort: Time = 0.000000 s, Comparisons = 1081
  insertion_sort: Time = 0.000000 s, Comparisons = 99
  merge_sort: Time = 0.000143 s, Comparisons = 356
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  radix_sort: Time = 0.000000 s, Comparisons = 99
  selection_sort: Time = 0.000000 s, Comparisons = 4950
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 4950
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 669
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 596
Benchmarking N=500, Type=random...
  bubble_sort: Time = 0.001000 s, Comparisons = 124747
  heap_sort: Time = 0.000143 s, Comparisons = 7424
  insertion_sort: Time = 0.000143 s, Comparisons = 61475
  merge_sort: Time = 0.000714 s, Comparisons = 3864
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 5400
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000143 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000143 s, Comparisons = 4464
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 5400
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 4456
Benchmarking N=500, Type=reverse_sorted...
  bubble_sort: Time = 0.000286 s, Comparisons = 124750
  heap_sort: Time = 0.000286 s, Comparisons = 7010
  insertion_sort: Time = 0.000143 s, Comparisons = 124750
  merge_sort: Time = 0.000000 s, Comparisons = 2216
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000143 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000286 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 6790
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 5076
Benchmarking N=500, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 499
  heap_sort: Time = 0.000143 s, Comparisons = 7756
  insertion_sort: Time = 0.000000 s, Comparisons = 499
  merge_sort: Time = 0.000143 s, Comparisons = 2272
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  radix_sort: Time = 0.000000 s, Comparisons = 499
  selection_sort: Time = 0.000429 s, Comparisons = 124750
  quick_sort_first_pivot: Time = 0.000286 s, Comparisons = 124750
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 4263
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 5435
Benchmarking N=1000, Type=random...
  bubble_sort: Time = 0.003000 s, Comparisons = 498015
  heap_sort: Time = 0.000143 s, Comparisons = 16911
  insertion_sort: Time = 0.000429 s, Comparisons = 246495
  merge_sort: Time = 0.000857 s, Comparisons = 8733
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 11016
  radix_sort: Time = 0.000143 s, Comparisons = 999
  selection_sort: Time = 0.001000 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000000 s, Comparisons = 10893
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 11016
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 11315
Benchmarking N=1000, Type=reverse_sorted...
  bubble_sort: Time = 0.003143 s, Comparisons = 499500
  heap_sort: Time = 0.000000 s, Comparisons = 15965
  insertion_sort: Time = 0.001286 s, Comparisons = 499500
  merge_sort: Time = 0.000286 s, Comparisons = 4932
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.000714 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.001571 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 15849
  quick_sort_random_pivot: Time = 0.000143 s, Comparisons = 11568
Benchmarking N=1000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 999
  heap_sort: Time = 0.000000 s, Comparisons = 17583
  insertion_sort: Time = 0.000000 s, Comparisons = 999
  merge_sort: Time = 0.000286 s, Comparisons = 5044
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 9520
  radix_sort: Time = 0.000000 s, Comparisons = 999
  selection_sort: Time = 0.001286 s, Comparisons = 499500
  quick_sort_first_pivot: Time = 0.000571 s, Comparisons = 499500
  quick_sort_median_of_three_pivot: Time = 0.000000 s, Comparisons = 9520
  quick_sort_random_pivot: Time = 0.000000 s, Comparisons = 12224
Benchmarking N=5000, Type=random...
  bubble_sort: Time = 0.049143 s, Comparisons = 12494260
  heap_sort: Time = 0.001143 s, Comparisons = 107630
  insertion_sort: Time = 0.017714 s, Comparisons = 6302243
  merge_sort: Time = 0.001857 s, Comparisons = 55242
  quick_sort_median_of_three_pivot: Time = 0.001143 s, Comparisons = 69275
  radix_sort: Time = 0.000571 s, Comparisons = 4999
  selection_sort: Time = 0.022714 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.001429 s, Comparisons = 68132
  quick_sort_median_of_three_pivot: Time = 0.000857 s, Comparisons = 69275
  quick_sort_random_pivot: Time = 0.000571 s, Comparisons = 67787
Benchmarking N=5000, Type=reverse_sorted...
  bubble_sort: Time = 0.053286 s, Comparisons = 12497500
  heap_sort: Time = 0.001429 s, Comparisons = 103227
  insertion_sort: Time = 0.031429 s, Comparisons = 12497500
  merge_sort: Time = 0.001714 s, Comparisons = 29804
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 106182
  radix_sort: Time = 0.000571 s, Comparisons = 4999
  selection_sort: Time = 0.023000 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.042143 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000714 s, Comparisons = 106182
  quick_sort_random_pivot: Time = 0.000714 s, Comparisons = 69056
Benchmarking N=5000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 4999
  heap_sort: Time = 0.001429 s, Comparisons = 112126
  insertion_sort: Time = 0.000000 s, Comparisons = 4999
  merge_sort: Time = 0.002429 s, Comparisons = 32004
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 60678
  radix_sort: Time = 0.000143 s, Comparisons = 4999
  selection_sort: Time = 0.023857 s, Comparisons = 12497500
  quick_sort_first_pivot: Time = 0.017429 s, Comparisons = 12497500
  quick_sort_median_of_three_pivot: Time = 0.000571 s, Comparisons = 60678
  quick_sort_random_pivot: Time = 0.000714 s, Comparisons = 70687
Benchmarking N=10000, Type=random...
  bubble_sort: Time = 0.240143 s, Comparisons = 49986089
  heap_sort: Time = 0.003571 s, Comparisons = 235292
  insertion_sort: Time = 0.068000 s, Comparisons = 25149713
  merge_sort: Time = 0.004857 s, Comparisons = 120453
  quick_sort_median_of_three_pivot: Time = 0.002000 s, Comparisons = 151973
  radix_sort: Time = 0.000571 s, Comparisons = 9999
  selection_sort: Time = 0.090857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.001857 s, Comparisons = 152407
  quick_sort_median_of_three_pivot: Time = 0.001429 s, Comparisons = 151973
  quick_sort_random_pivot: Time = 0.001571 s, Comparisons = 163961
Benchmarking N=10000, Type=reverse_sorted...
  bubble_sort: Time = 0.237714 s, Comparisons = 49995000
  heap_sort: Time = 0.002286 s, Comparisons = 226682
  insertion_sort: Time = 0.127000 s, Comparisons = 49995000
  merge_sort: Time = 0.003571 s, Comparisons = 64608
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 234923
  radix_sort: Time = 0.000571 s, Comparisons = 9999
  selection_sort: Time = 0.098857 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.168429 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.001286 s, Comparisons = 234923
  quick_sort_random_pivot: Time = 0.001571 s, Comparisons = 161961
Benchmarking N=10000, Type=sorted...
  bubble_sort: Time = 0.000143 s, Comparisons = 9999
  heap_sort: Time = 0.002429 s, Comparisons = 244460
  insertion_sort: Time = 0.000000 s, Comparisons = 9999
  merge_sort: Time = 0.003286 s, Comparisons = 69008
  quick_sort_median_of_three_pivot: Time = 0.001000 s, Comparisons = 131343
  radix_sort: Time = 0.000429 s, Comparisons = 9999
  selection_sort: Time = 0.086571 s, Comparisons = 49995000
  quick_sort_first_pivot: Time = 0.073143 s, Comparisons = 49995000
  quick_sort_median_of_three_pivot: Time = 0.000143 s, Comparisons = 131343
  quick_sort_random_pivot: Time = 0.000857 s, Comparisons = 151087
Benchmarking N=25000, Type=random...
  bubble_sort: Time = 1.812143 s, Comparisons = 312414347
  heap_sort: Time = 0.007714 s, Comparisons = 655052
  insertion_sort: Time = 0.397143 s, Comparisons = 156262378
  merge_sort: Time = 0.011143 s, Comparisons = 334228
  quick_sort_median_of_three_pivot: Time = 0.004571 s, Comparisons = 412579
  radix_sort: Time = 0.001714 s, Comparisons = 24999
  selection_sort: Time = 0.555857 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.004000 s, Comparisons = 424630
  quick_sort_median_of_three_pivot: Time = 0.003857 s, Comparisons = 412579
  quick_sort_random_pivot: Time = 0.004857 s, Comparisons = 418144
Benchmarking N=25000, Type=reverse_sorted...
  bubble_sort: Time = 1.357571 s, Comparisons = 312487500
  heap_sort: Time = 0.006000 s, Comparisons = 633719
  insertion_sort: Time = 0.795143 s, Comparisons = 312487500
  merge_sort: Time = 0.007857 s, Comparisons = 178756
  quick_sort_median_of_three_pivot: Time = 0.002714 s, Comparisons = 660758
  radix_sort: Time = 0.001429 s, Comparisons = 24999
  selection_sort: Time = 0.586143 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 1.164143 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.003714 s, Comparisons = 660758
  quick_sort_random_pivot: Time = 0.003000 s, Comparisons = 443707
Benchmarking N=25000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 24999
  heap_sort: Time = 0.006571 s, Comparisons = 677688
  insertion_sort: Time = 0.000286 s, Comparisons = 24999
  merge_sort: Time = 0.009714 s, Comparisons = 188476
  quick_sort_median_of_three_pivot: Time = 0.001714 s, Comparisons = 366397
  radix_sort: Time = 0.002000 s, Comparisons = 24999
  selection_sort: Time = 0.594000 s, Comparisons = 312487500
  quick_sort_first_pivot: Time = 0.274429 s, Comparisons = 312487500
  quick_sort_median_of_three_pivot: Time = 0.001000 s, Comparisons = 366397
  quick_sort_random_pivot: Time = 0.001143 s, Comparisons = 461717
Benchmarking N=50000, Type=random...
  bubble_sort: Time = 4.443429 s, Comparisons = 1249798879
  heap_sort: Time = 0.010286 s, Comparisons = 1409516
  insertion_sort: Time = 0.864143 s, Comparisons = 624039292
  merge_sort: Time = 0.011000 s, Comparisons = 718043
  quick_sort_median_of_three_pivot: Time = 0.004857 s, Comparisons = 879050
  radix_sort: Time = 0.001857 s, Comparisons = 49999
  selection_sort: Time = 1.193857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 0.004143 s, Comparisons = 967666
  quick_sort_median_of_three_pivot: Time = 0.003857 s, Comparisons = 879050
  quick_sort_random_pivot: Time = 0.004286 s, Comparisons = 921077
Benchmarking N=50000, Type=reverse_sorted...
  bubble_sort: Time = 2.889143 s, Comparisons = 1249975000
  heap_sort: Time = 0.006286 s, Comparisons = 1366047
  insertion_sort: Time = 1.635000 s, Comparisons = 1249975000
  merge_sort: Time = 0.006286 s, Comparisons = 382512
  quick_sort_median_of_three_pivot: Time = 0.003000 s, Comparisons = 1433133
  radix_sort: Time = 0.001429 s, Comparisons = 49999
  selection_sort: Time = 1.167857 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 2.033143 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002857 s, Comparisons = 1433133
  quick_sort_random_pivot: Time = 0.002000 s, Comparisons = 902571
Benchmarking N=50000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 49999
  heap_sort: Time = 0.006429 s, Comparisons = 1455438
  insertion_sort: Time = 0.000000 s, Comparisons = 49999
  merge_sort: Time = 0.006571 s, Comparisons = 401952
  quick_sort_median_of_three_pivot: Time = 0.001857 s, Comparisons = 782782
  radix_sort: Time = 0.001571 s, Comparisons = 49999
  selection_sort: Time = 1.068429 s, Comparisons = 1249975000
  quick_sort_first_pivot: Time = 1.024286 s, Comparisons = 1249975000
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 782782
  quick_sort_random_pivot: Time = 0.002000 s, Comparisons = 910163
Benchmarking N=75000, Type=random...
  bubble_sort: Time = 9.758000 s, Comparisons = 2812335744
  heap_sort: Time = 0.014143 s, Comparisons = 2200275
  insertion_sort: Time = 1.925143 s, Comparisons = 1406072739
  merge_sort: Time = 0.015714 s, Comparisons = 1121397
  quick_sort_median_of_three_pivot: Time = 0.006857 s, Comparisons = 1376114
  radix_sort: Time = 0.003571 s, Comparisons = 74999
  selection_sort: Time = 2.518429 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 0.007857 s, Comparisons = 1466857
  quick_sort_median_of_three_pivot: Time = 0.007286 s, Comparisons = 1376114
  quick_sort_random_pivot: Time = 0.007571 s, Comparisons = 1417559
Benchmarking N=75000, Type=reverse_sorted...
  bubble_sort: Time = 6.964714 s, Comparisons = 2812462500
  heap_sort: Time = 0.011857 s, Comparisons = 2138650
  insertion_sort: Time = 4.112714 s, Comparisons = 2812462500
  merge_sort: Time = 0.011286 s, Comparisons = 594612
  quick_sort_median_of_three_pivot: Time = 0.004429 s, Comparisons = 2272487
  radix_sort: Time = 0.002714 s, Comparisons = 74999
  selection_sort: Time = 3.078714 s, Comparisons = 2812462500
  quick_sort_first_pivot: Time = 5.474286 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.006000 s, Comparisons = 2272487
  quick_sort_random_pivot: Time = 0.004143 s, Comparisons = 1474721
Benchmarking N=75000, Type=sorted...
  bubble_sort: Time = 0.000000 s, Comparisons = 74999
  heap_sort: Time = 0.009857 s, Comparisons = 2268087
  insertion_sort: Time = 0.000143 s, Comparisons = 74999
  merge_sort: Time = 0.009571 s, Comparisons = 624316
  quick_sort_median_of_three_pivot: Time = 0.002143 s, Comparisons = 1195642
  quick_sort_first_pivot: Time = 2.648143 s, Comparisons = 2812462500
  quick_sort_median_of_three_pivot: Time = 0.002857 s, Comparisons = 1195642
  quick_sort_random_pivot: Time = 0.003714 s, Comparisons = 1432318
Benchmarking N=100000, Type=random...
  bubble_sort: Time = 26.387714 s, Comparisons = 4999913415
  heap_sort: Time = 0.021429 s, Comparisons = 3019574
  insertion_sort: Time = 3.670714 s, Comparisons = 2502704618
  merge_sort: Time = 0.025143 s, Comparisons = 1536282
  quick_sort_median_of_three_pivot: Time = 0.011714 s, Comparisons = 1924166
  radix_sort: Time = 0.004857 s, Comparisons = 99999
  selection_sort: Time = 5.085571 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 0.010714 s, Comparisons = 2115913
  quick_sort_median_of_three_pivot: Time = 0.010714 s, Comparisons = 1924166
  quick_sort_random_pivot: Time = 0.010286 s, Comparisons = 2006394
Benchmarking N=100000, Type=reverse_sorted...
  bubble_sort: Time = 12.516429 s, Comparisons = 4999950000
  heap_sort: Time = 0.013143 s, Comparisons = 2926640
  insertion_sort: Time = 6.979286 s, Comparisons = 4999950000
  merge_sort: Time = 0.012286 s, Comparisons = 815024
  quick_sort_median_of_three_pivot: Time = 0.006000 s, Comparisons = 3107283
  radix_sort: Time = 0.004143 s, Comparisons = 99999
  selection_sort: Time = 5.041571 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 9.247857 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.006571 s, Comparisons = 3107283
  quick_sort_random_pivot: Time = 0.007429 s, Comparisons = 2011616
Benchmarking N=100000, Type=sorted...
  bubble_sort: Time = 0.000286 s, Comparisons = 99999
  heap_sort: Time = 0.016000 s, Comparisons = 3112517
  insertion_sort: Time = 0.000286 s, Comparisons = 99999
  merge_sort: Time = 0.015286 s, Comparisons = 853904
  quick_sort_median_of_three_pivot: Time = 0.004000 s, Comparisons = 1665551
  radix_sort: Time = 0.003714 s, Comparisons = 99999
  selection_sort: Time = 4.650143 s, Comparisons = 4999950000
  quick_sort_first_pivot: Time = 4.057286 s, Comparisons = 4999950000
  quick_sort_median_of_three_pivot: Time = 0.003429 s, Comparisons = 1665551
  quick_sort_random_pivot: Time = 0.005143 s, Comparisons = 1949521

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
                 Bubble Sort         Random             100         0.000000                4859
                   Heap Sort         Random             100         0.000000                1016
              Insertion Sort         Random             100         0.000000                2766
                  Merge Sort         Random             100         0.000000                 547
Quick Sort (Median of Three)         Random             100         0.000000                 711
                  Radix Sort         Random             100         0.000000                  99
              Selection Sort         Random             100         0.000000                4950
                 Bubble Sort Reverse Sorted             100         0.000000                4950
                   Heap Sort Reverse Sorted             100         0.000000                 944
              Insertion Sort Reverse Sorted             100         0.000000                4950
                  Merge Sort Reverse Sorted             100         0.000143                 316
Quick Sort (Median of Three) Reverse Sorted             100         0.000000                 868
                  Radix Sort Reverse Sorted             100         0.000000                  99
              Selection Sort Reverse Sorted             100         0.000000                4950
                 Bubble Sort         Sorted             100         0.000000                  99
                   Heap Sort         Sorted             100         0.000000                1081
              Insertion Sort         Sorted             100         0.000000                  99
                  Merge Sort         Sorted             100         0.000143                 356
Quick Sort (Median of Three)         Sorted             100         0.000000                 669
                  Radix Sort         Sorted             100         0.000000                  99
              Selection Sort         Sorted             100         0.000000                4950
                 Bubble Sort         Random             500         0.001000              124747
                   Heap Sort         Random             500         0.000143                7424
              Insertion Sort         Random             500         0.000143               61475
                  Merge Sort         Random             500         0.000714                3864
Quick Sort (Median of Three)         Random             500         0.000143                5400
                  Radix Sort         Random             500         0.000000                 499
              Selection Sort         Random             500         0.000143              124750
                 Bubble Sort Reverse Sorted             500         0.000286              124750
                   Heap Sort Reverse Sorted             500         0.000286                7010
              Insertion Sort Reverse Sorted             500         0.000143              124750
                  Merge Sort Reverse Sorted             500         0.000000                2216
Quick Sort (Median of Three) Reverse Sorted             500         0.000000                6790
                  Radix Sort Reverse Sorted             500         0.000000                 499
              Selection Sort Reverse Sorted             500         0.000143              124750
                 Bubble Sort         Sorted             500         0.000000                 499
                   Heap Sort         Sorted             500         0.000143                7756
              Insertion Sort         Sorted             500         0.000000                 499
                  Merge Sort         Sorted             500         0.000143                2272
Quick Sort (Median of Three)         Sorted             500         0.000000                4263
                  Radix Sort         Sorted             500         0.000000                 499
              Selection Sort         Sorted             500         0.000429              124750
                 Bubble Sort         Random            1000         0.003000              498015
                   Heap Sort         Random            1000         0.000143               16911
              Insertion Sort         Random            1000         0.000429              246495
                  Merge Sort         Random            1000         0.000857                8733
Quick Sort (Median of Three)         Random            1000         0.000143               11016
                  Radix Sort         Random            1000         0.000143                 999
              Selection Sort         Random            1000         0.001000              499500
                 Bubble Sort Reverse Sorted            1000         0.003143              499500
                   Heap Sort Reverse Sorted            1000         0.000000               15965
              Insertion Sort Reverse Sorted            1000         0.001286              499500
                  Merge Sort Reverse Sorted            1000         0.000286                4932
Quick Sort (Median of Three) Reverse Sorted            1000         0.000000               15849
                  Radix Sort Reverse Sorted            1000         0.000000                 999
              Selection Sort Reverse Sorted            1000         0.000714              499500
                 Bubble Sort         Sorted            1000         0.000000                 999
                   Heap Sort         Sorted            1000         0.000000               17583
              Insertion Sort         Sorted            1000         0.000000                 999
                  Merge Sort         Sorted            1000         0.000286                5044
Quick Sort (Median of Three)         Sorted            1000         0.000143                9520
                  Radix Sort         Sorted            1000         0.000000                 999
              Selection Sort         Sorted            1000         0.001286              499500
                 Bubble Sort         Random            5000         0.049143            12494260
                   Heap Sort         Random            5000         0.001143              107630
              Insertion Sort         Random            5000         0.017714             6302243
                  Merge Sort         Random            5000         0.001857               55242
Quick Sort (Median of Three)         Random            5000         0.001143               69275
                  Radix Sort         Random            5000         0.000571                4999
              Selection Sort         Random            5000         0.022714            12497500
                 Bubble Sort Reverse Sorted            5000         0.053286            12497500
                   Heap Sort Reverse Sorted            5000         0.001429              103227
              Insertion Sort Reverse Sorted            5000         0.031429            12497500
                  Merge Sort Reverse Sorted            5000         0.001714               29804
Quick Sort (Median of Three) Reverse Sorted            5000         0.000571              106182
                  Radix Sort Reverse Sorted            5000         0.000571                4999
              Selection Sort Reverse Sorted            5000         0.023000            12497500
                 Bubble Sort         Sorted            5000         0.000000                4999
                   Heap Sort         Sorted            5000         0.001429              112126
              Insertion Sort         Sorted            5000         0.000000                4999
                  Merge Sort         Sorted            5000         0.002429               32004
Quick Sort (Median of Three)         Sorted            5000         0.000143               60678
                  Radix Sort         Sorted            5000         0.000143                4999
              Selection Sort         Sorted            5000         0.023857            12497500
                 Bubble Sort         Random           10000         0.240143            49986089
                   Heap Sort         Random           10000         0.003571              235292
              Insertion Sort         Random           10000         0.068000            25149713
                  Merge Sort         Random           10000         0.004857              120453
Quick Sort (Median of Three)         Random           10000         0.002000              151973
                  Radix Sort         Random           10000         0.000571                9999
              Selection Sort         Random           10000         0.090857            49995000
                 Bubble Sort Reverse Sorted           10000         0.237714            49995000
                   Heap Sort Reverse Sorted           10000         0.002286              226682
              Insertion Sort Reverse Sorted           10000         0.127000            49995000
                  Merge Sort Reverse Sorted           10000         0.003571               64608
Quick Sort (Median of Three) Reverse Sorted           10000         0.001286              234923
                  Radix Sort Reverse Sorted           10000         0.000571                9999
              Selection Sort Reverse Sorted           10000         0.098857            49995000
                 Bubble Sort         Sorted           10000         0.000143                9999
                   Heap Sort         Sorted           10000         0.002429              244460
              Insertion Sort         Sorted           10000         0.000000                9999
                  Merge Sort         Sorted           10000         0.003286               69008
Quick Sort (Median of Three)         Sorted           10000         0.001000              131343
                  Radix Sort         Sorted           10000         0.000429                9999
              Selection Sort         Sorted           10000         0.086571            49995000
                 Bubble Sort         Random           25000         1.812143           312414347
                   Heap Sort         Random           25000         0.007714              655052
              Insertion Sort         Random           25000         0.397143           156262378
                  Merge Sort         Random           25000         0.011143              334228
Quick Sort (Median of Three)         Random           25000         0.004571              412579
                  Radix Sort         Random           25000         0.001714               24999
              Selection Sort         Random           25000         0.555857           312487500
                 Bubble Sort Reverse Sorted           25000         1.357571           312487500
                   Heap Sort Reverse Sorted           25000         0.006000              633719
              Insertion Sort Reverse Sorted           25000         0.795143           312487500
                  Merge Sort Reverse Sorted           25000         0.007857              178756
Quick Sort (Median of Three) Reverse Sorted           25000         0.002714              660758
                  Radix Sort Reverse Sorted           25000         0.001429               24999
              Selection Sort Reverse Sorted           25000         0.586143           312487500
                 Bubble Sort         Sorted           25000         0.000000               24999
                   Heap Sort         Sorted           25000         0.006571              677688
              Insertion Sort         Sorted           25000         0.000286               24999
                  Merge Sort         Sorted           25000         0.009714              188476
Quick Sort (Median of Three)         Sorted           25000         0.001714              366397
                  Radix Sort         Sorted           25000         0.002000               24999
              Selection Sort         Sorted           25000         0.594000           312487500
                 Bubble Sort         Random           50000         4.443429          1249798879
                   Heap Sort         Random           50000         0.010286             1409516
              Insertion Sort         Random           50000         0.864143           624039292
                  Merge Sort         Random           50000         0.011000              718043
Quick Sort (Median of Three)         Random           50000         0.004857              879050
                  Radix Sort         Random           50000         0.001857               49999
              Selection Sort         Random           50000         1.193857          1249975000
                 Bubble Sort Reverse Sorted           50000         2.889143          1249975000
                   Heap Sort Reverse Sorted           50000         0.006286             1366047
              Insertion Sort Reverse Sorted           50000         1.635000          1249975000
                  Merge Sort Reverse Sorted           50000         0.006286              382512
Quick Sort (Median of Three) Reverse Sorted           50000         0.003000             1433133
                  Radix Sort Reverse Sorted           50000         0.001429               49999
              Selection Sort Reverse Sorted           50000         1.167857          1249975000
                 Bubble Sort         Sorted           50000         0.000000               49999
                   Heap Sort         Sorted           50000         0.006429             1455438
              Insertion Sort         Sorted           50000         0.000000               49999
                  Merge Sort         Sorted           50000         0.006571              401952
Quick Sort (Median of Three)         Sorted           50000         0.001857              782782
                  Radix Sort         Sorted           50000         0.001571               49999
              Selection Sort         Sorted           50000         1.068429          1249975000
                 Bubble Sort         Random           75000         9.758000          2812335744
                   Heap Sort         Random           75000         0.014143             2200275
              Insertion Sort         Random           75000         1.925143          1406072739
                  Merge Sort         Random           75000         0.015714             1121397
Quick Sort (Median of Three)         Random           75000         0.006857             1376114
                  Radix Sort         Random           75000         0.003571               74999
              Selection Sort         Random           75000         2.518429          2812462500
                 Bubble Sort Reverse Sorted           75000         6.964714          2812462500
                   Heap Sort Reverse Sorted           75000         0.011857             2138650
              Insertion Sort Reverse Sorted           75000         4.112714          2812462500
                  Merge Sort Reverse Sorted           75000         0.011286              594612
Quick Sort (Median of Three) Reverse Sorted           75000         0.004429             2272487
                  Radix Sort Reverse Sorted           75000         0.002714               74999
              Selection Sort Reverse Sorted           75000         3.078714          2812462500
                 Bubble Sort         Sorted           75000         0.000000               74999
                   Heap Sort         Sorted           75000         0.009857             2268087
              Insertion Sort         Sorted           75000         0.000143               74999
                  Merge Sort         Sorted           75000         0.009571              624316
Quick Sort (Median of Three)         Sorted           75000         0.002143             1195642
                  Radix Sort         Sorted           75000         0.002000               74999
              Selection Sort         Sorted           75000         2.967143          2812462500
                 Bubble Sort         Random          100000        26.387714          4999913415
                   Heap Sort         Random          100000         0.021429             3019574
              Insertion Sort         Random          100000         3.670714          2502704618
                  Merge Sort         Random          100000         0.025143             1536282
Quick Sort (Median of Three)         Random          100000         0.011714             1924166
                  Radix Sort         Random          100000         0.004857               99999
              Selection Sort         Random          100000         5.085571          4999950000
                 Bubble Sort Reverse Sorted          100000        12.516429          4999950000
                   Heap Sort Reverse Sorted          100000         0.013143             2926640
              Insertion Sort Reverse Sorted          100000         6.979286          4999950000
                  Merge Sort Reverse Sorted          100000         0.012286              815024
Quick Sort (Median of Three) Reverse Sorted          100000         0.006000             3107283
                  Radix Sort Reverse Sorted          100000         0.004143               99999
              Selection Sort Reverse Sorted          100000         5.041571          4999950000
                 Bubble Sort         Sorted          100000         0.000286               99999
                   Heap Sort         Sorted          100000         0.016000             3112517
              Insertion Sort         Sorted          100000         0.000286               99999
                  Merge Sort         Sorted          100000         0.015286              853904
Quick Sort (Median of Three)         Sorted          100000         0.004000             1665551
                  Radix Sort         Sorted          100000         0.003714               99999
              Selection Sort         Sorted          100000         4.650143          4999950000

Full results table saved to graphs\csv_data\all_sorting_benchmark_results.csv

--- Correlation Analysis Summary ---
Algorithm                           | Correlation (r) | P-value
----------------------------------------------------------------------
Bubble Sort                         |          0.9322 | 1.5655e-12
Heap Sort                           |          0.9535 | 1.5871e-14
Insertion Sort                      |          0.9985 | 4.0813e-33
Merge Sort                          |          0.9516 | 2.5401e-14
Quick Sort (Median of Three)        |          0.7797 | 1.6375e-06
Radix Sort                          |          0.9564 | 7.0517e-15
Selection Sort                      |          0.9963 | 4.0734e-28

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