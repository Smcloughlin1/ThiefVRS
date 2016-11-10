# ThiefVRS

def chase_right_down(): 
    global x, y

    x, y = randrange(0, 800), randrange(0, 500)  # Randomize x and y (note that you should substitute your max and min canvas coordinate values if you want the ball to stay in view.

    can.coords(ball, x-r, y-r, x+r, y+r) 
 
 def chase_left_up(): 
    global x, y

    x, y = randrange(0, 800), randrange(0, 500)  # Randomize x and y (note that you should substitute your max and min canvas coordinate values if you want the ball to stay in view.

    can.coords(ball, x-r, y-r, x+r, y+r) 
 
def move_ball():
    global flag, x, y, moving
 
    if moving == True:
        chase_right_down()
    if moving == False:
        chase_left_up()
       
    if x <= 20 or y <= 20:
        moving = True
    if x >= 480 or y >= 480:
        moving = False
 
