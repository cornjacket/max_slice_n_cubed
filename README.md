# max_slice_n_cubed
Find the max sum slice of an array. Simple algorithm with Big O of n cubed to illustrate concept.

Try it out at https://jsbin.com/qufiqo/edit?js,console


Write a max_slice function that takes an array of integers as input and returns the slice with the largest sum of elements.

# some examples:
[1,2,3] => [1,2,3]
[1,-2,3] => [3]
[1,-2,3, 4] => [3, 4]
[-1,-2,-3] => [-1]

Walk-thru

The algorithm uses a brute force double iteration in order to visit every starting element of the input array and every potential slice end point and calculates the max sum for every possible slice.

The algorithm starts by setting the max_sum to be the first element of the input array.

The outer loop visits each element of the input array as a starting point for a potential slice. The inner loop visits each starting point as well as all the elements following the starting point as an ending point for a potential slice. This creates all possible slices. Then the algoritm calculates the sum of the slice (potential_max_sum) and compares to the current max_sum.

The outer and inner loops create an n squared timing function, and the call to sum makes the entire algorithm run at n cubed. This is not an efficient algorithm.