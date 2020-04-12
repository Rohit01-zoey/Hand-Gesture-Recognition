# Hand-Gesture-Recognition

The following code helps in finding convexity defects in the given img( in our case is the video shot
from the laptop) and helps in marking them.So, the contour of max area is marked by green, while
the "furthest point" of the Convexhull is marked by a red dot.The defects object stores the coordinates
of the start and end of the contour, the farthest point and approximately the distance to this point.
We use this to find 'start', 'end' and 'far' points amd thus a triangle is formed. 'angle' stores the
angle (in degrees) opposite to the side formed the 'start' and 'end' points.To get the 'angle' in degrees
we essentially need to multiply its value in radians(math.acos returns angle in radians)
by 180/pi which roughly is 57. 

Thus, now we have that if this 'angle' is less than 90, then its a so-called defect. After this, the code demands
we add different text to our image governed by the number of defects in our image.
