from termcolor import colored
import random


off_color = {1: "➀", 2: "➁", 3: "➂", 4: "➃", 5: "➄",
             6: "➅", 7: "➆", 8: "➇", 9: "➈", 10: "➉"}

on_color = {1: "➊", 2: "➋", 3: "➌", 4: "➍", 5: "➎",
             6: "➏", 7: "➐", 8: "➑", 9: "➒", 10: "➓"}

class Pin(object):
  IN = 0
  OUT = 1

  def __init__(self, pin_number=None, type=None):
    self.pin = pin_number
    self.type = type
    self._value = 0
    self.ON = None
    self.random_values = []
    if self.type == Pin.IN:
      l = [0 for i in range(random.randint(3,7))] + [1 for i in range(random.randint(3,7))] 
      random.shuffle(l)
      self.random_values = l
      

  def value(self, value=None):
    if self.type == Pin.IN and value is None:
      self._value = random.choice(self.random_values)
    if value is not None:
      self._value = value
    print(colored(f" {self._value} ", "white" ,"on_red"))
    return self._value

  def on(self):
    if self.type == Pin.OUT:
      self.ON = True
      self._value = 1
      print(colored(on_color[self.pin],'green'))

  def off(self):
    if self.type == Pin.OUT:
      self.ON = False
      self._value = 0
      print(colored(off_color[self.pin],'green'))
