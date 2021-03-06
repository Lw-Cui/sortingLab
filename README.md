# Sorting Laboratory #

## Introduction ##
This is a tiny project assigned by `Data structure and algorithm` course at `Harbin Institute of Technology`. We were asked to complement some sorting algorithms including `quick sort`, `heap sort`, `selection sort` and so on. Performance comparson is preferred.

## Feature ##
To make the program scalable I use `shared object` file to implement algorithm. Any algs implementing the interface should work with this program without issue. The interface is in the `sortingLab/sortAlgs/interface.hpp`:
```
void sort(std::vector<int> &);
const char *self();
```
The first implement algs while the second show its info.

## Usage ##
* In subdirectory `sortAlgs` of this repository please execute `cmake . && make` command.


Then in the root directory of this repo you could type `make`.
The executable file built by `Makefile` will search the subdir `lib` in repo and dynamically load `lib(\w+).so` object.
You could specify different distribution to test algorithm performance by adding compile option `-DPOISSON` or `-DBINOMIAL`(default is uniform distribution).

 * Result
```
For 10000 integers
    Quick sort is 1.27 times faster than Qsort(3 way)
    Qsort(3 way) is 1.04 times faster than Merge sort
    Merge sort is 1.00 times faster than Radix sort
    Radix sort is 1.02 times faster than Shell sort
    Shell sort is 1.18 times faster than Heap sort
    Heap sort is 57.43 times faster than Insertion sort
    Insertion sort is 3.75 times faster than Bubble sort

For 30000 integers
    Radix sort is 1.01 times faster than Quick sort
    Quick sort is 1.11 times faster than Qsort(3 way)
    Qsort(3 way) is 1.11 times faster than Merge sort
    Merge sort is 1.11 times faster than Shell sort
    Shell sort is 1.10 times faster than Heap sort
    Heap sort is 148.07 times faster than Insertion sort
    Insertion sort is 3.89 times faster than Bubble sort
	....
```
