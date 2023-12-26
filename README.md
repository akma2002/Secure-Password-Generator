import random

digits = '0123456789'
lowercase_letters = 'abcdefghijklmnopqrstuvwxyz'
uppercase_letters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
punctuation = '#$%&*+-=?@^_'
chars = ''

q1=input('Введите количество паролей для генеации')
q2=input('Введите длину пароля')
q3=input('Включать ли цифры в пароль + = да')
q4=input('Включать ли прописные буквы + = да')
q5=input('Включать ли строчные буквы + = да')
q6=input('Включать ли символы + = да')
q7=input('Исключать ли неоднозначные символ + = да')
if q3 == '+':
    chars=chars+digits
if q4 == '+':
    chars=chars+lowercase_letters
if q5 == '+':
    chars=chars+uppercase_letters
if q6 == '+':
    chars=chars+punctuation

def generate_password(length, chars):
    password = ''
    for j in range(length):
        password += random.choice(chars)
    return password
            
for _ in range(int(q1)):
    print(generate_password(int(q2), chars))
