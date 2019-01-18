# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0
    while (a < n * n * n) 
      a = a + n * n
```
O(N^3)
```
b)  sum = 0
    for (i = 0; i < n; i++)
      for (j = i + 1; j < n; j++)
        for (k = j + 1; k < n; k++)
          for (l = k + 1; l < 10 + k; l++)
            sum++
O(N^3) maybe a little more. the + 10 adds a constant value 
that will cause it to run over n^3  but not enough to call it 
N^4 
```

```
c)  bunnyEars = function(bunnies) {
      if (bunnies == 0) return 0
      return 2 + bunnyEars(bunnies-1)
    }

    O(n) if bunnies is 0 1 operation  if bunnies is 5  there will be 5 operations and  so on and so on operations match bunnies.
```

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also
that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get
broken if dropped off a floor less than floor _f_. Devise a strategy to
determine the value of _f_ such that the number of dropped eggs is minimized.


def find_level (levels, target, min_level, high_level):
  
  mid = (min_level + high_level) // 2 
  if len(arr) == 0:
    return -1  #doesn't break at all. 
  if levels[mid] == target:
    return target
  elif levels[mid] < target: 
    arr = levels[:mid]
    high_level = mid -1 
    find_level(arr, target, min_level, high_level)
  elif levels[mid] > target:
    arr = levels[mid+1:]
    min_level = mid + 1 
    find_level(arr, target, min_level, high_level)
binary search problem

