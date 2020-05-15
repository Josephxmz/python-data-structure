# python-data-structure
北大陈斌数据结构

栈的应用：一维消消乐
开心消消乐我们都熟悉，我们可以用刚学过的栈来做一个“一维”的开心消消乐游戏，这个游戏输入一串字符，逐个消去相邻的相同字符对。
如果字符全部被消完，则输出不带引号的“None”  
from pythonds.basic.stack import Stack  

s = input()  
sta = Stack()  

for a in s:  
    if not sta.isEmpty() and a == sta.peek():  
        sta.pop()  
    else:  
        sta.push(a)  
if sta.isEmpty():  
    print("None")  
else:  
    list0 = list(range(sta.size()))  
    size = sta.size()  
    for i in range(size):  
        list0[size-i-1] = sta.pop()  
    
    print("".join(list0))  
