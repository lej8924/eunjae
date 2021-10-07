__#python03-lab submission#__

* 제일 처음 화면을 켰을 때 나타나는 모습
  
<img scr="https://user-images.githubusercontent.com/71022086/136337115-285abde8-e4fb-46f0-a418-b3a0223f9c9e.png">

```python
    turtle.title("turtle_runaway_game") //"turtle_runaway_game"이라는 타이틀을 달아줌
    turtle.bgcolor("grey") //배경색을 회색으로 변경
    self.drawer.color("violet") //나타나는 글씨 색상을 보라색으로 변경
    self.drawer.write(f'Is catched? {is_catched} elapse:{elapse:.0f}\n score: {self.score}',font=("Times New Roman",15,"normal"))
    //elapse와 score를 추가하고, 폰트 크기와 글꼴을 변경함
 ```
    
*************************************************************

* score가 20이 되었을 때 게임이 종료되는 모습
* 
<img scr="https://user-images.githubusercontent.com/71022086/136337121-5f9c8a3f-617e-46b2-8093-af5d825a5ed2.png">

```python
    if(is_catched==True): //chaser가 runner를 잡았을 때 
            self.score+=1 //score에 1을 더해줌
            if(self.score==20)://score가 20이 되었을 때
                self.drawer.setpos(-300,0) //drawer거북이의 위치를 옮김
                self.drawer.color("red") //drawer거북이의 색상을 빨간색으로 변경
                self.drawer.write('종료를 원하시면 화면을 클릭!',font=("Times New Roman",25,"normal")) //"종료를 원하시면 화면을 클릭!"을 띄움
                turtle.exitonclick() //화면을 클릭하면 turtle게임을 중지함
                
                
    def __init__(self, canvas, runner, chaser, catch_radius=20, init_dist=400, score=0): // score=0을 추가해줌
    self.score = score
 ```
 
 
 
 
 
