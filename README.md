# hirst-painting-project

# this program recreates the famous Hirst painting using Turtle graphics in Python
# i also used another module called colorgram.py to generate different colors from a photo on the net


import turtle as t
from turtle import Turtle, Screen
import random


# def random_colors():
#     r = random.randint(0, 255)
#     g = random.randint(0, 255)
#     b = random.randint(0, 255)
#
#     random_color = (r, g, b)
#     return random_color

"""You can generate a tuple of rgb colors from any image online with the codes below. 
Download the image and paste it into your project file. 
You can then download the colorgram module and import it to generate an RGB tuple list of colors"""

# import colorgram
# rgb_colors = []
# colors = colorgram.extract("image.jpeg", 10)
# for color in colors:
#     r = color.rgb.r
#     g = color.rgb.g
#     b = color.rgb.b
#     new_colors = (r, g, b)
#     rgb_colors.append(new_colors)

# print(rgb_colors)

color_list = [(237, 216, 95), (247, 152, 58), (236, 204, 236), (182, 215, 246), (83, 163, 235), (172, 170, 3), (206, 131, 187), (199, 70, 1), (128, 224, 184)]

tim = Turtle()
tim.shape("turtle")
tim.speed(6)
t.colormode(255)
tim.penup()
tim.hideturtle()
tim.setheading(255)
tim.forward(50)
tim.setheading(0)
number_of_dots = 100

for dot_count in range(1, number_of_dots + 1):
    tim.dot(15, random.choice(color_list))
    tim.forward(50)

    if dot_count % 10 == 0:
        tim.setheading(90)
        tim.forward(50)
        tim.setheading(180)
        tim.forward(500)
        tim.setheading(0)


