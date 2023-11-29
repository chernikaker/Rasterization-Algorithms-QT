# Rasterization-Algorithms-QT documentation

## Intro
This cross-platform QT application rasterizes segments and curves using the following algorithms: Naive algorithm, DDA-line, Bresenham's segment algorithm, Bresenham's circle algorithm.

## Algorithms

### Naive algorithm

**Example:**

x1=1, x2=-3, y1=4, y2=9

dx  = x2-x1 =-4; dy =y2-y1=5

a = dx/dy = -0.8

x =1, y = 4

**iterations**

1

**point(1,4)**

y:=5 x:= 0,2

2

**point(0,5)**

y:=6 x:= -0,6

3

**point(-1,6)**

y:=7 x:= -1,4

4

**point(-1,7)**

y:=8 x:= -2.2

5

**point(-2,8)**

y:=9 x:= -3

6

**point(-3,9)**

### DDA line

**Example:**

x1=1, x2=-3, y1=4, y2=9

L = max(|x1-x2|,|y1-y2|) = 5

**iterations**

1

x = round(1+0*(-3-1)/5) = 1

y = round(4+0*(9-5)/5) = 4

**point(1,4)**

2

x = round(1+1*(-3-1)/5) = 0

y = round(4+1*(9-5)/5) = 5

**point(0,5)**

3

x = round(1+2*(-3-1)/5) = -1

y = round(4+2*(9-5)/5) = 6

**point(-1,6)**

4

x = round(1+3*(-3-1)/5) = -1

y = round(4+3*(9-5)/5) = 7

**point(-1,7)**

5

x = round(1+4*(-3-1)/5) = -2

y = round(4+4*(9-5)/5) = 8

**point(-2,8)**

5

x = round(1+5*(-3-1)/5) = -3

y = round(4+5*(9-5)/5) = 9

**point(-3,9)**
