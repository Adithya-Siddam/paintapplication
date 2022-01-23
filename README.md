# Web Page for Paint Application

## AIM:

To design a static website for Paint Application using HTML5 canvas.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML,CSS and canvas.

### Step 3:

Write javascript to capture move events.

### Step 4:

Perform the drawing operation based on the user input.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
~~~
<!DOCTYPE html>
<html>
<body id="back">
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Paint Application</title>
    <div class="box">
    <h1>Paint Application</h1>
    </div>
    <div id="boss">
<canvas id="myCanvas" width="800" height="600" onclick="showCoords(event)"></canvas></div>
<center>
<button onclick="shape=1" id="cast">Circle</button>
<button onclick="shape=2" id="cast">Square</button>
<button onclick="shape=3" id="cast">Triangle</button>
<center>
<button onclick="change_color(this)" id="colur" style="background: violet;"></button>
<button onclick="change_color(this)" id="colur" style="background: greenyellow;"></button>
<button onclick="change_color(this)" id="colur" style="background: blue;"></button>
<button onclick="change_color(this)" id="colur" style="background: yellow;"></button>
<button onclick="change_color(this)" id="colur" style="background: orange;"></button>
<button onclick="change_color(this)" id="colur" style="background: red;"></button>
<button onclick="change_color(this)" id="colur" style="background: black;"></button>

</center>

<script>
const canvas = document.getElementById("myCanvas");
const ctx = canvas.getContext("2d");
ctx.fillStyle = "#FF0000";
canvas.height =600;
canvas.width=800;
ctx.transform(1, 0, 0, -1, 0, canvas.height);
let xMax = canvas.height;
let yMax = canvas.width;
let csize= 20;
let sqsize= 50;
let tsize=30;
let board="black";
function change_color(element){
    board=element.style.background;
}

    function showCoords(event)

    {
    var x = event.clientX-545;
    var y = yMax-event.clientY;
    var coords = "X co-ordinate: " + x + ", Y co-ordinate: " + y;
    document.getElementById("dam").innerHTML = coords;

        if (shape==1){
            ctx.beginPath();
            ctx.arc(x, y, csize, 0, 2 * Math.PI);
            ctx.strokeStyle=board;
            ctx.stroke();
        }

        if (shape==2){
            ctx.beginPath();
            ctx.rect(x-(sqsize/2),y-(sqsize/2), sqsize,sqsize);
            ctx.strokeStyle=board;
            ctx.stroke();
        }
        if (shape==3){
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.lineTo(x-(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x+(tsize/2),y-(tsize*0.86602));
            ctx.lineTo(x,y)
            ctx.strokeStyle=board
            ctx.stroke();
        }

    }

</script>
<center><p id="dam" style="color: black;"></p></center>
<p style="color: black; font-family: sans-serif;" >Developed by Adithya Chowdary.S</p>
<style>

.box{
    color: black;
    font-size: 25px;
    text-align: center;
}
          
#boss{
    text-align: center;
   
}
#myCanvas{
    background-color: white; 
    border: 1px solid #ffffff;
}
#cast{
    border: 1px solid rgb(10, 10, 10);
    border-radius: 15px;
    color: black;
    padding: 15px 32px;
    text-align: center;
    display: inline-block;
    font-size: 20 px;
    margin: 4px 2px;
}

#back{
    background-color: cyan;
}
#colur{
    border: 2px solid #ffffff;
    border-radius: 25px;
    padding: 25px 25px;
    text-align: center;
    display: inline-block;
    font-size: 15px;
    margin: 4px 2px;
}
</style>
</body>
</html>
~~~

## OUTPUT:
![OUTPUT](/IMAGES/img1.png)
## Result:
Thus a website is designed and validated for paint application using HTML5 canvas.