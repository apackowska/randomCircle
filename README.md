# randomCircle

import random
from graphics import *

def main():
    win = GraphWin("Random Circle", 500, 500)
    # give random from 0-1
    win.setCoords(0.0,0.0,1,1)
    circle = Circle(Point(0.5,0.5), 0.1)
    circle.draw(win)
    while True:
        pt = win.checkMouse()
        key = win.checkKey()
        if pt:
            circle.undraw()
            x = random.random()
            y = random.random()
            circle = Circle(Point(x,y), 0.1).draw(win)
        if key:
            win.close()


main()


