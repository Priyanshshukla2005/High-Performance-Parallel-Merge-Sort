# High-Performance Parallel Merge Sort ⚡⚡

A multithreaded merge sort implementation with performance benchmarking using [Google Benchmark](https://github.com/google/benchmark).  
Visualize the speedup and efficiency of multithreaded sorting with auto-generated graphs.

---
## Author

Priyansh Shukla  
B.Tech CSE, Bennett University

---

## Features

- **Multiple Merge Sort Variants**
  - Standard library sort (for reference)
  - Classic sequential merge sort
  - Naive parallel merge sort (spawns a thread at each recursive call)
  - OpenMP optimized merge sort
  - Parallel merge sort using custom thread pools with load balancing
- **Thread Pool Implementation**
  - Efficient task management with minimal thread creation overhead
  - Safe queueing and graceful shutdown
- **Benchmarking**
  - Uses Google Benchmark to compare performance across implementations and input sizes
  - Exporting of benchmark results to CSV / JSON formats
- **Visualization**
  - Python plotting script to analyze and compare timing results, both in normal and logarithmic scale

---

## Installation

### 1. Clone this repository
```bash
git clone https://github.com/Priyanshshukla2005/High-Performance-Parallel-Merge-Sort.git
cd High-Performance-Parallel-Merge-Sort
```

---

## Build & Run

### Compile the program using the makefile (Ensure Google Benchmark and OpenMP are installed):
```bash
make
```

### Run the benchmark and export results:
```bash
./merge_sort --benchmark_format=json > benchmark.json
```

---

## Plot the Benchmark

Use the provided Python script to generate graphs:

```bash
python3 plot.py -f benchmark.json
```

### Output Visualization

#### Linear Scale
![Benchmark Graph - Linear Scale](output_log.png)

#### Logarithmic Scale
![Benchmark Graph - Logarithmic Scale](output.png)

---

## Files

| File             | Description                                        |
|------------------|----------------------------------------------------|
| `merge_sort.cpp` | Core multithreaded merge sort logic                |
| `thread_pool.h`  | ThreadPool with task queue + synchronisation logic |
| `plot.py`        | Graphs runtime from benchmark results file         |
| `benchmark.csv`  | Output benchmark (auto-generated)                  |

---
