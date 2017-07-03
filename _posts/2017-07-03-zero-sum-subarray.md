---
layout: post
title: Pair Sums In An Array
categories: []
tags: [04. array algorithms]
description:
comments: true
---

### Q: Given an array find a pair of element with the given sum.

#### Input:

```python3
a = [0, 1, -1, 4, 2, -3, -1, 0, 4]
```

#### Output:

```python3
[0]
[0, 1, -1]
[1, -1]
[0]
[-3, -1, 0, 4]
```

#### Algorithms:

* Logic:
  * Hash sums and ending indices.
  * If a sum is seen previously then the elements in between sum to 0.

```python3
a = [0, 1, -1, 4, 2, -3, -1, 0, 4]
sum_idx = {}
s = 0
for i in range(len(a)):
    s = s + a[i]
    l = sum_idx.get(s, [])
    if s == 0:
        [print(a[: i+1])]
    [print(a[j+1: i+1]) for j in l]   
    l.append(i)
    sum_idx[s] = l
```

## REFERENCES:

<small>[500 Data Structures and Algorithms practice problems and their solutions](https://techiedelight.quora.com/500-Data-Structures-and-Algorithms-practice-problems-and-their-solutions){:target="_blank"}</small>
<small>[Find sub-array with 0 sum](http://www.techiedelight.com/find-sub-array-with-0-sum/){:target="_blank"}</small>