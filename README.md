import turtle
import math

screen = turtle.Screen()
screen.title("Indian National Flag - Tiranga")
screen.bgcolor("white")

flag = turtle.Turtle()
flag.speed(5)

def draw_rectangle(color, y):
    flag.penup()
    flag.goto(-300, y)
    flag.pendown()
    flag.color(color)
    flag.begin_fill()
    for _ in range(2):
        flag.forward(600)
        flag.right(90)
        flag.forward(100)
        flag.right(90)
    flag.end_fill()

draw_rectangle("orange", 100)     # Saffron
draw_rectangle("white", 0)        # White
draw_rectangle("green", -100)     # Green

chakra = turtle.Turtle()
chakra.speed(10)
chakra.penup()
chakra.goto(0, 0)
chakra.pendown()
chakra.color("navyblue")

chakra.begin_fill()
chakra.circle(45)
chakra.end_fill()

chakra.penup()
chakra.goto(0, 45)
chakra.setheading(270)
chakra.pendown()
chakra.color("white")
chakra.width(2)
for _ in range(24):
    chakra.forward(45)
    chakra.backward(45)
    chakra.left(15)

chakra.penup()
chakra.goto(0, 0)
chakra.dot(6, "navyblue")

flag.hideturtle()
chakra.hideturtle()

turtle.done()
