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

