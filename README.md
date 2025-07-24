from turtle import *

# Set up the screen
screen = Screen()
screen.title("pointer Follows Pointer")
screen.bgcolor("black")

# Create the pointer(turtle)
pointer = Turtle()
pointer.shape("turtle")
pointer.color("green")
pointer.speed(0)

# Function to move the dragon to the mouse pointer
def follow_pointer(x, y):
    pointer.setheading(pointer.towards(x, y))
    pointer.goto(x, y)

# Bind mouse movement to the follow_pointer function
screen.onscreenclick(follow_pointer)

# Keep the window open
screen.mainloop()
    

