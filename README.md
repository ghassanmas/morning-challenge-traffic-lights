**Author**: [@finnhodgkin](https://github.com/finnhodgkin)

**Maintainer**: [@finnhodgkin](https://github.com/finnhodgkin)  

# Traffic light callback challenge:vertical_traffic_light:

![traffic light gif](https://user-images.githubusercontent.com/22300773/27510355-77a53678-5906-11e7-8215-845f9c987e09.gif)

## Setup

1. Clone the repo

```
$ git clone https://github.com/foundersandcoders/morning-challenge-traffic-lights.git
```

2. Open the folder in your favourite text editor.

3. For instant feedback on all your changes run live server :sparkles:

```
$ npm i && npm run live
```

## Refreshment on passing function as a parameter


Function could be passed as a  parameter to other function, specially when the function is Async, consider the following the examples:


In the above example we are using the built-in JS function ```setTimeout``` to call the ```toggle``` function after 5 seconds.


```
function toggle(){
 document.getElementById("someElement").classList.toggle('hover-over');
}

setTimeout(toggle,1000*5);
```


Now consider this scenario where the ```toggle```  function takes a parameter ```id```

```
function toggle(id){
 document.getElementById(id).classList.toggle('hover-over');
}
```

```setTimeout(toggle(id),1000*5);```

Why the above the wont work? passing ```toggle(id)``` as parameter will return ```undefined``` since we are not passing a function, we are passing whatever the function **return**. and since the function doesn't return anything; it will return ```undefined``` by default.

To get around it we can wrap ```toggle(id)``` in an anonymous function such as:

```
setTimeout(function(){
toggle(id);
},1000*5);
```

## Your task

Your task is to replicate the traffic lights shown above. The only file you'll
need to edit is `script.js`. Hopefully the instructional comments will speak for
themselves.

If you get stuck check out th e [hints branch](https://github.com/foundersandcoders/morning-challenge-traffic-lights/tree/hints).

### Part 1 ```light()```:

Light up the first traffic light in the following order:

+ :green_apple: green
+ :green_apple: green
+ :sun_with_face: yellow
+ :red_circle: red
+ :red_circle: red
+ :red_circle: red
+ :red_circle: red
+ :red_circle::sun_with_face: red & yellow

### Part 2 ```light2()```:


+ :red_circle: red
+ :red_circle: red
+ :red_circle: red
+ :red_circle::sun_with_face: red & yellow
+ :green_apple: green
+ :green_apple: green
+ :sun_with_face: yellow
+ :red_circle: red

### Part 3:

Loop the light so it plays forever, consider the recursion concept where the function calls itself

### Part 4:

Loop the second light with the following rules:

+ Green should show only when the other light is red.
+ When transitioning from green to red, show yellow.
+ If the other light is green or yellow, show red.
+ When transitioning from red to green show yellow and red simultaneously.

:vertical_traffic_light: If successful you should see something like the
gif above. :tada:

### Finished?

Have you solve it using recursion?, where the function calls itself, could you solve it with ```setInterval```? check the [W3School](https://www.w3schools.com/jsref/met_win_setinterval.asp) documents about it.

### Solutions:

Check out the two solution branches (solution and solution-fun) for two complete examples
