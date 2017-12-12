# intropython
Scripts del curso  Introduction to Computer Science de Udacity

#Guardando un cambio.

#Clase 5: Procedures

#Ejercicio 1:
# Define a procedure, sum3, that takes three
# inputs, and returns the sum of the three
# input numbers.
# To help you out, the code for sum(a,b) is below.
#Ejemplos:
#print sum3(1,2,3) #>>> 6
#print sum3(93,53,70)#>>> 216
#Respuesta:
def sum3(a, b, c):
    return a + b + c

x=1
y=2
z=3

print sum3(x, y, z)

#Ejercicio 15: 

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

