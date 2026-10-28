HoopLab — Interactive Basketball Play Designer

CS4804 — Data Visualization | Assignment 1

Live Website: https://davischarlesb27-jpg.github.io/a1-ghd3/

Project Description

HoopLab is a basketball interactive play designer using javaScript, HTML, CSS, and D3.js. This visualization shows a half court basketball set where there are 5 offensive players, with the 1 (point guard) having the ball above the top of the key, the 2 and 3 at the 3pt line elbow line extended, and the 5 in the key. 

The user clicks Run Pick and Roll to start the animation and see the play unfold. Player 5 moves from the paint(inside of the colored box) to the top of the key, where he sets a screen for player 1 who then dribbles around the screen. As player 5 comes up, 3 goes to the corner, and the 1 fills 3s spot. Player 5 then rolls to the basket and receives the pass to score. 

<img width="643" height="556" alt="hooplab-start" src="https://github.com/user-attachments/assets/df1596d0-2dc3-427b-86a5-a7789a96c74c" />
<img width="640" height="555" alt="hooplab-play (1)" src="https://github.com/user-attachments/assets/7512684f-d039-4f33-8386-74a7ab5e641b" />   

How to Use

Open the live website.
Click "Run Pick & Roll" to begin the animation.
Watch the players move and the passing route appears.
Click "Reset Play" to return to the original formation.


Technical and design Achievement

My technical achievement for this animation is mainly using D3.js to animate all of the different players moving on different paths. I used D3 transitions to animate all of the players, then JavaScript's async/await and Promise.all(), which controls the timing of the play (i.e. when the players move). Using these functions, I was able to have multiple players moving at the same time, keeping the overall play sequence correct and making it understandable and the time applicable for actual basketball plays. One challenge I ran into while making this simulation was making the point guard move around the screen on a curve. Using SVG Bézier curves and D3's attrTween(), I animated the players to have more natural curved paths, as in basketball no one really moves in straight lines unless the defense is doing something really wrong. My next challenge was having the basketball follow the point guard and then it to be passed to the 5, I used getPointAtLength() to calculate those paths to ensure the visualization looked accurate. 
In terms of design achievement, only so much can be done for a basketball simulation, still I made the court accurate to what it looks like in real life, and kept the movements simple and easy to follow as most people who would be using this visualization may be still learning the game still and how the movements work. I used a wood colored background, white court markings for the key and 3 pt line, the paint is colored a darker brown to distinguish it, and the hoop is orange and white. Players are shown as blue circles, and their paths are different colors to show who is favored on the play. The players' numbers are coordinated to their position. I chose the starting position based on my favorite set in basketball to run and I thought when I was a kid and my mom was my coach, she would have loved something like this to show us what to do, she used to have a magnetic board in practice and would move the players along just the simulation.  

Sources and Acknowledgments

CS4804 Assignment 1 Starter Repository — Initial HTML and D3 project structure.
D3.js — JavaScript visualization library.
OpenAI ChatGPT — Assisted with generating and explaining HTML, CSS, JavaScript, D3 drawing code, and animation logic. I directed the basketball concept, formation, and changes to player movement.


