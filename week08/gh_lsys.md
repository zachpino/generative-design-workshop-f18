### Lindenmayer System in Grasshopper

[Download the definition](lsys.gh)

```python
import rhinoscriptsyntax as rs
import random as rv
import math

#class
class Walker : 
	def __init__(self) :	
		self.x = 0
		self.y = 0
		self.z = 0
		self.heading = 0

	def display(self) :
		shape = rs.AddPoint(self.x,self.y,self.z)
		return shape

	def step(self, op) :
			if op == "F" : 
				xCalc = math.cos(self.heading)* step
				yCalc = math.sin(self.heading)* step
				self.x += xCalc 
				self.y += yCalc

			elif op == "+" :
				self.heading = (self.heading + angle)%(math.pi * 2)

			elif op == "-" :
				if self.heading < angle :
					self.heading = ((math.pi * 2) + self.heading) - angle
				else : 
					self.heading = self.heading - angle


# parse axioms
original = a

for i in range(time) : 
	original = original.replace("A", a)
	original = original.replace("B", b)
	original = original.replace("C", c)

instruction = original.replace(" ", "")
instruction = instruction.replace("A", alphaReplace)
instruction = instruction.replace("B", alphaReplace)
instruction = instruction.replace("C", alphaReplace)


# instance
w = Walker()

# list of points
pList = []
firstPoint = rs.AddPoint(0,0,0)
pList.append(firstPoint) 

#walk through generations
move = step
for t in range(len(instruction)) :
	w.step(instruction[t])
	pList.append(w.display())

points = pList

axiom = instruction
```
