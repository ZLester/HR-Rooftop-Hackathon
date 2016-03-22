Intro to objects.



An easy way to introduce the concept of objects would be to compare it to something physical. In this case, it could be different types of balls.



Ask the class what attributes the basketball has. Color, texture, shape, is it inflated, ect.

var basketball = {};

console.log(basketball);



"As of right now, our basketball has no attributes. Let’s give it some:"

basketball.color = “Orange.”;

basketball.texture = “Rough”;

basketball.isInflated = true;

basketball.shape = “Round”;

console.log(basketball);



"Now it has values! In javascript, there’s more another way to give an ‘Object’ values. Say we wanted know the brand of our basketball object. 

Instead of saying basketball.brand = “Wilson” we could also say basketball[“brand”] = “Wilson”. Either way will work!"

basketball[“brand”] = “Wilson”.

console.log(basketball);



Ask the class to now make their own “football” object. It should have color, texture, shape, & brand properties. Instruct them to use “console.log” to make sure it has all of the properties it needs!



What if we didn’t care about the shape, color, or texture of our basketball? What if all we wanted to know was: “is it inflated or not?”. Explain to the class that we can lookup specific values without having to see the whole object. Turns out, we can do this in two different ways:

console.log( basketball.isInflated )

OR

console.log( basketball[“isInflated”] );



Either will work!



Ask the class to log the “isInflated” value of their basketball object.

Ask the class to log the “color” value of their football object.



(The following exercise assumes students understand what functions are and how to use them!)

Explain to the class that not only can objects store values, but they can’t store behaviors as well. Once we’ve created these behaviors (also known as ‘methods’) we can call them whenever we want!



basketball.bounce = function() {

  console.log(“Bounce!”);

 };



remember, to make a method run (‘method’ being the basketball.bounce behavior we just made) we have to follow it with ‘()’



basketball.bounce(); -> “Bounce!”

basketball.bounce(); -> “Bounce!”



No one likes basketball. Let’s pop our ball.



basketball.popBall = function() {

  console.log(“POP!”);

  basketball.isInflated = false;

  basketball.shape = “Flat”;

 };



basketball.popBall();



But wait… you can’t bounce a flat ball! That doesn’t make sense! A ball should only bounce if it’s inflated. Fortunately, we can change the basketball's ‘bounce’ to handle this.



basketball.bounce = function() {

  if( basketball.isInflated === true ) {

  console.log(“Bounce!”);

 } else {

  console.log(“Your flat basketball slaps onto the ground and just sits there.“);

 }

 }



basketball.bounce();