# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

T(n/13) + 5 

(T(n/13) +5) +5 = T(n/13) +10

T(n/13) + 5 +10 = T(n/13) + 15

T(n) = $T(n/13^i)$+ 5i

i = log13n

T(n) = $T(n/13^i)$+ 5i

T(n) = $T(n/13^{log13n})$+ 5(log13n)

T(n) = 1 + 5(log13n)
ends up being O(log13n)

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n) = 13(13T (n/13) +5) +5$

$T(n) = 169T(n/13) + 70$

$T(n) = 169(13T(n/2197) +5) +70$

$T(n) = 2197T(n/2197) +915$

$T(n) =13^i T(n/13^i)+ 5(13^{i-1}+ 13^{i-2}+ ..+13 +1)$

$n/13^i$ = 1

i = log13n
​
T(1) = x, x is a constant

$T(n) = 1 + (5(13^i -1))/12$
 which simplifies to O(n)

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

$T(n) = 13(13T (n/13) +2(n/13)) +2n$

$T(n) = 169T(n/13) + $

$T(n) = 169(13T(n/2197) +2n) +28n^2$

$T(n) = 2197T(n/2197) +366n^3$

$T(n) =13^i T(n/13^i)+ 5(13^{i-1}+ 13^{i-2}+ ..+13 +1)$

$n/13^i$ = 1

i = log13n

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”
