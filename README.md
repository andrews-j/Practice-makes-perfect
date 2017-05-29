# Practice-makes-perfect
#From Codecademy

def is_int(x):
    if x - int(x) == 0:
        return True
    else:
        return False
float(raw_input("Enter a number: "))
print is_int(4.5)

# FACTORIAL MACHINE!!
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

# DETERMINE PRIME NUMBER
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

# REVERSAL MACHINE
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

# Ant_vowel!
vowels = ['a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U']
def anti_vowel(text):
    no_vowels = ''
    for letters in text:
        if letters not in vowels:
            no_vowels += letters
    print no_vowels
    return no_vowels

anti_vowel('Coffee Meets Bagel')

# Scrabble Score
score = {"a": 1, "c": 3, "b": 3, "e": 1, "d": 2, "g": 2, 
         "f": 4, "i": 1, "h": 4, "k": 5, "j": 8, "m": 3, 
         "l": 1, "o": 1, "n": 1, "q": 10, "p": 3, "s": 1, 
         "r": 1, "u": 1, "t": 1, "w": 4, "v": 4, "y": 4, 
         "x": 8, "z": 10}

def scrabble_score(word):
    word= word.lower()
    total = 0
    for things in word:
        total += score[things]
    print total
    return total
scrabble_score(raw_input("Enter a word: "))

# CENSOR, EXAMPLE OF TEXT.SPLIT (HOW TO EXECUTE WITH RAW_INPUT??)

def censor(text, word):
    splited_text = text.split() # spliting large string and  storing in a variable
    x = [] # declaring empty list
    
    for string in splited_text: # iteration through the contents 
        if string == word:
            string = string.replace(word, "*" * len(string)) # replaces the word with *
            x.append(string) # stores the new word in the empty list
        else:
            x.append(string)    #???
   
    text = " ".join(x) #???
    print text
    return text

censor('yes we can', 'yes')

# COUNT FUNCTION (Tells you how many times a number appears in a list)
def count(sequence, item):
    x = 0
    for i in sequence:
        if i == item:
            x += 1
    else:
        x = x
        print x
    return x
    
count([1,2,2,2,2,2,3,4,5,6,5,4,3,4,5,6,5,4,5], 5)

# MEDIAN CALCULATOR (Not accepted by codecademy, but seems to work)
def median(values):
    values = sorted(values)
    length = len(values)
    if length == 1:
        return values[0]
    elif length % 2 == 0:
        sum = values[length/2] + values[(length/2)-1]
        sum = float(sum)
        return sum/2
    else:
        return values[(length)/2]
    
median([4,5,5,4])

# CODECADEMY ACCEPTED MEDIAN CODE:
def median(lst):
    lst = sorted(lst)
    length = len(lst)
    summa = 0
    if length == 1:
        return lst[0]
    elif length % 2 != 0:
        return lst[(length/2)]
    else:
        for i in lst[(length/2)-1:(length/2)+1]:
            summa += i
        return float(summa)/2
median([6, 8, 12, 2, 23]) 


for i in range(1,int(raw_input())+1): #More than 2 lines will result in 0 score. Do not leave a blank line also
    print range(i).join()


# Bobby's bizarre range code(DOESN'T WORK)
def range( end=None, start=None, step_size = None):	
    if end == None:
        return [0]
    if start == None:
        start = 1
    if step_size == None:
        step_size = 1
    rng = []
    entry = start
    while entry < int(end):
        rng.append(entry)
        entry+=step_size
    return rng

#s = raw_input()
e = raw_input()
#step = raw_input()

print range(e)
