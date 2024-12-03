# exemple
import random
import time


class Player:
    def __init__(self):
        self.name = str(...)

        self.choice = ...

        self.attack = 0
        self.defense = 0
        self.health = 0

        self.character = {
            # 1: "Ученый",
            # 2: "Инженер",
            # 3: "Лидер"
            1: {'attack':random.randint(5, 8),
                'defense':random.randint(4, 7),
                'health':random.randint(30, 35)},

            2: {'attack':random.randint(7, 10),
                'defense':random.randint(3, 5),
                'health':random.randint(20, 28)},

            3: {'attack':random.randint(2, 6),
                'defense':random.randint(8, 18),
                'health':random.randint(30, 50)}
        }

        self.ex = 0
        self.inv = {}

    def attack(self, value, enemy):
        enemy.health -= value

    def get_attack(self, value):
        self.health -= value

class Enemy:
    def __init__(self, name, health, attack, defense):
        self.name = name
        self.health = health
        self.attack = attack
        self.defense = defense

    def attack(self, value, player):
        player.health -= value

    def get_attack(self, value):
        self.health -= value




class Play:
    def __init__(self):
        self.items = ["зелье здоровья", "зелье атаки", 'самогонка','ключ']
    player = Player()

    locations = []
    print('Добро пожаловать в (тупое название игры)')
    while True:
        player.name = input("Введите никнейм:\n")
        try:
            player.choice = int(input("Выберите класс:\n"))
            player.attack = player.character[player.choice]['attack']
            player.defense = player.character[player.choice]['defense']
            player.health = player.character[player.choice]['health']
        except:
            print("Введите корректные значения")
            continue

        print(f"{player.name} ,вы заблудились в лесу, вам нужно из него выбраться, для этого вам понадобиться победить врагов, которые встанут у вас на пути.")
        time.sleep(0.5)
        print("...")
        time.sleep(0.5)
        print("...")
        time.sleep(0.5)
        print("...")

        print('Начальная локация: Тропа')






        break


test = Play()

