# Practice-makes-perfect
#From Codecademy

def is_int(x):
    if x - int(x) == 0:
        return True
    else:
        return False
float(raw_input("Enter a number: "))
print is_int(4.5)

#FACTORIAL MACHINE!!
def factorial(x):
    list = []
    for i in range(x):
        list.append(str(x))
        x -= 1
    total = 1
    for n in list:
        total *= int(n)
    print total
    return total
    
factorial(int(raw_input('enter a number to calculate the factorial:')))

#DETERMINE PRIME NUMBER
def is_prime(x):
    if x < 2:
        return False
    elif x == 2:
        return True
    for n in range(2, x):
        integer = int(x/n)
        y = float(x)
        w = float(n)
        decimal = (y/w)
        if (decimal - integer) == 0:
            print False
            return False
    else:
        print True
        return True
is_prime(int(raw_input('Enter a number to determine if it is prime:')))

#REVERSAL MACHINE
def reverse_a_string(a_string):
    a_string = str(a_string)
    new_strings = []
    index = len(a_string)
    while index:
        index -= 1                       
        new_strings.append(a_string[index])
    ''.join(new_strings)    
    final = ''.join(new_strings)
    print final
    return final

reverse_a_string(raw_input('enter input bro: '))

#Ant_vowel!
vowels = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']
def anti_vowel(text):
    no_vowels = ''
    for letters in text:
        if letters not in vowels:
            no_vowels += letters
    print no_vowels
    return no_vowels

anti_vowel('Coffee Meets Bagel')
