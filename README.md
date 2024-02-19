# Python-RegEx-or-Regular-Expression



# Regular-Expression:-
         -> A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.
         -> A regular expression (or RE) specifies a set of strings that matches it.
         -> A Regular Expression or RegEx is a special sequence of characters that uses a search pattern to find a string or set of strings.



import re
pattern = re.compile('Python')
print(pattern.finditer('Learning python is very easy'))



# start() - Start index of a match
# end() - end+1 index of a match
# group() - Return match String


import re
pattern = re.compile('cd')
matcher = pattern.finditer('cdcccdcdcdccdccdccd')
for match in matcher:
    print('match is available at the start index:',match.start())
    print('match is available at the start index:', match.end())
    print('match is available at the start index:', match.group())



# .

import re
count = 0
pattern = re.compile('cd')
matcher = pattern.finditer('cdcccdcdcdccdccdccd')
for match in matcher:
    count = count+1
    print('match is available at the start index:',match.start())
print('The number of occurences:',count)



# .

import re
count = 0
pattern = re.compile('cd')
matcher = pattern.finditer('cdcccdcdcdccdccdccd')
for match in matcher:
    count = count+1
    print('start:{},end:{},group{}'.format(match.start(),match.end(),match.group()))
print('The number of occurences:',count)



# [abc] - either a or b or c
# [^abc] - except a and b and c
# [a-z] - All the characters with lower case
# [A-Z] - All the characters with upper case
# [a-zA-Z] - Any Alphabet
# [0-9] - Any digits
# [a-zA-Z0-9] - All the alphabet and the numbers
# [^a-zA-z0-9] - All other character



import re
matcher = re.finditer('[a,z]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())




# .

import re
matcher = re.finditer('[^a,z]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())


# .

import re
matcher = re.finditer('[0,9]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('[a-z]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())


# .

import re
matcher = re.finditer('[A-Z]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())


# .

import re
matcher = re.finditer('[a-zA-Z]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('[0-9]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())


# .

import re
matcher = re.finditer('[a-zA-Z0-9]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .


import re
matcher = re.finditer('[^a-zA-z0-9]','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())





# Predefined Character classes

     # \s- search for space character
     # \S- Except space character
     # \d- Any digits
     # \D- Except digits
     # \w- Any word character either caps,small or digits(alpha numeric)
     # \W- special characters
     # . - Every characters


import re
matcher = re.finditer('\s','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('\S','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('\d','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('\D','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())



# .

import re
matcher = re.finditer('\w','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())




# .

import re
matcher = re.finditer('\W','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())


# .

import re
matcher = re.finditer('.','ab$Z12@9z t65&R')
for m in matcher:
    print(m.start(),'......',m.group())




# Quantifiers

import re
matcher = re.finditer('c','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())



# .

import re
matcher = re.finditer('d','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())


# .

import re
matcher = re.finditer('c+','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())



# .

import re
matcher = re.finditer('c*','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())


# .

import re
matcher = re.finditer('cd+','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())



# .

import re
matcher = re.finditer('c?','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())


# Atmost one c

import re
matcher = re.finditer('c{3}','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())


# .

import re
matcher = re.finditer('c{2,3}','cdcccdcdcdccdccdccd')
for m in matcher:
    print(m.start(),'.....',m.group())




# Import functions in RE Module:
   # match() - to check the given pattern at the begnning of the target string.
   # fullmatch()
   # search()
   # findall
   # finditer
   # sub()
   # subn()
   # split()
   # compile()


# match()

import re
s = input('Enter the pattern to check:')
m = re.match(s,'Python learning is Very simple and easy')
if m!=None:
    print('Match is available at the begnning of the starting')
    print('start index:{} and end index:{}'.format(m.start(),m.end()))
else:
    print('Match is not available at the not begnning of the started')



# fullmatch()


import re
s = input('Enter the pattern to check:')
m = re.fullmatch(s,'Python learning is Very simple and easy')
if m!=None:
    print('full string is match')
    print('start index:{} and end index:{}'.format(m.start(),m.end()))
else:
    print('full string is not match')




# search()


import re
s = input('Enter the pattern to check:')
m = re.search(s,'cdccddccdcdcdccdddccdcd')
if m!=None:
    print('searched string matched')
    print('start index:{} and end index:{}'.format(m.start(), m.end()))
else:
    print('searched string did not matched')



# findall

import re
s = input('Enter the pattern to check:')
m = re.findall(s,'cdccddccdcdcdccdddccdcd')
print(m)



# finditer
import re
matcher = re.finditer('cd','cdccddccdcdcdccdddccdcd')
for m in matcher:
    print(m.start(),m.end(),m.group())

    


# findall


import re
l = re.findall('\W','a7# !*9bvx8&^%123$')
print(l)

import re
l = re.findall('\w','a7# !*9bvx8&^%123$')
print(l)

import re
l = re.findall('\s','a7# !*9bvx8&^%123$')
print(l)

import re
l = re.findall('\S','a7# !*9bvx8&^%123$')
print(l)

import re
l = re.findall('\d','a7# !*9bvx8&^%123$')
print(l)





# sub()


import re
l = re.sub('\d','#','a7# !*9bvx8&^%123$')
print(l)



# subn() - return the tupple with result and no of replacement


import re
l = re.subn('\d','#','a7# !*9bvx8&^%123$')
print(l)
print(l[0])
print(l[1])

# split()


import re
l = re.split('-','10-20-30-40-50-60-70-80-90')
print(l)


# .

import re
l = re.split('\.','www.vikasmishra.in')
print(l)


# .

import re
l = re.split('[.]','www.vikasmishra.in')
print(l)


# .

import re
s = 'Learning python is very simple'
res = re.search('^Learn',s)
if res!=None:
    print('Target string start with Learn')
else:
    print('Target string does not start with Learn')



# .

import re
s = 'Learning python is very simple'
res = re.search('simple$',s)
if res!=None:
    print('Target string ends with simple')
else:
    print('Target string does not start with Learn')




# .

import re
s = 'Learning python is very SIMPLE'
res = re.search('simple$',s)
if res!=None:
    print('Target string ends with simple')
else:
    print('Target string does not start with Learn')



# .

import re
s = 'Learning python is very SIMPLE'
res = re.search('simple$',s,re.IGNORECASE)
if res!=None:
    print('Target string ends with simple')
else:
    print('Target string does not start with Learn')



# .


import re
s = input("Enter Phone No: ")
mn = re.fullmatch('(0|91|\+91|)?[678]\d{9}',s)
if mn!=None:
    print("Valid Phone No")
else:
    print("Not Valid Phone No")




# .


import re,urllib
import urllib.request
sites = ['http://google.com','http://readiff.com']
for s in sites:
    print('Searching...',s)
    u = urllib.request.urlopen(s)
    text = u.read()
    title = re.findall('<title>.*</title>',str(text),re.IGNORECASE)
    print(title[0])







