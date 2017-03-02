# Learn Python the Hard Way
# Notes for ex37

# key words
1. del
code:
>>>a = [-1 , 3 , 'aa' , 85] #define a list
>>>a
[-1 , 3 , 'aa' , 85]
>>> del a[0] #delete element
>>>a
[3 , 'aa' , 85]
>>>del a[2:4] #delete the 2nd to 4th elements excludes the 4th
>>>a
[3 , 'aa']
>>> del a # delete all of the list

# global
If you wanna define a variable out of the function, you need to claim the variable is global. 
The key global is to serve for this job.
However, we don't recommend you to avoid doing so.
fun_g.py:
 def fun():
   global x
   print 'x is', x
   x = 2
   print 'changed local x to', x
 
 x = 50
 func()
 print 'value of x is', x

output:
$python fun_g.py
x is 50
changed global x to 2
value of x is 2

