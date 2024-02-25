Привіт!
Настав час об'єднати наші попередні домашні завдання в одне.

Зараз ми нарешті ми об'єднаємо попередні домашні завдання в один функціональний проєкт. Сьогодні ти навчишся:

• Створенню класу Birthday з можливістю додавання поля для дня народження до контакту 

• Підтримці нового списку команд, включаючи обробку додавання та показу дня народження для контактів. 

• Коректному закриттю програми після виконання команди close або exit

Формат здачі: Розмістіть файли з розв'язанням у репозиторії goit-core-hw-07, та прикріпіть лінки до них у відповідь на домашнє завдання.

Поїхали!🚀

Ми продовжимо робити консольного бота помічника. Настав час об'єднати наші попередні домашні завдання в одне.
По перше додамо додатковий функціонал до класів з попередньої домашньої роботи:
Додайте поле birthday для дня народження в клас Record . Це поле має бути класу Birthday. Це поле не обов'язкове, але може бути тільки одне.
class Birthday(Field):
    def __init__(self, value):
        try:
            # Додайте перевірку коректності даних
            # та перетворіть рядок на об'єкт datetime
        except ValueError:
            raise ValueError("Invalid date format. Use DD.MM.YYYY")

class Record:
    def __init__(self, name):
        self.name = Name(name)
        self.phones = []
        self.birthday = None

Додайте функціонал роботи з Birthday у клас Record, а саме функцію add_birthday, яка додає день народження до контакту.
Додайте функціонал перевірки на правильність наведених значень для полів Phone, Birthday.
Додайте та адаптуйте до класу AddressBook нашу функцію з четвертого домашнього завдання, тиждень 3, get_upcoming_birthdays, яка для контактів адресної книги повертає список користувачів, яких потрібно привітати по днях на наступному тижні.
Тепер ваш бот (4 домашнє завдання тиждень 5) повинен працювати саме з функціоналом класу AddressBook. Це значить, що замість словника contacts ми використовуємо book = AddressBook()
Для реалізації нового функціоналу також додайте функції обробники з наступними командами:
add-birthday - додаємо до контакту день народження в форматі DD.MM.YYYY
show-birthday - показуємо день народження контакту
birthdays - повертає список користувачів, яких потрібно привітати по днях на наступному тижні
@input_error
def add_birthday(args, book):
    # реалізація
@input_error
def show_birthday(args, book):
    # реалізація
@input_error
def birthdays(args, book):
    # реалізація
Тож в фіналі наш бот повинен підтримувати наступний список команд:
add [ім'я] [телефон]: Додати новий контакт з іменем та телефонним номером.
change [ім'я] [новий телефон]: Змінити телефонний номер для вказаного контакту.
phone [ім'я]: Показати телефонний номер для вказаного контакту.
all: Показати всі контакти в адресній книзі.
add-birthday [ім'я] [дата народження]: Додати дату народження для вказаного контакту.
show-birthday [ім'я]: Показати дату народження для вказаного контакту.
birthdays: Показати дні народження, які відбудуться протягом наступного тижня.
hello: Отримати вітання від бота.
close або exit: Закрити програму.

def main():
    book = AddressBook()
    print("Welcome to the assistant bot!")
    while True:
        user_input = input("Enter a command: ")
        command, *args = parse_input(user_input)

        if command in ["close", "exit"]:
            print("Good bye!")
            break

        elif command == "hello":
            print("How can I help you?")

        elif command == "add":
            # реалізація

        elif command == "change":
            # реалізація

        elif command == "phone":
            # реалізація

        elif command == "all":
            # реалізація

        elif command == "add-birthday":
            # реалізація

        elif command == "show-birthday":
            # реалізація

        elif command == "birthdays":
            # реалізація

        else:
            print("Invalid command.")

Критерії оцінювання:

Реалізувати всі вказані команди до бота
Всі дані повинні виводитися у зрозумілому та зручному для користувача форматі
Всі помилки, такі як неправильний ввід чи відсутність контакту, повинні оброблятися інформативно з відповідним повідомленням для користувача
Валідація даних:
Дата народження має бути у форматі DD.MM.YYYY.
Телефонний номер має складатися з 10 цифр.
Програма повинна закриватися коректно після виконання команд close або exit

Формат здачі: Розмістіть файли з розв'язанням у репозиторії goit-core-hw-07 , та прикріпіть лінки до них у відповідь на домашнє завдання. 

Формат оцінювання: залік/не залік