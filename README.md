# walking-cat-js
Exercises: Cat Walk (GDI)

This was an excercise executed in colaboration with Mila through the Pair Up! meetup workshop event organized by Girl Develop It Chicago on May 30th, 2015.

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
credit to: http://www.pairuptocode.com/exercises/catwalk.html

The goal of this exercise to make an awesome interactive animated cat.

You may find these slides helpful.

Start with this webpage, which has an img of a cat walking, and JavaScript functions that animate the cat across the screen. (For all of these, you shouldn't need to touch the original code - just add code below.)
        <!DOCTYPE html>
        <html>
         <head>
          <meta charset="utf-8" />
          <title>Cat Walk</title>
         </head>
         <body>
          
          <button id="start-button">Start</button>
          <button id="speed-button">Go Faster!</button>
          <button id="stop-button">Stop</button>
          <div id="info"></div>
          
          <img style="position:absolute; left: 0px; top: 80px;" src="http://www.anniemation.com/clip_art/images/cat-walk.gif">

          <script>
            var movePixels = 10;
            var delayMs = 50;
            var catTimer = null;
            function catWalk() {
              var img = document.getElementsByTagName('img')[0];
              var currentLeft = parseInt(img.style.left);
              img.style.left = (currentLeft + movePixels) + 'px';
              if (currentLeft > (window.innerWidth-img.width)) {
                img.style.left = '0px';
              }
            }
            function startCatWalk() {
              catTimer = window.setInterval(catWalk, delayMs);
            }
          </script>

         </body>
        </html>
      
1. Add an event listener to the start button, so that the cat starts moving across the screen when its clicked.
2. Add an event listener to the stop button, so that the cat stops moving when clicked.
3. Add an event listener to the speed button, so that the cat moves faster when it's clicked.

Bonus: Disable the start/stop/faster buttons at the appropriate times (e.g. the user shouldn't be able to click "stop" if the cat isn't currently moving.)

Fork my solution. Thanks, deva
