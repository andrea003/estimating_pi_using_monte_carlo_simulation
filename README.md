# How to Estimate pi Using Monte Carlo Simulation in R

The idea behind the simulation is to simulate random (x, y) points within a two-dimensional Cartesian coordinate system where the domain is a circle and its bounding square. 

As the area of a circle is calculated by pi * r^2, and the area of the bounding square is (2r)^2 = 4r^2. Dividing the area of the circle by the area of the square we get pi/4.

This means we can estimate pi using the formula: pi = 4 * simulated points within circle / total number of simulated points.

By simulating random numbers within this square, we get estimated values for the area of the circle and the area of the square. Hence we can estimate pi by calculating the ratio of simulated points that fall within the circle and total number of simulated points. 

To identify which points fall within the circle we use the equation of the circle: 

(x-a)^2+(y-b)^2 = r^2, where (a, b) is the circle center.  

In our example the circle center is $(0, 0)$ and the radius is 1, so simulated points that satisfy sqrt((x-a)^2+(y-b)^2) <= 1 are within the circle. 
