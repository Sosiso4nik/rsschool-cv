# Cherny Vladislaw

***
### Python teacher in onine school 
### and 
### trainee front-end developer
***

## Contact information:
__Phone__: +375447131011
__E-mail__: chernyj.for.learn@gmail.com
__GitHub__: @Sosiso4nik
__Telegram__: @BChernyj
__Discord__: vladislaw(Сладкий мишка)) 

-------------------------------

## Skills and Profiency:
* HTML/CSS
* Java BASIC
* Python Back-end
* Git, GitHub
* PyCharm, VS CODE
* 3D modeling in Blender

------------------------------

## About me:
Hi friend, as you've already read at the beginning of my CV, my name is Vlad. I enjoy programming, and I also like teaching others. I teach Python development to children at an online programming school. I'm also interested in 3D modeling, and in the future, I would like to develop in that direction as well. Thank you for paying attention to my CV, and good luck to you going forward!

------------------------------

## Code example:
### Paint app with KIVY library on Python Language:
```
from kivy.core.window import Window

from kivy.app import App
from kivy.uix.button import Button
from kivy.uix.widget import Widget
from kivy.graphics import (Color, Ellipse, Rectangle, Line)

from random import random

class PainterWidget(Widget):
    def on_touch_down(self, touch):
        with self.canvas:
            Color(random(),random(),random(),1)
            rad = 10
            Ellipse(pos=(touch.x-rad/2,touch.y-rad/2), size=(rad, rad))
            touch.ud['line']=Line(points=(touch.x,touch.y), width = 5)

    def on_touch_move(self, touch):
        touch.ud['line'].points += (touch.x,touch.y)

class PaintApp(App):
    def clear_canvas(self, instance):
        self.painter.canvas.clear()

    def save_canvas(self, instance):
        self.painter.size = (Window.size[0], Window.size[1])
        self.painter.export_to_png('image.png')

    def build(self):
        parent = Widget()
        self.painter = PainterWidget()
        parent.add_widget(self.painter)

        parent.add_widget(Button(text='Clear', on_press=self.clear_canvas, size=(100, 50)))
        parent.add_widget(Button(text='Save', on_press=self.save_canvas, size=(100, 50), pos = (100, 0)))
        return parent

if __name__ == "__main__":
    PaintApp().run()
```
---

## Language:
* English: A2+
* Russian: Native