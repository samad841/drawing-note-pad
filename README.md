from turtle import *

# Set up the screen
screen = Screen()
screen.title("Dragon Follows Pointer")
screen.bgcolor("black")

# Create the dragon (turtle)
dragon = Turtle()
dragon.shape("turtle")
dragon.color("green")
dragon.speed(0)

# Function to move the dragon to the mouse pointer
def follow_pointer(x, y):
    dragon.setheading(dragon.towards(x, y))
    dragon.goto(x, y)

# Bind mouse movement to the follow_pointer function
screen.onscreenclick(follow_pointer)

# Keep the window open
screen.mainloop()
    

