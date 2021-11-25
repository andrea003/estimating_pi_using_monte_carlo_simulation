# How to Estimate pi Using Monte Carlo Simulation in R

The idea behind the simulation is to simulate random numbers from the uniform distribution within a coordinate system representing a 
square, in this case the first quadrant. By identifying the points that fall within the quarter circle, with the circle's radius being the square's side length, 
we can estimate pi. 

## Area of the circle
`circle area` = pi * radius^2.   
`pi` = A / radius^2.   

Note here that radius^2 is also the area of the quadrant. We will simulate points to fall within this square, some of which will fall within the area of the quarter circle/under the curve. Since we will only look at the first quadrant in this case, we will use:

`Q` = 1/4 * circle area.  
`pi` = 4 * Q / radius^2, where radius^2 is estimated by the total number of simulated data points.

## Finding the curve
To decide if the simulated points fall within the area under the curve, we apply the equation of the circle:  

(x - a)^2 + (y - b)^2, where (a, b) is the centre of the circle.  

Will identify the points that satisfy sqrt(x^2 + y^2) <= 1

