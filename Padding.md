## simplified setting：

* 2-D discrete convolutions (N = 2)
* square inputs ($i_1$ =$ i_2$ = $i$),
* square kernel size ($k_1$ =$ k_2$ = $k$)
* same strides along both axes ($s_1$ =$ s_2$ = $s$)
* same zero padding along both axes ($p_1$ =$ p_2$ = $p$)

### Unit strides ( for $s = 1$ )

1. No zero padding

   **Relationship 1.** For any $i$ and $k$, and $p = 0$, 

$$
o = (i − k) + 1
$$

2. Zero padding

   **Relationship 2.** For any $i$, $k$ and $p$,

$$
o = (i − k) + 2p + 1
$$
> **Half (same) padding**
> **Relationship 3. **For any $i$ and for $k$ odd ($k = 2n + 1, n ∈ N$), $p = \lfloor \frac{k}{2} \rfloor = n$, 
> $$
> o = i + \lfloor \frac{k}{2} \rfloor − (k − 1) = i + 2n − 2n = i
> $$
> **Full padding**
>
> **Relationship 4.** For any $i$ and $k$, and for $p = k − 1$, 
> $$
> o = i + 2(k − 1) − (k − 1) = i + (k − 1).
> $$

### Non-nit strides ( for $s > 1$ )

1. No zero padding

   **Relationship 5.** For any $i$ and $k$, and $p = 0$, 

$$
o = \lfloor \frac{i − k}{s} \rfloor + 1
$$

2. Zero padding

   **Relationship 6.** For any $i$, $k$ and $p$,

$$
o = \lfloor \frac{i + 2p − k}{s} \rfloor + 1
$$



## Reference:

[1] Dumoulin V, Visin F. A guide to convolution arithmetic for deep learning[J/OL]. arXiv:1603.07285 [cs, stat], 2016[2021–10–30]. http://arxiv.org/abs/1603.07285.
