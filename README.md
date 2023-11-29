# Rasterization-Algorithms-QT documentation

## Intro
This cross-platform QT application rasterizes segments and curves using the following algorithms: Naive algorithm, DDA-line, Bresenham's segment algorithm, Bresenham's circle algorithm.

## Installing
To start using the app you should just download the archive "executable" from this repozitory to your computer, unzip it and run the .exe file.

## Examples of algorithms

### Naive algorithm

x1=1, x2=-3, y1=4, y2=9

dx  = x2-x1 =-4; dy =y2-y1=5

a = dx/dy = -0.8

x =1, y = 4

**iterations**

_1
_
**point(1,4)**

y:=5 x:= 0,2

_2_

**point(0,5)**

y:=6 x:= -0,6

_3_

**point(-1,6)**

y:=7 x:= -1,4

_4_

**point(-1,7)**

y:=8 x:= -2.2

_5_

**point(-2,8)**

y:=9 x:= -3

_6_

**point(-3,9)**

### DDA line

x1=1, x2=-3, y1=4, y2=9

L = max(|x1-x2|,|y1-y2|) = 5

**iterations**

_1_

x = round(1+0*(-3-1)/5) = 1

y = round(4+0*(9-5)/5) = 4

**point(1,4)**

_2_

x = round(1+1*(-3-1)/5) = 0

y = round(4+1*(9-5)/5) = 5

**point(0,5)**

_3_

x = round(1+2*(-3-1)/5) = -1

y = round(4+2*(9-5)/5) = 6

**point(-1,6)**

_4_

x = round(1+3*(-3-1)/5) = -1

y = round(4+3*(9-5)/5) = 7

**point(-1,7)**

_5_

x = round(1+4*(-3-1)/5) = -2

y = round(4+4*(9-5)/5) = 8

**point(-2,8)**

_6_

x = round(1+5*(-3-1)/5) = -3

y = round(4+5*(9-5)/5) = 9

**point(-3,9)**

###  Bresenham's segment algorithm

x1=0, x2=4, y1=0, y2=3

**point(0,0)**

**iterations**

_1_

d = 2*3-4 = 2 => deltay = 1

**point(0+1,0+1) = (1,1)**

_2_

d = 2+ 2*3-2*4 = 0 => deltay = 1

**point(1+1,1+1) = (2,2)**

_3_

d = 0+ 2*3-2*4= -2 => deltay = 0

**point(2+1,2+0) = (3,2)**

_4_

d = -2+ 2*3= 4 => deltay = 1

**point(3+1,2+1) = (4,3)**

###  Bresenham's circle algorithm

x0=0, y0=0, r=4
x =0; y = 4
**point(0,4)**

**point(0,-4)**

**point(4,0)**

**point(-4,0)**


_1_

dg = (0+1)*(0+1)+4*4-4*4 = 1

dd = (0+1)*(0+1)+(4-1)*(4-1)-4*4 = -6

|dg|<|dd|

x= 1
y= 4

**point(1,4)**

**point(1,-4)**

**point(-1,4)**

**point(-1,-4)**

**point(4,1)**

**point(-4,1)**

**point(4,-1)**

**point(-4,-1)**

_2_

dg = (1+1)*(1+1)+4*4-4*4 = 4

dd = (1+1)*(1+1)+(4-1)*(4-1)-4*4 = -3

|dg|>|dd|

x= 2
y= 3

**point(2,3)**

**point(2,-3)**

**point(-2,3)**

**point(-2,-3)**

**point(3,2)**

**point(-3,2)**

**point(3,-2)**

**point(-3,-2)**

_3_

dg = (2+1)*(2+1)+3*3-4*4 = 2

dd = (2+1)*(2+1)+(3-1)*(3-1)-4*4 = -3

|dg|<|dd|

x= 3
y= 3

**point(3,3)**

**point(3,-3)**

**point(-3,3)**

**point(-3,-3)**








