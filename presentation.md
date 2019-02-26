title: Programming for Artists
class: animation-fade
layout: true

<!-- This slide will serve as the base layout for all your slides -->
.bottom-bar[
  {{title}}
]

---
class: impact
# Programming for Artists
---

# Drawing with particles by 01010101 (2009)
---
class: art-page
![](assets\DavidDessens-CartesianCreatures.jpg)
## Cartesian Creatures by David Dessen (2007)
---
class: art-page
![](assets\DésOrdres_Vera_Molnár_1974.jpg)
## (Dés)Ordres by Vera Molnár (1974)
---
class: art-page
![](assets\Bubble+Chamber+-+Jared+Tarbell,+2003.jpg)
## Bubble Chamber by Jared Tarbell (2003)
---
class: art-page
![](assets\Nude_Portrait_Robbie_Barrat_2018.png)
## Nude Portrait by Robbie Barrat (2018)
---
class: art-page
<video controls loop preload='auto'>
  <source src="assets\Sun-robert-hodgin.mp4"
            type="video/mp4">
</video>
## Sol by Robert Hodgin
---
class: art-page
<video controls muted loop preload='auto'>
  <source src="assets\Mechanical_Parts_Matthias_Dörfelt_2013.mp4"
            type="video/mp4">
</video>
## Mechanical Parts by Matthias Dörfelt (2013)
---
# What is code?
* A series of instructions for the computer
* A precise way of explaining how to do something
* Written in a programming language
* Facilitate communication between human and machine, rather than human and human
---
# Code as an artistic tool
* Like a paintbrush which can be used to paint a wall 
* Add interactivity
* Artists, designers, architects use software to realise artistic vision – learning code gives more flexibility
* Generative art - “taking strict, cold, logical processes and subverting them into creating illogical, unpredictable, and expressive results. […] Generative art is about creating the organic using the mechanical.”
---
# Organic vs Mechanical
> From the standpoint of Taoist philosophy natural forms are not made but grown, and there is a radical difference between the organic and the mechanical.
> Things which are made, such as houses, furniture, and machines, are an assemblage of parts put together, or shaped, like sculpture, from the outside inwards.
> But things which grow shape themselves from within outwards—they are not assemblages of originally distinct parts; they partition themselves, elaborating their own structure from the whole to the parts, from the simple to the complex. 

.right.alt[ \- Alan Watts, 1958]
---
# Getting Started
* Search for “openprocessing” and open link
* Sign up
* Create first sketch
* Change the background to pink
* `background(‘pink’)`
* `noLoop();`
---
# Canvas
* We need canvas to draw
* We need to know how big the canvas is (width & height)
* `createCanvas(width,height)`
* Width and height are pixels
.bottom-right[![](assets\noun_canvas_1095664.svg)]
---
# Circles
* Two pieces of information
* Location
* Diameter
.bottom-right[![](assets\circleDiameter.png)]
---
# Coordinate system (computer)
.contain.center[![](assets\400coordinates.png)]
---
# Draw some circles
* Canvas is measured in pixels, which are TINY!
* Ellipse to circle like rectangle to square
* Try drawing some circles: ellipse(x, y, diameter)
* Examples:
```javascript
ellipse(0,0,200);
ellipse(150,120,50);
ellipse(180,200,20);
```
---
# Try making this
.contain.center[![](assets\concentricCircles.png)]
---
# Saving and forking
* Go through saving work on openprocessing
* Talk about forking work 
* Let them fork my work to try it out
---
# Other shapes
* Rectangle:
```javascript
rect(x,y,width,height)
```
 x and y refer to top left corner
* Line:
* line(startX, startY, endX, endY)
* Check p5 reference for more shapes
* http://p5js.org/reference
---
# Some grammar for code
* Read from top to bottom
* Semi colon at end of line
* Case sensitive
* Commands to the computer look like this
* ellipse(argument1, arguement2);
* The brackets make the command run
* The arguments are information we give the command, e.g. how big to make circle or where to put circle
---
# Colours
* Named colours
* ‘darkolivegreen’
* ‘dimgrey’
* ‘dodgerblue’
* Try changing the colour of the circles by using typing the following before the circles: 
* fill(‘purple’);
* More colours: colours.neilorangepeel.com
---
# More Colour
* Grayscale – color(100)
* If one number provided to color command it will use grayscale
* 0 is black, 255 is white
* RGB – color(red,green,blue)
* Hex codes – color(‘#6495ED’)
------
# Randomness
* Computers can come up with random numbers
* To pick a random number you want to know the range
* random(100);
* This picks a number between 0 and 100
* random(100,200);
* This picks a number between 100 and 200
* Try giving your circles a random size or location
---
# Random Colour
* Lists, in a computer program, are surrounded by square brackets
* [1,2,3,4]
* We can have a list of named colours:
* [‘red’, ‘green’, ‘blue’, ‘yellow’]
* We can use the random instruction to tell the computer to pick a random colour
* random([‘darkcyan’, ‘olive’, ‘yellowgreen’])
* Try giving the circles random colours
---
# Putting it together
* background(‘#94A537’);
* fill( random([‘green’, ‘purple’]) );
* circle(random(800),random(500),random(100));
* Try finding your own colours to use
* Try having some things random and others not – for example you could pick a specific size for your circles
* See what happens if you change the range for the randomness
---
# Variables
* A way of saving a value to use later
* Can use them to easily change the size of several shapes 
* Can use it to easily move connected shapes
* Could use it to give several shapes the same random number or random colour
* Built in variables: width, height, windowWidth, windowHeight
---
# Worked Example
---
# Functions
Grouping commands together
function randomCircle() {
fill(random([‘red’,’black’]));
circle(random(width),random(height),100);
}
Can give them ‘arguments’:
function randomCircle(diameter) {
fill(random([‘red’,’black’]));
circle(random(width),random(height),diameter);
}
---
# Challenge
Try making this shape
Try making its location random
Try making its colour random
---
# Loops
Counts numbers
We choose starting number
We choose number it ends at
We choose whether we count up, down, and how much we add or subtract each time
Each time the loop counts it performs an action, the action can be based on the number the loop is at in the count
---
# If this then that
---
# Loop inside a loop
---

class: impact

# {{title}}
## With a good subtitle :-)

---

# The basics

## Getting started

Use [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) to write your slides. Don't be afraid, it's really easy!

--

## Making points

Look how you can make *some* points:
--

- Create slides with your **favorite text editor**
--

- Focus on your **content**, not the tool
--

- You can finally be **productive**!

---

# There's more

## Syntax highlighting

You can also add `code` to your slides:
```html
<div class="impact">Some HTML code</div>
```

## CSS classes

You can use .alt[shortcut] syntax to apply .big[some style!]

...or just <span class="alt">HTML</span> if you prefer.

---

# And more...

## 12-column grid layout

Use to the included **grid layout** classes to split content easily:
.col-6[
  ### Left column

  - I'm on the left
  - It's neat!
]
.col-6[
  ### Right column

  - I'm on the right
  - I love it!
]

## Learn the tricks

See the [wiki](https://github.com/gnab/remark/wiki) to learn more of what you can do with .alt[Remark.js]
