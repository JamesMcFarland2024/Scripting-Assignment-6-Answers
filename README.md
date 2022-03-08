# Scripting-Assignment-6-Answers

#Question 1

class Student
def__init__(self, first_name, last_name, email, all_course):
        self.first_name = first_name
        self.last_name = last_name
        self.email = email
        self.all_course = all_course
	
#Read sentences & extract only line which contain the keywords

import students.txt
import re

#Open file

keyword = open('students.txt', 'r', encoding = 'utf-8').readlines()
texts = open('sent_token.txt', 'r', encoding = 'utf-8').readlines()

#Define function to read file & remove next line symbol

def read_file(students.txt):
    texts = []
    for word in file:
        text = word.rstrip('\n')
        texts.append(text)
    return texts
    
#Save to variable   

key = read_file(keyword)
corpus = read_file(texts
from nltk.tokenize import sent_tokenize
text = open('Input/data.txt', 'r', encoding = 'utf-8')
text_file = open("Output/sent_token.txt", "w", encoding='utf-8')
string_without_line_breaks = ""
for line in text:
    stripped_line = line.rstrip() + " "
    string_without_line_breaks += stripped_line
sent_token = sent_tokenize(string_without_line_breaks)
for word in sent_token:
    text_file.write(word)
    text_file.write("\n")
text_file.close()

print("*This Program Contains Student Information*")

D = dict()

n = int(input('How many student records you want to store? '))

#Add student information to the dictionary

for i in range(0,n):
	x, y = input("Enter the complete name (First and last name) of student: ").split()
	z = input("Enter contact number: ")
	m = input('Enter Marks: ')
	D[x, y] = (z, m)
	
#Define a function for shorting names based on first name

def sort():
	ls = list()
	
	#Fetch key & value using items() method
	
	for sname,details in D.items():
	
		#Store key parts as an tuple
		
		tup = (sname[0],sname[1])
		
		#Add tuple to the list
		
		ls.append(tup)
		
  #Append the list of students from the file
   
   ls.append(students.txt)
    
	#Sort the final list of tuples
	
	ls = sorted(ls)
	for i in ls:
	
		#Print first name & second name
		
		print(i[0],i[1])
	
	return

#Define a function for finding the minimum marks in stored data

def minmarks():
	ls = list()
	
	#Fetch key & value using items() methods
	
	for sname,details in D.items():
	
		#Add details second element (marks) to the list
		
		ls.append(details[1])
	
	#Sort the list elemnts
	
	ls = sorted(ls)
	print("Minimum marks: ", min(ls))
	
	return

#Define a function for searching student contact number

def searchdetail(fname):
	ls = list()
	
	for sname, details in D.items():
	
		tup=(sname,details)
		ls.append(tup)
		
	for i in ls:
		if i[0][0] == fname:
			print(i[1][0])
	return

#Define a function for asking the options

def option():

	choice = int(input('Enter the operation detail: \n \
	1: Sorting using first name \n \
	2: Finding Minimum marks \n \
	3: Search contact number using first name: \n \
	4: Exit\n \
	Option: '))
	
	if choice == 1:
		#Function call
		sort()
		print('Want to perform some other operation? Y or N: ')
		inp = input()
		if inp == 'Y':
			option()
			
		#Exit function call
		exit()
		
	elif choice == 2:
		minmarks()
		print('Want to perform some other operation? Y or N: ')
		
		inp = input()
		if inp == 'Y':
			option()
		exit()
		
	elif choice == 3:
		first = input('Enter first name of student: ')
		searchdetail(first)
		
		print('Want to perform some other operation? Y or N: ')
		inp = input()
		if inp == 'Y':
			option()
			
		exit()
	else:
		print('Thank you! Goodbye!')
		exit()
		
option()

  
#Question 2

#Read the contents of each .txt file
f1 = open( 'f1.txt', 'r')
content = f1.read()
f1.close()

f2 = open('f2.txt', 'r')
content2 = f2.read()
f2.close()

f3 = open('f3.txt', 'r')
content3 = f3.read()
f3.close

#Write the contents of each .txt file into one function file called final_file.txt
f4 = open('final_file.txt', 'w')
f4.write(content)
f4.write(content2)
f4.write(content3)
f4.close()

#Safeguard if files don't exist
for x in l:
    if not os.path.exists(x):
        print >> sys.stderr , "No such file", x
