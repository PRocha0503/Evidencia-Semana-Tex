# TC1001S - Herramientas Computacionales

This is a code to learn how to use github, we used it as practice

Author: Pablo Rocha A01028638, Alfredo Jeong Hyun Park A01658259, Salvador Ulibarri A01066922

Original games code from: http://www.grantjenks.com/docs/freegames/index.html

We selected this 3 games

- Snake
- Cannon
- Memory

## Changes made by each member

### Pablo Rocha

#### Snake

- changed the speed of the snake

```
ontimer(move, 50)
```

- made the snake able to go to the edges

```
return -210 < head.x < 210 and -210 < head.y < 210
```

#### Cannon

- made the ball never go down

```
speed.y -= 0.1
```

- changed the color of the targets

```
dot(20, 'orange')
```

#### Memory

- made the font bold

```
write(tiles[mark], font=('Arial', 30, 'bold'))
```

- change the size of the window

```
setup(840, 840, 370, 0)
```

### Alfredo Jeong Hyun Park

#### Snake

- Made speed increase everytime food is eaten

```
speed = 100

if head == food:
   # Increase speed everytime food is eaten
   global speed
   speed -= 6
   print('Snake:', len(snake))
   food.x = randrange(-15, 15) * 10
   food.y = randrange(-15, 15) * 10
else:
   snake.pop(0)
```

#### Memory

- Added counting total taps

```
taps = 0

def square(x,y):
   global taps
   taps += 1
   print("Taps: " + str(taps))
```
### Salvador Ulibarri Sierra A01066922

#### Snake
-changed the color of the snake from black to blue
 for body in snake:
        square(body.x, body.y, 9, 'blue')#a modification was done here

#### Memory

-changed the coloures of the tiles and the lines of the tiles
def square(x, y):
    "Draw white square with black outline at (x, y)."
    up()
    goto(x, y)
    down()
    color('white', 'blue') # a change was made here
    begin_fill()
    for count in range(4):
        forward(50)
        left(90)
    end_fill()


### Installing the Freegames module

1. Make sure Python 3 is installed in your computer, and that you can call
   it from a terminal
2. Download the pip installer from: https://bootstrap.pypa.io/get-pip.py
3. Run the installer:

```
python3 get-pip.py
```

4. Install the module:

```
pip install freegames
```
