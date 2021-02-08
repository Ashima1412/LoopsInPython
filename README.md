# LoopsInPython
Understand concepts of Python
#1 What is the output of the following code?


nums = set([1,1,2,3,3,3,4,4])
print(len(nums)

Output

4

#2 What will be the output?

d = {"john":40, "peter":45}
print(list(d.keys()))

Output

['john', 'peter']

#3 A website requires a user to input username and password to register. Write a program
to check the validity of password given by user. Following are the criteria for checking
password:
1. At least 1 letter between [a-z]
2. At least 1 number between [0-9]
1. At least 1 letter between [A-Z]
3. At least 1 character from [$#@]
4. Minimum length of transaction password: 6
5. Maximum length of transaction password: 12

Code:

import re
userid = input('enter your user id: ')
pwd= input("enter your password: ")
x = True
while x:  
    if (len(pwd)<6 or len(pwd)>12):
        break
    elif not re.search("[a-z]",pwd):
        break
    elif not re.search("[0-9]",pwd):
        break
    elif not re.search("[A-Z]",pwd):
        break
    elif not re.search("[$#@%&*]",pwd):
        break
    elif re.search("\s",pwd):
        break
    else:
        print("Valid Password")
        x=False
        break

if x:
    print("Not a Valid Password")


Output:

enter your user id: ashima
enter your password: ashi12@A
Valid Password


#4 Write a for loop that prints all elements of a list and their position in the list

Code:

str1 = [4,7,2,9,3]
str2=[]
n=len(str1)
for i in range(n):
    str2.append(i)
print('The index of ',str1)
print('is ',str2)

Output:

The index of  [4, 7, 2, 9, 3]
is  [0, 1, 2, 3, 4]

#5 Please write a program which accepts a string from console and print the
characters that have even indexes.

Code:

str1 = input('enter string ')
str2=[]
#n=len(str1)
for i in str1:
    if(i.isalpha() and str1.index(i)%2==0):
        str2.append(i)
        #print(i,str1.index(i))
    else:
        pass
print('The final list is: ',str2)
#convert list to string
str3=''.join(str2)
print('The final string is: ',str3)

Output:

enter string H1e2l3l4o5w6o7r8l9d
The final list is:  ['H', 'e', 'l', 'l', 'o', 'w', 'o', 'r', 'l', 'd']
The final string is:  Helloworld


#6 Please write a program which accepts a string from console and print it in reverse
order.


Code:

str1 = input('enter the string: ')
str2 = ''.join(reversed(str1))
print('Reversed string is: ',str2)

Using Function:

def string_rev(s):
    str2=''
    for i in s:
        str2 = i+str2
    return str2

str1 = input('enter the string: ')    
str3=string_rev(str1)
print('Reverse string is: ',str3)

Output:

enter the string: I am ashima gupta
Reversed string is:  atpug amihsa ma I

#7 Please write a program which count and print the numbers of each character in a
string input by console.


Code:

str1=input('enter the string  ')
freq = {}
for i in str1:
    if i in freq:
        freq[i]+=1
    else:
        freq[i]=1
print('occurence of each character is: ',freq)

Output:

enter the string  ashimagupta
occurence of each character is:  {'a': 3, 's': 1, 'h': 1, 'i': 1, 'm': 1, 'g': 1, 'u': 1, 'p': 1, 't': 1}



#8 With two given lists [1,3,6,78,35,55] and [12,24,35,24,88,120,155], write a
program to make a list whose elements are intersection of the above given lists

Code:

list1 = [1,3,6,78,35,55,24]
list2 = [112,24,35,24,88,120,155]
list3=[]
for i in list1:
    for j in list2:
        if(i==j):
            list3.append(i)

print('Intersection of two list is: ',set(list3))



#9 By using list comprehension, please write a program to print the list after removing
the value 24 in [12,24,35,24,88,120,155].

Code:

list1 =  [12,24,35,70,88,120,155]
list1 = [i for i in list1 if i!=24]
print(list1)



#10 .By using list comprehension, please write a program to print the list after removing
the 0th,4th,5th numbers in [12,24,35,70,88,120,155].

Code:
list1 =  [12,24,35,70,88,120,155]
list1 = [i for i in list1 if list1.index(i)!=0 and list1.index(i)!=4 and list1.index(i)!=5]
print(list1)



#11 By using list comprehension, please write a program to print the list after removing
delete numbers which are divisible by 5 and 7 in [12,24,35,70,88,120,155].

Code:

list1 =  [12,24,35,70,88,120,155]
list1 = [i for i in list1 if i%5!=0 or i%7!=0]
print(list1)



#12 Write a program to compute 1/2+2/3+3/4+...+n/n+1 with a given n input by
console (n>0).

Code:

def pattern1(n):
    sum1=0
    for i in range(1,n+1):
        sum1 = sum1+(i/(i+1))
    #print('sum is: ',sum1)
    return sum1
n1 = int(input('enter the value of n '))
print('sum is: ',pattern1(n1))


