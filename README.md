#Exercise 1
import re 
if name == '__main__':
 string = "YourString123" 
pattern = re.compile("[A-Za-z0-9]+")
 # if found match (entire string matches pattern)
 if pattern.fullmatch(string) is not None:
 print("Found match: " + string) 
else: 
# if not found match
 print("No match")
#Exercise 2
import re
def text_match(text): 
patterns = '\w*ab.\w*' 
if re.search(patterns, text): 
return 'Found a match!' 
else:
 return('Not matched!')
 print(text_match("its about to rain."))
print(text_match("abnormal to see too much of crowd."))
#Exercise 3
import re
def end_num(python):
 text = re.compile(r".*[0-9]$")
 if text.match(python):
 return True 
else: 
return False 
print(end_num('python6'))
print(end_num('python7'))
#Exercise 4
import re
results = re.finditer(r"([0-9]{1,3})", "Exercises number 1, 12, 13, and 345 are important")
print("Number of length 1 to 3")
for n in results: 
print(n.group(0))
#Exercise 5
import re
def text_match(text):
 patterns = '^[A-Z]*$' 
if re.search(patterns, text):
 return 'Found a match!'
 else:
 return('Not matched!')
 print(text_match("MULTIPLICATION"))
print(text_match("ADDITION"))
