# Interpretation-Python-Notation
Notes for Python Notation

## Key Words
# del
>>> a = [-1, 3, 'aa', 85] # 定义一个list
>>> a
[-1, 3, 'aa', 85]
>>> del a[0] # 删除第0个元素
>>> a
[3, 'aa', 85]
>>> del a[2:4] # 删除从第2个元素开始，到第4个为止的元素。包括头不包括尾 = range(0,4)
>>> a
[3, 'aa']
>>> del a # 删除整个list

# global
 如果你想要为一个定义在函数外的变量赋值，那么你就得告诉Python这个变量名不是局部的，而是 全局 的。我们使用global语句完成这一功能。没有global语句，是不可能为定义在函数外的变量赋值的。
 你可以使用定义在函数外的变量的值（假设在函数内没有同名的变量）。然而，我并不鼓励你这样做，并且你应该尽量避免这样做，因为这使得程序的读者会不清楚这个变量是在哪里定义的。使用global语句可以清楚地表明变量是在外面的块定义的。
def func():
　　global x
　　print 'x is', x
　　x = 2
　　print 'Changed local x to', x

x = 50
func()
print 'Value of x is', x

输出:
$ python func_global.py
x is 50
Changed global x to 2
Value of x is 2

# with
 Python中的with可以改变代码的友好度
with open('a.txt') as f:
  print f.readlines()
  
class A():
  pass

with A() as a:
  print ' '

# assert
1、assert语句用来声明某个条件是真的
2、如果你非常确信某个你使用的列表中至少有一个元素，而你想要检验这一点，并且在它非真的时候引发一个错误，那么assert语句是应用在这种情形下的理想语句。
3、当assert语句失败的时候，会引发一AssertionError
Test：
>>> mylist = ['item']
>>> assert len(mylist) >= 1
>>> mylist.pop()
'item'
>>> assert len(mylist) >= 1
Traceback (most recent call last):
 File "<stdin>", line 1, in <module>
AssertionError


