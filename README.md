# Amor
Para el amor de mi vida 
import turtle
import time

# Configuración de pantalla
pantalla = turtle.Screen()
pantalla.bgcolor("lightpink")
pantalla.title("Para Janeth")

# Crear la tortuga
corazon = turtle.Turtle()
corazon.pensize(3)
corazon.color("red")
corazon.speed(1)

# Función para dibujar un corazón
def dibujar_corazon():
    corazon.begin_fill()
    corazon.left(140)
    corazon.forward(180)
    corazon.circle(-90, 200)
    corazon.left(120)
    corazon.circle(-90, 200)
    corazon.forward(180)
    corazon.end_fill()

# Dibujar el corazón
dibujar_corazon()

# Mensaje de amor
corazon.penup()
corazon.goto(0, -180)
corazon.color("white")
corazon.write("Te quiero, Janeth", align="center", font=("Arial", 18, "bold"))

# Animación de latido
for i in range(3):
    corazon.clear()
    corazon.color("darkred")
    dibujar_corazon()
    time.sleep(0.3)
    corazon.clear()
    corazon.color("red")
    dibujar_corazon()
    time.sleep(0.3)

# Final
corazon.hideturtle()
pantalla.mainloop()
