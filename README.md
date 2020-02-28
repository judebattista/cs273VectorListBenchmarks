# Benchmarking container classes #
**source.cpp** contains a series of tests intended to exercise a variety of functions on your container classes.  
In its initial state, these tests execute against the stl::vector and stl::list classes, comparing their benchmarks.

## Testing your own container classes ##
Simply replace the using statements on lines 15 and 16 of **benchmark.h** with using statements that reference your containers.  
This likely takes the following form: 
``` 
using cs273::vector;  
using cs273::list;  
```

## Testing sets ##
You will notice that **source.cpp** uses two different testing sets. `target` and `orderOfSearchSpace` are several orders of magnitude larger than `smallTarget` and `orderOfSmallSpace`. Some of the operations under test are computationally expensive. Passing them the smaller parameters allows the tests to execute more quickly, making the development process more fluid. Once you are convinced that your own containers work the way you want them to, you can switch to the larger parameters in order to get proportionally correct tests.
1. Lines 31-34: replace `orderOfSmallSpace` with `orderOfSearchSpace`
2. Lines 38-41: replace `orderOfSmallSpace` with `orderOfSearchSpace`
3. Lines 51-54: replace `orderOfSmallSpace` with `orderOfSearchSpace` and `smallTarget` with `target`
4. Lines 58-61: replace `orderOfSmallSpace` with `orderOfSearchSpace` and `smallTarget` with `target`  

If the default testing sets prove too slow on your machine, feel free to create smaller test sets to speed up your development cycle.