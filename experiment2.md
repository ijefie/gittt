班级：21计科1班

学号：B20210302122

姓名：奉洋

github地址：https://github.com/ijefie/gittt.git

codewars地址：https://www.codewars.com/users/fyhfyhfyh


### 一、实验过程与结果
1. Python变量、简单数据类型和列表简介

变量和简单数据类型练习
```python
message="hello world python!"
print(message)
message="hello world c++"
print(message)
first_name="a"
last_name="b"
full_name=f"{first_name}{last_name}"
print(full_name)
name="tom"
print(name.title())
x,y,z=1,2,3
print(x,y,z)
```
2. Codewars Kata挑战
   
挑战一：你的任务是找到一个正整数n的最近的平方数 例如，如果n=111，那么nearest_sq(n)（nearestSq(n)）等于121，因为111比100（10的平方）更接近121（11的平方）。 如果n已经是完全平方（例如n=144，n=81，等等），你需要直接返回n。
```python
def nearest_sq(n):
    import math
    m = round(math.sqrt(n))
    return m * m
```

挑战二：一个孩子在一栋高楼的第N层玩球。这层楼离地面的高度h是已知的。他把球从窗口扔出去。球弹了起来, 例如:弹到其高度的三分之二（弹力为0.66）。他的母亲从离地面w米的窗户向外看,母亲会看到球在她的窗前经过多少次（包括球下落和反弹的时候）？

一个有效的实验必须满足三个条件：

参数 "h"（米）必须大于0

参数 "bounce "必须大于0且小于1

参数 “window "必须小于h。

如果以上三个条件都满足，返回一个正整数，否则返回-1。 注意:只有当反弹球的高度严格大于窗口参数时，才能看到球。
```python
def bouncing_ball(h, bounce, window):
    if not 0 < bounce < 1: return -1
    count =0
    while h > window:
        count += 1
        h *= bounce
        if h > window: 
            count += 1
    return count or -1
```

挑战三：返回给定字符串中元音的数量（计数）。对于这个Kata，我们将考虑a、e、i、o、u作为元音（但不包括y）。输入的字符串将只由小写字母和/或空格组成。
```python
def get_count(sentence):
    return sentence.count('a')+sentence.count('e')+sentence.count('i')+sentence.count('o')+sentence.count('u')
    pass
```

挑战四：创建一个函数接收一个整数作为参数，当整数为偶数时返回”Even”当整数位奇数时返回”Odd”。
```python
def even_or_odd(number):
    if number % 2==0:
        return 'Even'
    else:
        return 'Odd'
```

3. 使用Mermaid绘制程序流程图

挑战二
```mermaid
flowchart  LR
Start(开始) --> Scanf[用户输入h,bounce,window]
    Scanf --> |判断|If{h是否大于window且window是否大于0且bounce是否大于0小于1}
If --> |不成立|ou[返回-1]
If --> |成立|ji[count++]
    ou --> End(结束)
    ji --> |判断|if{h*=bounce>window}
if --> |成立|k[count++]
k --> |判断|if{h*=bounce>window}
if --> |不成立|h[返回count]
h --> End(结束)

```

### 二、实验考察
1. Python中的简单数据类型有那些？我们可以对这些数据类型做哪些操作？

        Python中的简单数据类型有整数，浮点数，布尔和复数类型。

        可进行的操作：数字运算，字符串，列表，元组，字典，集合
2. 为什么说Python中的变量都是标签？

       python中的变量不是容器，而是指向python对象的标签。因为对象位于解释器的命名空间中，但是任意数量的标签可以指向同一个对象，当对象发生变化时，所有指向它的变量的值都会改变。

3. 有哪些方法可以提高Python代码的可读性？

       格式化代码、使用有意义的变量名、合理使用注释、封装代码块、合理利用空白行和使用合适的缩进

### 三、实验总结
1. 通过此次实验，我较好地理解了python的变量和数据类型的操作方法。也初步利用python进行了编程，学到了许多python编程知识。最后还学会了用VScode画一些简单的流程图。
