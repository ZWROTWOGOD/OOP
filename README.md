Тут я буду рассуждать по поводу ООП обЪекты и классы
```python
# Это класс (чертеж)
class car:
    def __init__(self,brand,color):
      self.brand=brand # характеристики : марка
      self.color=color # характеристики : цвет

    def drive(self): # метод: ехать
        return f"car {self.color} {self.brand} едет" 

# Это обьекты (конкретные машины)
car1 = car("ford" , "red")
car2 = car("tesla" , "blue")
print(car1.drive()) # Вывод: Red Ford едет!
print(car2.drive()) # Вывод: Blue Tesla едет!
 







 class Student:
    def __init__(self, name, score):
        self.name = name
        self.score = score

    def get_score(self):
        return f"Student {self.name} has score {self.score}"
    def set_score(self, new_score): 
        if 0 <= new_score <= 100:
             self.score = new_score
             return f"Score updated to {self.score}"
        else:

             return "Invalid score! Must be between 0 and 100"
student1 = Student("Anton", 70)
student2 = Student("Anna", 87)
print(student1.get_score())  # Вывод: Student Anton has score 70
print(student2.get_score())  # Вывод: Student Anna has score 87 
print(student1.set_score(85))
print(student1.get_score()) 
# upd буду добавлять каждый день в код что то новое ))))




class Runner:
  def __init__(self, name, time, color, round=False):
      self.name = name
      self.place = None  # место пока не известно
      self.time = time
      self.round = round  # номер круга
      self.color = color  # цвет спортсмена (для вывода на экран)

  def __str__(self):
      if self.round:
          return f"{self.name} в {self.color} — провалился на {self.round} круге"
      return f"{self.name} в {self.color} пробежал за {self.time} сек, {self.place} место"

  @staticmethod
  def sort_runners(runners):
      valid_runners = [r for r in runners if not r.round]
      valid_runners.sort(key=lambda x: x.time)
      # Присваиваем места
      for i, runner in enumerate(valid_runners, 1):
          runner.place = i
      return runners

# Создаём список бегунов после определения класса
runners = [
  Runner("anton", 12.3, color="red"),
  Runner("oleg", 10.5, color="blue", round=True),
  Runner("dima", 12.5, color="green"),
  Runner("sergey", 11.5, color="black"),
  Runner("pavel", 17.3, color="yellow"),
  Runner("vlad", 10.9, color="white"),
]

# Сортируем и выводим
runners = Runner.sort_runners(runners)
for runner in runners:
  print(runner)