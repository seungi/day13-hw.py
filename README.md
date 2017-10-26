# day13-hw.py
import turtle as t #거북이 모형 사용
import random #랜덤 사용
t.up() #펜의 꼬리를 올림(색칠이 안되게 한다)
t.forward(250) #앞으로 250만큼 간다
t.down() #펜의 꼬리를 내린다(앞으로 색칠이 되게 한다)
#500x500 사각형을 그린다
t.left(90)
t.forward(250)
t.left(90)
t.forward(500)
t.left(90)
t.forward(500)
t.left(90)
t.forward(500)
t.left(90)
t.forward(250)

#거북이를 원래상태로로 돌려놓는다
t.up()
t.left(90)
t.forward(250)
t.right(180)

a = random.randint(1, 360) #a라는 변수를 지정한다. 1부터 360까지 컴퓨터에서 랜덤으로 뽑는다.
speed = 5 #speed라는 변수를 5로 지정한다.
t.listen() #과정이 실행되게 한다.
while True: #무한 반복
  t.forward(speed) #speed만큼 앞으로 간다
  if t.xcor() > 250 or t.xcor() < -250: #만약 x의 좌표값이 250보다 크거나, -250보다 작을 경우
    t.right(a) #a만큼 오른쪽으로 회전한다.
  if t.ycor() > 250 or t.ycor() < -250: #만약 y의 좌표값이 250보다 크거나, -250보다 작을 경우        
    t.right(a) #a만큼 오른쪽으로 회전한다.    
    t.forward(speed) #speed만큼 앞으로 간다
