# Turtle-Graphics-4
### Turtles drawing stars in random sizes where users click with their mouse

```python
import turtle
import random

def star(): #star라고 정의
    length=random.randint(1,300) #1~300중 랜덤으로 별의 선분길이 지정
    way=random.randint(0,360) #0~360중 랜덤으로 각도 지정
    t.setheading(way)
    for i in range(5): #별을 그리기 위해 직선과 왼쪽으로 144도 회전 짝꿍을 5번 반복
        t.fd(length)
        t.lt(144)
    pass

def mv(x,y):
    t.penup() #펜을 들어올림
    t.goto(x,y) #x,y의 위치로 감
    t.pendown() #펜을 내림(사용자가 별을 그릴 위치 마우스로 클릭)
    star() #위에 정의된 star() 함수가 실행된

t=turtle.Turtle()
t.shape("turtle")

turtle.onscreenclick(mv) #사용자의 마우스 클릭을 통해 거북이가 별을 그리도록 선언

```
