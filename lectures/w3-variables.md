# Variables

## System Variables

### Mouse position
`mouseX` and `mouseY` store the current mouse position in numbers.

```java
void draw() {
  ellipse(mouseX, mouseY, 100, 100);
}
```

```java
void draw() {
  fill(mouseX, 0, 255);
  ellipse(mouseX, mouseY, 200, 200);
}
```

### Previous mouse position
`pmouseX` and `pmouseY` store the mouse position of the previous frame.

```java
void draw() {
 line(pmouseX, pmouseY, mouseX, mouseY);
}
```

### Window width and height
`width` and `height` variables store the width and height of the current window.

```js
void setup() {
  size(500, 500);
}

void draw() {
  background(200);
  ellipse(width/2, height/2, 200, 200);
  line(0, 0, width, height);
  line(width, 0, 0, height);
}
```

### Display size
`displayWidth` and `displayHeight` store the size of the browser window. As you resize the window, the values will change.

```js
void setup() {
  size(displayWidth, displayHeight);
}

void draw() {
  background(200);
  ellipse(width/2, height/2, 200, 200);
}
```

### Fullscreen
If you want to run your sketch in fullscreen, instead of `size()`, use `fullScreen()` function.

```java
void setup() {
  fullScreen();
}
```

### Counting frames
`frameCount` stores the number of frames that have passed since the sketch started running. As the sketch keeps running, the value will keep increasing.

```js
void draw() {
  println(frameCount);
}
```

## Create your own variable
A variable stores a value in the computer memory so that it can be used later in a program. Once you create a variable, you can use it as many times as you want. The value can also be changed while the program is running.

```java
int life; // declare
life = 3; // initialize
```

```java
int life = 3; // declare and initialize a variable at the same time
```

When creating a variable, use a descriptive name.
```js
int a = 21; // what is a?
int age = 21; // this is better.
```

Variables are not limited to a number. You can store more complex data in a variable. Below is an example of color.
```js
color col = color(0, 200, 100);
fill(col);
ellipse(width/2, height/2, 100, 100);
```

### Different types of variables

There are a few different types of variables, and you need to use the right type depending on the data you work with.

```java
int a = 3; // integer: whole numbers
float b = -3.2 // float: decimal numbers
boolean c = true // boolean: either true or false
char d = 'A'; // character: a single character. use single quotes.
color e = color(255, 0, 0); // color
String f = "Hello!"; // string contains a string of text. use double quotes.
```


### Variable scope
When a variable is declared outside of any functions such as `setup()` or `draw()`, it can be used from anywhere in the program. This is called a *global variable*.
```js
int diam = 200; // global variable

void setup() {
  size(400, 400);
}

void draw() {
  ellipse(width/2, height/2, diam, diam);
}
```

When a variable is declared within a function, it can only be used within the function it was created from. This is called a *local variable*.

```js
void setup() {
  size(400, 400);
  int diam = 200; // local variable
}

void draw() {
  ellipse(width/2, height/2, diam, diam); // error - draw() cannot see diam variable.
}
```
  
## Print to console
To print a value, use `println()`. This is useful to check the current value of any variables.

```js
String a = "How are you?";
println(a);

int b = 3;
println(b);
```

What you print using `println()` does not show up on your canvas. You have to open up the JavasScript console from the browser.


## Assignment operator
One equal sign `=` is an assignment operator. It does not mean that the values on the left and right side of the equation are the same. To evaluate, you need to use two equals `==`.

```js
int a = 10;
int b = a;
println(b);

int c = 10;
int d = 15;
d = c;
println(d);

int e = 10;
e = e + 5;
println(e);

int f = 12;
f = f * 2;
println(f);
```
  
-----
*Exercise: Draw multiple shapes on screen. Set their properties such as x, y coordinates, size, color, etc. Now, create a variable (or use one of the existing system variables) and apply the same variable to multiple shapes. Change the value and see how they relate.*
