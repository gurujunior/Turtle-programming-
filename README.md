import turtle

# Function to draw a square with a given side length
def draw_square(side_length):
    for _ in range(4):
        turtle.forward(side_length)
        turtle.left(90)

# Function to draw a triangle with a given side length
def draw_triangle(side_length):
    for _ in range(3):
        turtle.forward(side_length)
        turtle.left(120)

# Set up the turtle
turtle.speed(1)
turtle.bgcolor("skyblue")
turtle.pensize(2)

# Draw the main body of the house
turtle.penup()
turtle.goto(-100, -100)
turtle.pendown()
draw_square(200)

# Draw the roof of the house
turtle.penup()
turtle.goto(-100, 100)
turtle.pendown()
draw_triangle(200)

# Draw the door
turtle.penup()
turtle.goto(-30, -100)
turtle.pendown()
draw_square(60)

# Draw the window on the left side
turtle.penup()
turtle.goto(-70, 0)
turtle.pendown()
draw_square(40)

# Draw the window on the right side
turtle.penup()
turtle.goto(30, 0)
turtle.pendown()
draw_square(40)

# Keep the window open until manually closed
turtle.done()
