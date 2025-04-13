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

student1 = Student("Anton", 70)
student2 = Student("Anna", 87)
print(student1.get_score())  # Вывод: Student Anton has score 70
print(student2.get_score())  # Вывод: Student Anna has score 87