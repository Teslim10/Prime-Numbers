# Prime-Numbers
'''Create a program that receives inputs (as figures with commas and spaces) from a user, and supplies a list of all the prime numbers between 1 and that number.
The program receives, for example, the number, "1, 234, 567" from a user, removes all unneeded characters, and produces a list such as [2,3,5,7,11,13...]. 
Remember: A Prime Number is a number that has only two factors: 1 and itself.'''
prime_numbers = []
remainder = []
x = input("Lower limit: ")
y = input("Upper limit: ")
x = x.replace(" ", "") # This removes white or empty spaces from the input
x = x.replace(",", '') # This removes  comma from the input
y = y.replace(" ", "") # This removes white or empty spaces from the input
y = y.replace(",", '') # This removes  comma from the input
y = int(y) # This converts string to integer
div = 1
num = int(x)
while num <= y:
    while div <= y:
        remainder.append(num % div)
        div += 1   
    if remainder.count(0) == 2:
        prime_numbers.append(num)
    else:
        pass
    remainder = []
    div = 1
    num += 1
print(" ")
print(prime_numbers)
