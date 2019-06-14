Add your answers to the Algorithms exercises here.

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```
a)  a = 0                           O(1)
    while (a < n * n * n):          O(n)
      a = a + n * n                 O(1)
```
Solution: O(n)

```
b)  sum = 0
    for i in range(n):                      O(n)
      i += 1
      for j in range(i + 1, n):             O(n)
        j += 1
        for k in range(j + 1, n):           O(n)
          k += 1
          for l in range(k + 1, 10 + k):    O(n)
            l += 1
            sum += 1
```
Solution: O(n^4)

```
c)  def bunnyEars(bunnies):             O(1)
      if bunnies == 0:                  O(1)
        return 0                        O(1)

      return 2 + bunnyEars(bunnies-1)   O)(n)
```
Solution: O(n)

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

I would start at half of n and drop an egg, then I would continue to half it and drop an egg going up or down based on if the egg cracks or doesnt until I find __f__.

This is the "divide and concor" strategy and the big O for it is log(n)