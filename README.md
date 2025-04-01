import turtle
import time

def draw_heart():
    # Thiết lập màn hình
    screen = turtle.Screen()
    screen.title("Trái Tim Nhấp Nháy")
    screen.bgcolor("black")
    
    # Tạo và thiết lập turtle
    pen = turtle.Turtle()
    pen.hideturtle()
    pen.speed(0)
    
    # Hàm vẽ trái tim với màu sắc cụ thể
    def heart(color):
        pen.clear()
        pen.color(color)
        pen.fillcolor(color)
        
        pen.up()
        pen.goto(0, -150)
        pen.down()
        
        pen.begin_fill()
        pen.left(140)
        pen.forward(224)
        
        for i in range(200):
            pen.right(1)
            pen.forward(2)
        
        pen.left(120)
        for i in range(200):
            pen.right(1)
            pen.forward(2)
            
        pen.forward(224)
        pen.end_fill()
    
    # Hiệu ứng nhấp nháy
    colors = ["red", "deep pink", "hot pink", "pink"]
    try:
        while True:
            for color in colors:
                heart(color)
                time.sleep(0.5)
    except:
        screen.bye()

# Chạy chương trình
if __name__ == "__main__":
    draw_heart()
