# intropython
Scripts del curso  Introduction to Computer Science de Udacity

# Clase 5: Procedures

# Ejercicio 1:
# Define a procedure, sum3, that takes three
# inputs, and returns the sum of the three
# input numbers.
# To help you out, the code for sum(a,b) is below.
# Ejemplos:
#print sum3(1,2,3) #>>> 6
#print sum3(93,53,70)#>>> 216
# Respuesta:
def sum3(a, b, c):
    return a + b + c

x=1
y=2
z=3

print sum3(x, y, z)

# Ejercicio 15: 

# Define a procedure, find_second, that takes
# two strings as its inputs: a search string
# and a target string. It should return a
# number that is the position of the second
# occurrence of the target string in the
# search string.
#Respuesta:
def find_second (a, b): 
    first = a.find (b)
    return a.find (b, first+1)
    
danton = "De l'audace, encore de l'audace, toujours de l'audace"

print find_second(danton, 'audace')

#>>> 25

# Ejercicio 17:
# Define a procedure, bigger, that takes in
# two numbers as inputs, and returns the
# greater of the two inputs.

def bigger(a, b):
    if a > b:
        return a
    return b

print bigger(6, 7)
print bigger(8, 7)

# otra posibilidad seria:

def bigger(a,b):
    if a > b:
        return a
    else:
        return b

print bigger(6, 7)
print bigger(8, 7)

# Ejercicio 18:
# Define a procedure, is_friend, that
# takes a string as its input, and
# returns a Boolean indicating if
# the input string is the name of
# a friend. Assume I am friends with
# everyone whose name starts with D
# and no one else. You do not need to
# check for the lower case 'd'

# Respuesta: 
def is_friend (name):
    if name[0] == 'D':
        return True
    else: 
        return False
    
print is_friend('Diane')
print is_friend('Fred')

# otra forma de hacerlo: como queremos recuperar un valor booleano (True/False) es suficiente con que el procedimiento describa una ecuación comparativa... así que no es estructamente necesario usar un if-statement:

def is_friend(name):
    return name[0] == "D"

print is_friend('Diane')
print is_friend('Fred')

# Ejercicio 19:

# Define a procedure, is_friend, that takes
# a string as its input, and returns a
# Boolean indicating if the input string
# is the name of a friend. Assume
# I am friends with everyone whose name
# starts with either 'D' or 'N', but no one
# else. You do not need to check for
# lower case 'd' or 'n'

def is_friend (name):
    if name[0] == 'D':
        return True
    if name[0] == "N": 
        return True
    else: 
        return False
    
print is_friend('Diane')
print is_friend('Ned')
print is_friend('Moe')

def is_friend (name):
    if name[0] == 'D':
        return True
    else: 
        if name[0] == "N": 
            return True
        else: 
            return False
    
print is_friend('Diane')
print is_friend('Ned')
print is_friend('Moe')

# Ejercicio 21 (no lo resolví):
# Define a procedure, biggest, that takes three
# numbers as inputs and returns the largest of
# those three numbers.

def biggest(a,b,c):
    if a > b:
        if a > c:
            return a
        else:   
            return c
    else:
        if b > c:
            return b
        else:
            return c

print biggest(3, 6, 9)
#>>> 9
print biggest(6, 9, 3)
#>>> 9
print biggest(9, 3, 6)
#>>> 9
print biggest(3, 3, 9)
#>>> 9
print biggest(9, 3, 9)
#>>> 9

# O se puede repetir dos veces un proceso menor: bigger. 
# De esa manera, se despeja primer el mayor entre a y b, 
# y ese resultado se compara con c, despejando el mayor
# de los tres:

def bigger (a,b):
    if a > b:
        return a
    else:
        return b

def biggest(a,b,c):
    return bigger (bigger(a,b),c)
        
print biggest(3, 6, 9)
#>>> 9
print biggest(6, 9, 3)
#>>> 9
print biggest(9, 3, 6)
#>>> 9
print biggest(3, 3, 9)
#>>> 9
print biggest(9, 3, 9)
#>>> 9

# Ejercicio 22:

# Define a procedure, print_numbers, that takes
# as input a positive whole number, and prints 
# out all the whole numbers from 1 to the input
# number.

# Make sure your procedure prints "upwards", so
# from 1 up to the input number.

def print_numbers(a):
    x = 0
    while a > x:
        x = x + 1
        print x

print print_numbers(10)


# Ejercicio 23 (no lo resolví):
# Define a procedure, factorial, that
# takes one number as its input
# and returns the factorial of
# that number.

def factorial(n):
    result = 1
    while n >= 1:
        result =  result*n       
        n = n - 1
    else: 
        return result

print factorial(4)

#print factorial(4)
#>>> 24
#print factorial(5)
#>>> 120
#print factorial(6)
#>>> 720

# Ejercicio 27-28: 

def get_next_target(page)
    start_link = page.find("<href=")
    start_quote = page.find('"', start_link)
    end_quote = page.find ('"', start_quote+1)
    url = page[start_quote+1:end_quote]
    return url, end_quote
# en la siguiente lína se asignan los valores de url y de endquote a las variables url y endpos.
url, endpos = def get_next_target(page)

page = page[end_quote:]

start_link = page.find("<href=")
start_quote = page.find(""", start_link)
end_quote = page.find (""", start_quote+1)
url = page[start_quote+1:end_quote]
print url

# Ejercicio 29:

def get_next_target(page):
    start_link = page.find('<a href=')
    
        # if the link tag sequence is not found, find returns a -1
    if start_link == -1:
        # return the error codes of None, 0 now and skip the rest!
        return = None, 0
    
    start_quote = page.find('"', start_link)
    end_quote = page.find('"', start_quote + 1)
    url = page[start_quote + 1:end_quote]
    return url, end_quote
    
url, endpos = def get_next_target(page)
    
# Ejercicio 30:

def get_next_target(page):
    start_link = page.find('<a href=')
        if start_link == -1:
            return = None, 0
    start_quote = page.find('"', start_link)
    end_quote = page.find('"', start_quote + 1)
    url = page[start_quote + 1:end_quote]
    return url, end_quote
    
url, endpos = def get_next_target(page)

page = page[endpos:]

url, endpos = def get_next_target(page)

page = page[endpos:]

url, endpos = def get_next_target(page) 

def print_all_url(page):
    while True:
        url, endpos = def get_next_target(page)
        if url:
            print url
            page=page[endpos:]
    else: 
        break
        
        
# Ejercicios de repaso:

# Ejercicio 3: Median
ef bigger(a,b):
    if a > b:
        return a
    else:
        return b

def biggest(a,b,c):
    return bigger(a,bigger(b,c))

def smallest(a,b,c):
    return smaller(a,smaller(b,c))

def median(a,b,c):
    big = biggest(a,b,c)
    if big == a:
        return bigger(b,c)
    if big == b:
        return bigger(a,c)
    else:
        return bigger(a,b)

print(median(1,2,3))
#>>> 2

print(median(9,3,6))
#>>> 6

print(median(7,8,7))
#>>> 7

# Ejercicio 4: Blastoff!
# Define a procedure, countdown, that takes a
# positive whole number as its input, and prints
# out a countdown from that number to 1,
# followed by Blastoff!
# The procedure should not return anything.
# For this question, you just need to call 
# the procedure using the line
# countdown(3)
# instead of print countdown(3).

def countdown(n):
    n > 0
    while n > 0:
        print n
        n = n-1
    else: 
        print "Blastoff!"

print countdown(6)

# Ejercicio 6: Find Last

# Define a procedure, find_last, that takes as input
# two strings, a search string and a target string,
# and returns the last position in the search string
# where the target string appears, or -1 if there
# are no occurrences.
#
# Example: find_last('aaaa', 'a') returns 3

# Make sure your procedure has a return statement.

# Mi solución:
def find_last(a,b):
    first_pos = a.find(b)
    next_pos = a.find(b,first_pos+1)
    if next_pos == -1:
        return first_pos
    else: 
        while next_pos != -1:
            first_pos = first_pos + 1
            next_pos = a.find(b,first_pos+1)
        else:
            return first_pos
    
# La solución del profesor: 
def find_last(s,t):
    last_pos = -1
    while True
        pos = s.find(t, last_pos+1)
        if pos == -1:
            return last_post
        last_post = pos


print find_last('aaaa', 'a')
#>>> 3

print find_last('aaaaa', 'aa')
#>>> 3

print find_last('aaaa', 'b')
#>>> -1

print find_last("111111111", "1")
#>>> 8

print find_last("222222222", "")
#>>> 9

print find_last("", "3")
#>>> -1

print find_last("", "")
#>>> 0



