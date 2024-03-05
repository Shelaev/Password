import random
import string


def generate_password(length, use_uppercase, use_digits, use_special_chars):
    password = ''
    if use_uppercase:
        password += string.ascii_uppercase
    if use_digits:
        password += string.digits
    if use_special_chars:
        password += string.punctuation
    password += string.ascii_lowercase

    password = ''.join(random.sample(password, length))

    return password


length = int(input("Введіть довжину паролю: "))
use_uppercase = input("Використовувати великі літери? (Так/Ні): ").lower() == 'так'
use_digits = input("Використовувати цифри? (Так/Ні): ").lower() == 'так'
use_special_chars = input("Використовувати спеціальні знаки? (Так/Ні): ").lower() == 'так'

password = generate_password(length, use_uppercase, use_digits, use_special_chars)
print("Згенерований пароль:", password)

choice = input("Бажаєте зберегти пароль у файлі? (Так/Ні): ").lower()
if choice == 'так':
    filename = input("Введіть назву файлу: ")
    with open(filename, 'w') as file:
        file.write(password)
        print(f"Пароль збережено у файлі '{filename}'")
