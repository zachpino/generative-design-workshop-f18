### Simple Walker in Python

[Agent-Based Modeling](https://en.wikipedia.org/wiki/Agent-based_model) is in many ways the opposite of the evolutionary form finding and simulated formal development discussed previously. 

Rather than the designer thinking about an idealized *final outcome* to minimize or maximize, an agent-based modeling approach allows the designers to specifically define the parameters and abilities of an agent — and then observe how that agent exists autonomously given what it can do. An individual is defined, and then *outcomes emerge*. Designing in this way is often termed *Generative Design* because the design, in many meaningful ways, *generates* itself -- though through shaping behaviors the designer can influence the results.

In this simple example, an agent starts at `(0,0,0)` and then, for each time step, is allowed to move a random amount in each of the three dimensions. As time passes, a line connects all of the different positions of the walker, showing the path that it traversed.

![walker](walker.gif)

This script can be placed inside of a `Python` node in Grasshopper, with inputs for `seed` and `time` hinted to `integer`.

```python
"""Provides a scripting component.
    Inputs:
        x: The x script variable
        y: The y script variable
    Output:
        a: The a output variable"""

__author__ = "your name"

#import some dependencies
import rhinoscriptsyntax as rs
import random as r

#set seed value from a slider for new random numbers
r.seed(seed)

#generate a class called walked
class Walker : 
  #what does the walker look like when it is born?
	def __init__(self) :
		self.x = 0
		self.y = 0
		self.z = 0

  #how does the walker appear at any moment in time? 
	def point(self) : 
		shape = rs.AddPoint(self.x,self.y,self.z)
		return shape

  #what does the walker do at each time step?
	def step(self) : 		
		#generate random numbers 
    	stepX = r.uniform(-1,1)
		stepY = r.uniform(-1,1)
		stepZ = r.uniform(-1,1)

    #change the position of the walker
		self.x += stepX		
		self.y += stepY		
		self.z += stepZ		


#The actual code -- let's simulate time passing

#Make a walker as defined above
w = Walker()

#Make an empty list of points to hold our walker's position over time
pList = []

#move through time
for t in range(time):
	#take a step
	w.step()
  #add a point for each moment in time
	pList.append(w.point())

#output the list of points
a = pList
```



	
	
