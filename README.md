from random import *
def game1():
    true_numb = randint(1,50)
    num = int(input("Вгадай число від 1 до 50:"))
    while num != true_numb:
        if true_numb > num:
            print("мое число більше")
        elif true_numb < num:
            print("мое число менше")
        num = int(input("Введіть число:"))
    print("Ти правильно ввів число")
    print("вітаю з перемогою")
   
def game2():
    chislo = randint(1,100) 
    chislo2 = randint(1,150)
    suma = int(input(f"Порахуй суму чисел {chislo} + {chislo2}"))
    while (chislo + chislo2) != suma:
        print("це не правильно, пробуй ще")
        suma = int(input(f"Порахуй суму чисел {chislo} + {chislo2}"))
    print(" це правильно")
game = ""
while game != "ні":
    print("Привіт,обери гру.Додавання або Вгадай число")
    name_game = input("Додавання або Вгадай число")
    if name_game.capitalize() == "Додавання":
        print("Ви вибрали гру Додавання")
        game2()
    elif name_game.lower() == "вгадай число":
        print("Ви вибрали гру вгадай число")
        game1()
    else:
        print("такої гри немає")
        continue
    game = input("Хочеш продовжити далі?")
