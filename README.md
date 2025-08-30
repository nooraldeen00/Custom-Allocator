# ⚙️ Custom-Allocator
<img width="300" height="300" alt="Custom-Allocator" src="https://github.com/user-attachments/assets/bfe9038d-a182-4b2e-aa61-dcca797bf9a5" />

A custom memory allocator written in C that re-implements malloc, free, calloc, and realloc.
The project demonstrates low-level heap management, pointer arithmetic, and memory optimization strategies, benchmarked against the standard malloc() provided by the C library.

# 📖 About the Project

This allocator was built as part of a systems programming assignment to understand how memory management works under the hood.

## The implementation:

- Provides four allocation strategies: First Fit, Next Fit, Best Fit, Worst Fit

- Implements splitting and coalescing of free blocks to reduce fragmentation

- Tracks detailed statistics (mallocs, frees, reuses, splits, coalesces, heap growth, fragmentation)

- Benchmarks performance against the standard malloc()

## This project demonstrates strong skills in:

- 🔧 Systems-level programming in C

- 🧮 Pointer arithmetic and heap manipulation

- ⚡ Performance benchmarking and analysis

- 🐞 Debugging with GDB and memory tracing

# 🚀 Features

- ✅ First Fit, Next Fit, Best Fit, Worst Fit allocator strategies

- 🔄 Splitting and Coalescing free blocks to reduce fragmentation

- 📊 Statistics tracking (mallocs, frees, splits, coalesces, heap growth, fragmentation)

- 🧩 Implemented malloc, free, calloc, and realloc

- 🧪 Benchmarking suite to compare custom allocators with system malloc()

- 🐛 Integrated debugging workflow with GDB + LD_PRELOAD

# 🛠️ Tech Stack

- Language: C (compiled on Linux Codespaces)

- Build: GNU Make + provided Makefile

- Debugging: GDB, Valgrind-style tracing

- Testing: Custom allocator test suite (ffnf, bfwf, test1–4)

# ▶️ Building and Running

## 🔨 Build
make

## ▶️ Run Tests
Each allocator compiles into its own shared library. Use LD_PRELOAD to override system malloc:

## First Fit
env LD_PRELOAD=lib/libmalloc-ff.so tests/ffnf  

## Best Fit
env LD_PRELOAD=lib/libmalloc-bf.so tests/bfwf  

## Next Fit
env LD_PRELOAD=lib/libmalloc-nf.so tests/test1  

## Worst Fit
env LD_PRELOAD=lib/libmalloc-wf.so tests/test2  

# 📊 Example Statistics Output

mallocs: 8  
frees: 8  
reuses: 1  
grows: 5  
splits: 1  
coalesces: 1  
blocks: 5  
requested: 7298  
max heap: 4096  

# 🎯 Learning Outcomes

- Through this project, I gained hands-on experience in:

- Implementing a real allocator with C and pointer arithmetic

- Debugging segmentation faults with GDB & exec-wrappers

- Designing memory management strategies

- Benchmarking custom allocators vs system malloc

- Evaluating trade-offs in performance and fragmentation

# 🚀 Future Enhancements

- 🧮 Add buddy allocation system

- 📂 Integrate Valgrind-style leak detection

- 🧩 Add thread safety with locks for multi-threaded programs
