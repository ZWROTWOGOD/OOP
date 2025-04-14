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