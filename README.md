Assignment 1 - Hello World: GitHub and d3
===
# GitHub Pages
https://saviocloud.github.io/a1-saviocloud-savio-ketnouvong/

# Assignment Description
For this assignment, I coded a representation of a soccer field and ball moving across it using D3.js. I used the four required graphics (rectangles, circles, lines, and polygons) to build everything. I also added an animation sequence to the soccer ball, moving it from one end of the field to the other, with a triangle trail following it to show the change in velocity of the ball.

# Screenshots
![alt text](<Screenshot 2026-10-26 at 7.45.04 PM.png>) ![alt text](<Screenshot 2026-10-26 at 7.45.37 PM.png>)

# Technical and Design Choices
I implemented some complex (to me) code that I think can push my assignment grade into the "A" territory:

## Technical
**Background Field Generation:**
I didn't hard code the alternating green lines with rectangles, but rahter I wrote a look to generate 12 alternating verticle rectangles. I also calculated their x attributed dynamically to create the classic soccer field pitch lines.

**Animation and Easing:**
I used d3.transition() with ds.easeCubicOut to animate the ball. The easing function was the closest I found to the real world, as it is fast in the beginning, and slows down as time goes on.

**Groupings & Transformations:**
I grouped the ball and the trail (triangle) in an SVG <g> element. Then I used transitions with a duration(0) and a rotate(180) to transform the ball the moment the ball reached it's destination. this made the trail flip seemlessly to follow the balls path when it returned to the other side.

**Trail Shrinkage and Extension:**
I made a second animation that targeted the balls trail (triangle). The trail will dynamically shrink in length (from -40 to 0) in sync with the cubic deceleration of the ball. This helps further visualize the balls change in speed.

## Designs
**Cohesion:**
I tried to go beyond making isolated shaped by layering the field lines on top of the pitch pattern

**Layering:**
I managed the layers by using the DOM appending order. The grass pattern rendered first, which was followed by the pitch lines in white, with the fill set to none so the pitch pattern shows through them. I also used some rgba() colors with very low opacity so you can see the pattern of the pitch through some of the elements.

**Geometry:**
I made the pitch rely on exact spacing across the canvas (600x400). This made sure that there was symmatry between the two halves, with the center line being at exactly x = 300. This also allowed me to mirror the two boxes easily.

# Sources
**D3.js Documentation:**
I used the official D3 API documentation (https://d3js.org/api) for help with syntax in regards to d3.select(), appending elements, and using transitions and easing functions.

**AI Usage:**
I used Grammarly to help with spelling errors and refined wording in this README. I also used Google Gemini Flash-Lite to help resolve issues with orienting the trail triangle correctly, as the pointed side of the triangle was going into the ball rather than the flat side (comments on AI usage also shown in file with comments of input and used output).