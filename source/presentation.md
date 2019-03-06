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
class: full-image
![](assets\my10printwidecoloured.png)
---
class: art-page
![](assets\drawingwithparticlesbyjeromesaint-clair2009.png)
## Drawing with particles by 01010101 (2009)
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

.w-80.bottom-center[![](assets\code.png)]
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
* Stop it from looping
  * `noLoop();`

.bottom-right.bottom-3.w-50[![](assets\OpenProcessing.png)]
---
# Canvas
* We need canvas to draw
* We need to know how big the canvas is (width & height)
* `createCanvas(width,height)`
* Width and height are pixels
.bottom-right.w-30[![](assets\noun_canvas_1095664.svg)]
---
# Circles
* Two pieces of information
* Location
  * x and y coordinates
* Diameter
  * In pixels 
.bottom-right.bottom-10.w-40[![](assets\circleDiameter.png)]
---
# Coordinate system (computer)
.contain.center[![](assets\400coordinates.png)]
---
# Draw some circles
* Canvas is measured in pixels, which are TINY!
* Try drawing some circles: ellipse(x, y, diameter)
* Examples:

```javascript
ellipse(0,0,200);
ellipse(150,120,50);
ellipse(180,200,20);
```
---
# Challenge 1 - Concentric circles
.contain.center[![](assets\concentricCircles.png)]
---
# Saving and forking
* You need to save your work, it's not saved automatically!
* Forking work just means making a copy, you can do this with your own work or other people's
* If you are working on an idea and want to explore a different direction without losing the original, fork your work

.bottom-right.bottom-5.w-40[![](assets\forking.jpg)]
---
# Other shapes
* Rectangle:
```javascript
rect(x,y,width,height)
```
 x and y refer to top left corner
* Line:
```javascript
line(startX, startY, endX, endY)
```
* Check p5 reference for more shapes
* http://p5js.org/reference
---
# Some grammar for code
* Read from top to bottom
* Semi colon at end of line
* Case sensitive, the following **wouldn't** work

```javascript
Ellipse(100,100,50);
```

* Commands to the computer look like this

```javascript
ellipse(argument1, argument2);
```

* The brackets make the command run
* The arguments are information we give the command, e.g. how big to make circle or where to put circle
---
# Colours
* There are many named colours, for example:
  * `‘darkolivegreen’`
  * `‘dimgrey’`
  * `‘dodgerblue’`
* You can change the fill colour of shapes:

```javascript
fill('blue');
```

* You can change the stroke colour

```javascript
stroke("green");
```

* More colours: <a target="_blank" href="http://colours.neilorangepeel.com">colours.neilorangepeel.com</a>
.top-right[![](assets\bluefillgreenstroke.png)]
---
# More Colour
* Grayscale – `fill(100)`
  * If one number provided for color command it will use grayscale
  * 0 is black, 255 is white
* RGB – `color(red,green,blue)`
* Hex codes – `color(‘#6495ED’)`
* Colour picker: <a target="_blank"  href="https://www.webfx.com/web-design/color-picker/">www.webfx.com/web-design/color-picker/</a>
---
# Randomness
  * Computers can come up with random numbers
  * This picks a number between 0 and 100 (includes decimals):

```javascript
random(100);
```
  * This picks a number between 100 and 200  

```javascript
random(100,200);
```
  * This picks a random number between 0 and 1

```javascript
random();
```
---
# Random Colour
* Lists, in a computer program, are surrounded by square brackets

```javascript
[1,2,3,4]
```
* We can have a list of named colours:

```javascript
[‘red’, ‘green’, ‘blue’, ‘yellow’]
```
* We can use the random instruction to tell the computer to pick a random colour

```javascript
random([‘darkcyan’, ‘olive’, ‘yellowgreen’])
```
* Try giving the circles random colours
---
.row[# Challenge 2 - Random circles]

.row[
  .col-6.h-45[ .responsive[ ![](assets\randomCircles.png) ]] 
  .col-6[
* Try finding your own colours to use
* Try having some things random and others not – for example you could pick a specific size for your circles
* See what happens if you change the range for the randomness
  ]
]
.row[

```javascript
background(‘#94A537’);
fill( random([‘green’, ‘purple’]) );
circle(random(800),random(500),random(100));
```

]
---
# Variables
* A way of saving a value to use later
* Like a box where you can store something
* Built in variables: 
  * `width` - the width of your canvas
  * `height` - the height of your canvas
  * `windowWidth` - the width of the browser window the canvas is in
  * `windowHeight` - the height of the browser window

```javascript
var randomWidth = random(100,500);
ellipse(100,100,randomWidth);
ellipse(50,50,randomWidth);
```
---
# Worked Example
.responsive.center[ ![](assets\stackedCircles.png) ]
---
# Functions
Grouping commands together

```javascript
function randomCircle() {
  fill(random([‘red’,’black’]));
  ellipse(random(width),random(height),100);
}
```

Can give them ‘arguments’:

```javascript
function randomCircle(diameter) {
  fill(random([‘red’,’black’]));
  ellipse(random(width),random(height),diameter);
}
```
???
Apply function to stacked circles
---
.row[ # Challenge 3 - Flower ]
.row[
  .col-6[ .responsive[![](assets\circleFlower.png)] ]
  .col-6[
* Try making this shape
* Try making its location random
* Try making its colour random
* Try putting it into a function
  ]
]
---
# Loops
* Counts numbers
* We choose starting number
* We choose number it ends at
* We choose whether we count up, down, and how much we add or subtract each time
* Each time the loop counts it performs an action, the action can be based on the number the loop is at in the count

```javascript
for (var size=200; size>0; size=size-50) {
  ellipse(200,200,size);
}
```
???
Show lots of examples
---
# If this then that
* To choose whether or not to do something based on some condition we use an if-else statement 
* This statement checks a condition and performs an action if that condition is met, otherwise (else) it does another action, it will look something like this:

```javascript
if (random()>0.5) {
  doAnAction
}
else {
  doSomeOtherAction
}
```
The above code will do each action about half the time
---
# Drawing in a grid: Loop inside a loop
* One loops creates the "columns" or the x-values
* One loop creates the "rows" or the y-values
* The step is the height and width of each square in the grid

```javascript
var step = 20;
for (var x=0;X<width;x+=step) {
  for (var y=0;y<height;y+=step) {
    rect(x,y,step,step);
  }
}
```
---
.row[ # Final challenge ]
.row[
  .col-3[ .responsive[ ![](assets\my10print2.png) ] ]
  .col-1[ ![]() ]
  .col-8[
* Pattern created by randomly drawing either a left diagonal or right diagonal in a grid
* Play with the code and create variations

```Javascript
for (var x=0; x < width; x = x + 10) {
  for (var y=0; y < height;y = y + 10) {
    // Your line commands go here
  }
}
strokeWeight(3); 
stroke("red");
line(startingX,startingY,endingX,endingY);
```
  ]
]