# Sito_Eratostenesa_algoritm

Wyznaczenie ciągu liczb pierwszych z przedziału n, zrealizowane za pomocą algorytmu Sito Eratostenesa

### Method one
```py
def sito_algoritm2(n):

    _all = [x for x in range(1, n+1)]

    sito_step1 = [_all.remove(x1) for x1 in _all if (x1 % 2) == 0 and x1 != 2]
    sito_step2 = [_all.remove(x2) for x2 in _all if (x2 % 3) == 0 and x2 != 3]
    sito_step3 = [_all.remove(x3) for x3 in _all if (x3 % 5) == 0 and x3 != 5]
    sito_step4 = [_all.remove(x4) for x4 in _all if (x4 % 7) == 0 and x4 != 7]

    return _all
```

## Method two
```py
def sito_algoritm1(n):

    _all = set([a for a in range(1, n+1)])
    step_by2 = [x1 for x1 in range(4, n+1, 2)]
    step_by3 = [x2 for x2 in range(6, n+1, 3)]
    step_by5 = [x3 for x3 in range(10, n+1, 5)]
    step_by7 = [x4 for x4 in range(14, n+1, 7)]
    s_sum = set(step_by2 + step_by3 + step_by5 + step_by7)
    prime_num = s_sum.symmetric_difference(_all)

    return prime_num
```

![image](https://user-images.githubusercontent.com/111123372/200661732-eedfd5ef-70e7-4b49-96f4-5cb28b5ccfd9.png)


