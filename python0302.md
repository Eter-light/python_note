python

### 1.注释

(以IDE为pycharm为例)

**单行注释**：#+空格+文本（快捷键：crtl+/)

**多行注释**："""（三个双引号开始，结尾也是三个双引号）

​                 '''(三个单引号开始，三个单引号结尾)

### 2.格式化输出

（用于脚本中插入需要传入的变量,输出函数是print）

name="jiajia"

age=25

height=178.5

%s指代字符串型

%d指代整数型

%f指代浮点型 （这里的%.2f意思是保留两位小数）

输出格式为：print("he name is %s,%d岁,身高是%.2f"%(name,age,height))------>he name is jiajia,26岁,身高是178.50

也可以：print(f"hello,he is {name},he {age},he is {height} ")--->hello,he is jiajia,he 26,he is 178.5  ------注意这里的f哦

***f {}中括号格式化输出**如何设置精度：*

```
height=123.3
print(f"he is {height:.3f}")
print(f"he is {height:.2f}")
```

```python
print("my name is neinei\nnice to meet you")---->
my name is neinei
nice to meet you

print("you are a good audience",end="$_$")----->end指定分隔符为$_$
print("thank to you listening")

# 格式化输出并用0补全
print('%06d' % num) # 6位数 用0补全
print(f'{num1:06d}') # 6位  用0补全


```

### 3.输入

（从键盘中获取输入的函数，在python中使用的是input()函数）

***format***:input("提示输入的信息")---得到用户输入的内容，回车代表输入结束,得到的数据不管输入的内容是什么，均是字符串型

name=input("please insert your name:")   ---please insert your name:jiajia

print("你的名字是%s"%name)------你的名字是jiajia

***eg:***从键盘上输入苹果的价格，重量，输出：苹果单价9.00元/斤，购买了5.00斤。需要支付45.元

1. ```
   # 输入价格：
   price=input("请输入单价：")
   # 输入购买重量：
   weight=input("请输入重量：")
   # 计算共花费多少：
   result=float(price)*float(weight)----这一步为单位转换，因为input输入的默认是str
   # 输出需要支付的钱数
   print(f"苹果单价{price}元/斤，购买了{weight}斤。需要支付{result}元")
   
   请输入单价：9
   请输入重量：5
   苹果单价9元/斤，购买了5斤。需要支付45.0元
   
   ```

#### 4.类型转换

（将原始数据类型转换为我们需要的数据类型）

- float转换为int      f_num=3.14  num=int(f_num)   print(type(num))----->int

- 整数类型的字符串  s_num="10"  m_num=int(s_num)  print(type(s_num))---->int

  #### 5.条件控制语句

  ![1639218775850](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639218775850.png)

  ![1639219382073](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639219382073.png)

跟bash shell的区别

1.bash shell 是if 后的test命令返回状态码0，则执行then后面的语句

  python中是 if 后的条件为true时，执行。。。。。。。

2.python 条件控制语句的格式：（注意这里有个冒号）

![1638972893972](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1638972893972.png)

 在if语句的缩进内，属于if条件满足后，需要执行的代码

bash shell的格式：if  条件退出状态码为0

​                               then

​                                    需执行的代码块

​                                else

​                                     需执行的代码块2

​                                 fi     

eg：

![1638973866762](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1638973866762.png)

#### 5.if else 结构

![1638974147185](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1638974147185.png)

6.Debug模式

可以查看代码的执行过程

可以排查错误

**步骤：**

1.打断点（一般在代码的开始的地方打上断点，或者在查看问题代码的地方打断点）

2.右键debug运行代码

3.点击下一步，查看代码执行过程

![1638976612418](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1638976612418.png)

#### 6.if_elif_else 结构

**格式：**

​       if  判断条件1：

​             条件满足，执行的代码

​       elif 判断条件2：

​             (先）条件1不满足，条件2满足，执行的代码

​        else：

​             条件1 and 条件2都不满足，执行的代码

**eg:**

- [x] ```
  # 输入成绩
  grade = input("please input your name: ")
  # 将输入的字符串格式转化为整数型格式
  grade = eval(grade)
  
  # 进行成绩等级的判断
  if grade >= 90:
      print("等级为A")
  elif (grade >= 80) and grade < 90: -----(根据上面的格式可以知道，代码会先判断条件一是否不成立，所以没必要加上grade<90)
      print("等级为B")
  elif grade >= 70:
      print("等级为C")
  else:
      print("等级为D")
  
  
  
  
  ```

![img](file:///C:\Users\宝龟儿\AppData\Local\Temp\ksohtml\wps94A8.tmp.jpg)

![1639215078495](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639215078495.png)

```python

```

#### 7.if嵌套

**应用场景：****elif****：是同时判断多个条件，所有的条件是平级的

​                  ***嵌套if***：在之前条件满足的前提下，再增加额外的判断

**格式：**

![1639217537352](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639217537352.png)

eg:

```python
# 问卷调查
# an="是"
en = input("是否要进行评价：")
# 如果答案是“是”，则进入问卷调查页面
if en == '是': -----注意这里的字符串比较运算符是“==” 字符串需要用’‘单引号or"" 双引号括起来
    print("您将进入评价问卷")
    score = eval(input("请输入您的评分："))
    if score >= 9:
        print("谢谢您的肯定")
    elif score >= 7:
        print("我们会继续改进的")
    else:
        print("很遗憾给您带来不好的体验了")
else:
    print("打扰了")
```

#### 8.格式调整

```python
# 我出的拳（0：拳 1：布 2：剪刀）
me = int(input("我出的拳："))
# 电脑自己出的拳（这个需要取随机数）
comp = 1
print("我的拳%d VS 电脑的拳%d " % (me, comp))

# 电脑和我进行比较有三种情况 1，我胜 2.平局 3.我输
# 第一种结果 我出剪刀，电脑出布
# 第二种结果 我出布，电脑出石头
# 第三种结果 我出石头，电脑出剪刀
if (me == 2 and comp == 1) or (me == 1 and comp == 0) or (me == 0 and comp == 2):
    print("i win")
elif me == comp:
    print("we same")
else:
    print("computer win")
    
```

*由于多个逻辑运算符排一排，调整后：*

```python
# 我出的拳（0：拳 1：布 2：剪刀）
me = int(input("我出的拳："))
# 电脑自己出的拳（这个需要取随机数）
comp = 1
print("我的拳%d VS 电脑的拳%d " % (me, comp))

# 电脑和我进行比较有三种情况 1，我胜 2.平局 3.我输
# 第一种结果 我出剪刀，电脑出布
# 第二种结果 我出布，电脑出石头
# 第三种结果 我出石头，电脑出剪刀
if ((me == 2 and comp == 1) 
        or (me == 1 and comp == 0) 
        or (me == 0 and comp == 2)):
    
    print("i win")
elif me == comp:
    print("we same")
else:
    print("computer win")
```

![1639539855542](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639539855542.png)

#### 9.随机数处理

在python中，要使用随机数，先需要导入随机数的模块---工具包

import random

导入模块（工具包）后，可以在 **模块名称** 后面敲一个 . 然后按 tab 键，会提示该模块中包含的所有函数

![1639540601802](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639540601802.png)

格式：

random.randint(a,b)----返回[a,b]之间的整数，包含a b

random.randint(1,3)----生成随机数   3=>n >=1 1,2,3

random.randint(3,3)----结果永远是3

random.randint(3,1)----错误，上限必须大于下限

![1639540310557](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639540310557.png)

### 10.循环

让**特定的代码**重复执行

![1639558284374](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639558284374.png)

可以把while语句以及缩进部分看作一个完整的代码块

**eg：**

```
# 打印n 遍jiajia
n=int(input("输入需要打印的次数"))
#开始定义循环
# 计数器初始值
i=1
while i<=n:
    # 1.希望在循环中执行的代码
    print("jiajia")
    # 2.处理计数器
    i=i+1------>i += 1
        
```

#### 10.1.python中的计数方法

自然计数法（从1开始）

程序计数法（从0开始）---几乎所有的程序语言都选择从0开始计数

因此，大家在编写程序时，循环计数都从0开始

上面的代码改成计数从0开始时：

```
# 打印n 遍jiajia
n=int(input("输入需要打印的次数"))
#开始定义循环
# 计数器初始值
i=0
while i<n:      -----只有<= 变成了 <
    # 1.希望在循环中执行的代码
    print("jiajia")
    # 2.处理计数器
    i += 1
    
    
    
    
 
```

#### 10.2 循环计算

![1639561967597](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639561967597.png)

**eg：**

计算0-100之间，所有数的累计求和结果

```python
# 计算0-100之间所有数的累计求和结果
# 1.先定义一个变量计算循环的次数
i=1
# sum=1+2+3+4+5+6
# 定义一个存放最终结果的变量
sum=0
# 2.开始循环
while i<=100:
    # 1+0 1+2 1+2+3
    sum += i
    # 处理计数器
    i += 1
print("得出最终计算结果%d" % sum)

eg:
    计算0-100之间，所有偶数和
    i=0
    while i <= 100:
        print (i)
        i+=1
        ------------------先写一个基本框架（有计数变量 有循环 有计数更新）
        
   再进行进一步处理
# 计算0-100之间所有偶数的累计求和结果
# 1.先定义一个变量计算循环的次数
i=1
# sum=1+2+3+4+5+6
# 定义一个存放最终结果的变量
sum=0
# 2.开始循环
while  i <= 100:
    # 1+0 1+2 1+2+3
    if i%2==0:------因为发现i如果在条件里定义，则根本循环不下去，所以要在里面更新i的取值
        sum += i
    # 处理计数器
    i += 1
print("得出最终计算结果%d" % sum)


        
```

#### 10.3 break  and continue

break:是在某一条件满足时，**退出循环**，不再执行后续重复的代码

continue:某一条件满足时，不执行后续重复的代码（直接去执行条件判断的部分，不去执行continue后面的代码块）

​               注意这时要在continue前加针对计数器变量的更新

```python
while  i < 10:
    # 1+0 1+2 1+2+3
    if i==5:
        i += 1  ------当i=5时，先进行i的更新，在执行continue的操作
        continue
    print(i)
    # 处理计数器
    i += 1 ----这里的i += 1还是要保留的
    
    
  break 和 continue 只有在循环中才用


    
```

#### 10.4 循环嵌套

![1639803122038](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639803122038.png)

代码的缩进 表达了代码的所属关系



**tips**：

*字符串乘法*：

>>> ![1639806503308](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639806503308.png)

********

*tips:*

1.在默认情况下，print函数在输出内容之后，会自动在内容末尾增加换行

2.如果不希望末尾增加换行，可以在print函数输出内容的后面增加   ，end=""

3.其中""中间可以指定print函数输出内容之后，和下一个输出内容之间的分隔符

*eg：*

```python
print("i love",end="&&")
print("you")
```

------>i love&&you

```python
print("i love",end="")
print("you")
```

--------->i loveyou





*内部循环的例子：*

```python
# # 第一行 一颗星
# 第二行 两颗星
# 。。。。
# 第五行 五颗星
# 找到了每一行星星个数和行的关联
# 1.计数器的定义
row = 1

# 2.while 循环
while row <= 5:
# 3.while 代码块
    col=1
    while col <= row:
        print("*",end="")
        col += 1
    print("")----这行不可以省略，是为了在每一个内部循环结束时增加换行
# 4.计数器的更新
    row += 1
    
    
    
    
    eg：打印99乘法表
    
 # 打印九九乘法表

# 1.计数器的定义
row = 1

# 2.while 循环
while row <= 9:
# 3.while 代码块
    col=1
    while col <= row:
        print("%d * %d=%d" %(col,row,col*row),end=" ")------注意这里的格式化输出
        col += 1
    print("")
# 4.计数器的更新
    row += 1
  

  other:
    for i in range(1,10):
    for j in range(1,i+1):
        print("%d * %d = %d" %(j,i,i*j),end="\t")
    print("\n")
    
```

![1639886134334](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639886134334.png)

##### 10.4.1 转义字符

1.\t 在控制台输出一个制表符，协助在输出文本时垂直方向保持对齐

2.\n 在控制台输出一个换行符

制表符的功能是在不使用表格的情况下，在垂直方向按列对齐文本

eg:

![1639886503447](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639886503447.png)

这里将分隔符改成制表符，就不会有不对其的情况了

如果想在控制台输出 “ ‘ \ 都需要前面加\来转义



### 11.函数

**定义**：就是把具有独立功能的代码块 封装成一个小的模块，在需要的时候调用

**使用：**1.定义函数：封装独立的功能

​           2.调用函数：享受封装的成果

定义函数的格式：

def fun_name():

​    print("*"*5)

调用函数：

fun_name()

***tips：***pycharm的单步调试工具

F8(step over)可以单步执行代码，会把函数的调用过程看作是一行代码直接执行

F7(step into)可以单步执行代码，如果是函数，会进入函数内部

#### 11.1 函数的注释

1.函数的定义上方保留两个空行

![1639923822413](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639923822413.png)

eg:

```python
def multip():
    """打印九九乘法表"""---------------这里就是给这个函数增加注释
    # 打印九九乘法表

    # 1.计数器的定义
    row = 1

    # 2.while 循环
    while row <= 9:
    # 3.while 代码块
        col=1
        while col <= row:
            print("%d * %d = %d" %(col,row,col*row),end="\t")
            col += 1
        print("")
    # 4.计数器的更新
        row += 1
```

![1639924051824](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639924051824.png)

eg:计算两个数字的求和

```python
def sum_2_num():
    """计算两个数字的求和"""
    num1 = int(input("请输入数字1："))
    num2 = eval(input("请输入数字2："))
    sum1 = num1 + num2
    print("%d + %d = %d" % (num1, num2, sum1))

sum_2_num()




```

#### 11.2 函数参数的使用及其作用

![1639925551623](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639925551623.png)

**eg:**

```python
def sum_2_num(num1,num2):-----在定义时标注需要传入的参数名
    """计算两个数字的求和"""
    # num1 = int(input("请输入数字1："))
    # num2 = eval(input("请输入数字2："))
    sum1 = num1 + num2
    print("%d + %d = %d" % (num1, num2, sum1))

sum_2_num(2,3)----调用时，顺序对应上面，传入参数的具体值 2传入num1,3传给num2

```

**debug模式：**

![1639926103757](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1639926103757.png)



#### 11.3 形参和实参

形参：定义参数时传递的参数叫做形参 作用：在函数内部当作变量使用，可以计算

实参：调用函数时传递的参数叫做实参



#### 11.4 返回值

1，在程序开发中，有时候，会希望一个函数执行结束后，告诉调用者一个**结果**，以便调用者对具体的结果做后续的处理

2.**返回值**是程序完成工作后，最后给调用者的一个结果（返回值就是当你想将函数中的变量也可以在外面调用时）

3.在函数中使用**return关键字**可以返回结果（返回值也需要一个变量去接收）

4.调用函数的一方，可以**使用变量**来接收函数的返回结果

![1640094752061](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640094752061.png)

![1640095257386](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640095257386.png)

**eg:**

```python
def sum_2_num(num1,num2):
    """计算两个数字的求和"""
    # num1 = int(input("请输入数字1："))
    # num2 = eval(input("请输入数字2："))
    sum1 = num1 + num2
    return sum1    ----即表示返回，return后面编写的代码不会执行


result= sum_2_num(3,4) -----这里用result 变量来接受函数return的返回值
print(result)


```

**tips**：

1.return 关键字后边可以不写数据值，默认返回None

​    def dunc():

​          xxx

​          return   # 作用：返回none，并终止函数的运行

2.函数可以不写return，返回值默认是None

​       def func():

​             xxxx



#### 11.5 函数的嵌套调用



一个函数里面又调用了另一个函数，我们就叫它函数嵌套调用



函数的调用执行过程：

1.函数定义的地方是不执行的

2.调用函数时，会返回到函数的定义的位置，从上往下依次执行（函数定义里的代码）

3.函数执行后，返回到调用函数的地方继续往下执行

**模块：**

1.模块就好比是工具包，要想使用这个工具包中的工具，就需要导入（import）这个模块

2.每一个以扩展名py结尾的python源文件都是一个模块（工具包）

3.在模块中定义的全局变量，函数都是模块能够提供给外界直接使用的工具

****体验小结**：

1.可以在一个python文件中定义**变量或者函**数**

2.然后在另一个文件中使用**import****导入这个模块**

3.导入之后，就可以使用**模块名.变量**/**模块名.函数**的方式，使用这个模块中定义的变量或者函数

**模块可以让之前编写过的代码方便的被复用**

#### 11.6 全局变量 & 局部变量（根据变量作用域的不同）



**局部变量：**

![1640270221898](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640270221898.png)



![1640270454936](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640270454936.png![1640270730364](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640270730364.png)

**全局变量：**

![1640272396616](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640272396616.png)

内置方法：

1.my_str.join(可迭代对象)

fr:"mys-str".join("zifuchuan")-------以my_str作为join后面字符串的分隔符

eg:------>print("-*-".join("mylove"))------join后面的字符串

------->m-*-y-*-l-*-o-*-v-*-e

2.&3.



![1640877936381](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1640877936381.png)

### 12.列表

#### 12.1 列表的定义

列表：是python中的一种**数据类型**，可以存放多个数据，列表中的数据可以是**任意类型的**

​            列表list，定义使用[] 进行定义

**定义空列表：**

1:my_list = [ ]

print(my_list,type(my_list))

2:my_list1 = list( ) 

print(my_list2,type(my_list1))



**定义带数据的列表：**

my_list2 = [1,3.14,True,'isaac']

print(my_list,type(my_list2))

#求列表中数据元素的个数

len(my_list2)

#列表支持下标和切片操作

```python
print(my_list2[1])
```

```python
print(my_list2[1:4])
```

#下标操作和字符串中不同的是：字符串不能使用下标去修改其中的数据，但是列表可以使用下标去修改列表中的数据

```python
my_list2[0] = "jijia"
print(my_list2)

['jijia', 3.14, True, 'isaac']
```



#### 12.1 列表和字符串的遍历（可遍历的就是可迭代对象）

**1.字符串的遍历**

```python
for i in "chichao":
    print(i, end=' ')
```

输出结果：c h i c h a o 

**2.列表的遍历**

eg:

```python
my_list2 = [1,3.14,True,'isaac']
```

```python
for i in my_list2:
    print(i, end=' ')
```

输出结果：1 3.14 True isaac 

#### 12.3 向列表中添加数据：

```python
# 向列表中添加数据的方法，都是直接在原列表上进行添加，不会返回新列表
my_list = [1, 'aaa', True, 234]
# 列表.append(数据）向列表的尾部追加数据
my_list.append('jiajia')
print(my_list) ------[1, 'aaa', True, 234, 'jiajia']

# 列表.insert(下标，数据) 在指定的下标下插入数据，原位置数据会延后一个下标
my_list.insert(0, "guier")
print(my_list) ------['guier', 1, 'aaa', True, 234, 'jiajia']

# 列表.extend(可迭代对象) str 列表 ，会将可迭代对象中的数据逐个添加到原列表末尾
my_list.extend('pei') # 向列表中添加字符串
print(my_list)----['guier', 1, 'aaa', True, 234, 'jiajia', 'p', 'e', 'i']
# 注意 不能直接print(my_list.extend('pei'))
# 因为这样得到的是使用extend方法得到的返回值

my_list.extend([999, '感冒灵']) # 向列表中添加列表
print(my_list)------['guier', 1, 'aaa', True, 234, 'jiajia', 'p', 'e', 'i', 999, '感冒灵']
```

#### 

#### 12.4 列表查询操作

```python
my_str = 'hello'
print(my_str.index('l')) -----2

print(my_str.count('l'))-----2


my_list = [1, 'aaa', True, 234]
# index()方法是输入元素，查找元素所在的下标，找到返回元素的下标，没有找到，程序报错
# 列表中没有find方法，只有index（）方法
print(my_list.index(1)) -----0

print(my_list.index('aaa')) ----1
# print(my_list.index(100)) #报错，因为元素不存在

# count()方法统计元素出现的次数
my_list.count(1) ------1

print(int(True))-----返回1

# in/not in 判断是否存在，存在返回true,不存在返回false，一般和if结合使用
print('aaa' in my_list) -----返回true

print(345 not in my_list)----返回true
```

#### 12.5 删除元素操作	

```python
my_list = [1, 2, 3, 4, 6, 9]
# 删除列表中的元素操作
# 1.根据元素的值进行删除 my_list.remove(元素值)
my_list.remove(4)
print(my_list)

# 2.根据元素下标（索引）进行删除
# 2.1 pop(下标)默认删除最后一个数据，返回删除的内容
num = my_list.pop() # 删除最后一个数据 9
print(num)
print(my_list)

num = my_list.pop(2)
print(num)
print(my_list)

# 2.2 del 列表[]
del my_list[0]
print(my_list)

# del my_list[4] 删除不存在的下标，会报错
```

#### 12.6 列表排序和逆置

```python
# 想要对列表中的数据进行排序，前提是列表中数据类型是一样的
my_list = [1, 3, 5, 8, 4, 2]

# 列表.sort() 直接在原列表进行排序,默认是从小到大的升序
my_list.sort()
print(my_list) ---[1, 2, 3, 4, 5, 8]

my_list.sort(reverse=True)
print(my_list) ----[8, 5, 4, 3, 2, 1]


# 补充：sorted(列表) 排序，不会在原列表中进行排序，会得到一个新的列表
my_list1= sorted(my_list)
print(my_list1) ----[1, 2, 3, 4, 5, 8]

my_list2 = sorted(my_list, reverse=True)
print(my_list2)------[8, 5, 4, 3, 2, 1]

# 逆置
my_list3 = my_list[::-1]
print(my_list3) ---[1, 2, 3, 4, 5, 8]

# 在原列表进行逆置
my_list3.reverse()
print(my_list3)----[8, 5, 4, 3, 2, 1]



```

#### 12.7 列表的嵌套

```python
school = [['北大', '清华'], ['复旦', '交大', '上大'], ['长安大', '武大']]
print(school[1])  ---['复旦', '交大', '上大']
print(school[1][1]) ---交大
print(school[1][1][1]) ---大

print(school[2][1]) ----武大

# 遍历
for i in school:
    print(i)
    for j in i:
        print(j)
        
---- ['北大', '清华']
北大
清华
['复旦', '交大', '上大']
复旦
交大
上大
['长安大', '武大']
长安大
武大
        
```



#### 12.8 举例子 分配办公室

```python
import random  # 第一行都要把要使用的工具包导入

# 定义办公楼列表
built = [[], [], []]
# 定义老师列表
teachers = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h']
# 遍历老师列表，完成随机选择
for teacher in teachers:
    # 第一个老师随机分配办公室号
    num = random.randint(0, 2) # 产生的随机数，相当于办公司的下标，这里的2是在范围内的
    built[num].append(teacher)

print(built)

for i in built:
    # 打印每个办公司的人数，和老师姓名
    print('该办公司的人数：%d' % (len(i)))
    for t in i:
        print('老师的名字为：%s' % (t), end=' ')
    print()
```





### 13.元组

```python
# 元组和列表非常相似，都可以存放多个数据，可以存放不同数据类型的数据
# 不同点： 列表使用[]定义，元组使用()定义
# 列表中的数据可以修改，元组中的数据不能修改

my_list = [1, 2, 'aaa']  # 列表
my_tuple = (123, 3.14, 'bbb')  # 元 组

# 元组支持下标（索引）和切片操作
print(my_tuple[0]) ----123

# 定义空元组，没有意义，因为元组中的元素是无法修改的
my_tuple = ()
my_tuple = tuple()
print(type(my_tuple))----<class 'tuple'>

# 定义一个数据元素的元组，数据元素后边，必需有一个逗号
my_tuple3 = (1)
my_tuple2 = (1,)

print(type(my_tuple2))----<class 'tuple'>
print(type(my_tuple3))----<class 'int'>




```

### 14.字典

#### 14.1字典的创建

```python
# 字典dict定义使用{} 定义，是由键值对{key-value}
# 变量名 = {key1:value1,key2:value2,....} 一个key:value键值对是一个元素
# 字典的key可以是字符串类型和数字类型(int float),不能是列表
# value值可以是任何类型
# 1.定义空字典
my_dict = {}
my_dict = dict()

# 2.定义带数据的字典
my_dict2 = {'name': 'jiajia', 'age': 18, 123: 456, 'like': ['make', 'study']}

# 3.访问value值，在字典中没有 下标 的概念，使用 key 访问对应的 value 值
print(my_dict2['name']) ---jiajia
print(my_dict2['like'][1]) ---study

# 4.访问key值不存在的时候
print(my_dict2['zhu']) # 代码报错，因为key值不存在

# 字典的长度即为键值对的个数
print(len(my_dict2)) -----4


```

#### 14.2 get方法的使用

```python
# 1.字典.get(key) 如果key值不存在，不会报错，返回的none
print(my_dict2.get('age')) -----18
print(my_dict2.get('min')) -----none

# 2.字典.get(key,数据值)  如果key存在，返回key对应的value值；如果key值不存在，返回key后的数据值
print(my_dict.get('min', 'kan')) -----kan
print(my_dict2.get('name', 'rong')) -----jia'jia



```



#### 14.3 字典中数据的添加和修改



```python
# 字典中添加和修改数据，使用key值进行修改和添加
# 字典[key] = 数据值； 如果key值存在，就是修改，如果不存在，就是添加

my_dict = {'name': 'jiajia', 'age': 18, 123: 456, 'like': ['make', 'study']}
my_dict['age'] = 20  # key值已经存在，就是修改
my_dict['min'] = 'kan'  # key值不存在，是添加
print(my_dict)  ----{'name': 'jiajia', 'age': 20, 123: 456, 'like': ['make', 'study'], 'min': 'kan'}

# 注意 int 的 1 和 float 的 1.0 代表一个key
my_dict[1] = 'a'
print(my_dict) ------{'name': 'jiajia', 'age': 20, 123: 456, 'like': ['make', 'study'], 'min': 'kan', 1: 'a'}
my_dict[1.0] = 'b'
print(my_dict)-------{'name': 'jiajia', 'age': 20, 123: 456, 'like': ['make', 'study'], 'min': 'kan', 1: 'b'}
```



#### 14.4  字典数据的删除

```python
my_dict = {'name': 'jiajia', 'age': 18, 123: 456, 'like': ['make', 'study']}

# 根据key值删除数据 del 字典名[key]
del my_dict[123]
print(my_dict) ----{'name': 'jiajia', 'age': 18, 'like': ['make', 'study']}

# 字典.pop(key) 根据key值删除，返回值是删除的key对应的value值
print(my_dict.pop('age'))---18
print(my_dict) -----{'name': 'jiajia', 'like': ['make', 'study']}

# 字典.clear() 清空字典，删除所有的键值对,返回值是none
print(my_dict.clear()) -----None
print(my_dict) ----{}

# del 字典名 直接将这个字典删除，不能使用这个字典了
del my_dict
print(my_dict) ----报错，未被定义


```

#### 14.5 字典中遍历数据

```python
my_dict = {'name': 'jiajia', 'age': 18, 123: 456, 'like': ['make', 'study']}

# 1.for循环直接遍历字典，遍历的是字典的key值
for i in my_dict:
    print(i)
    print(i,my_dict[i])---
name
name jiajia
age
age 18
123
123 456
like
like ['make', 'study']

# 2.字典.keys()
print(my_dict.keys()) ----dict_keys(['name', 'age', 123, 'like'])
# 字典,keys()获取字典中所有的key值，得到的类型是dict_keys,该类型具有特点：
# 1 可以使用list()进行类型的转换，
# 2.可以使用for循环遍历
for key in my_dict.keys():
    print(key,my_dict[key])
    
--name jiajia
age 18
123 456
like ['make', 'study']
```

![1641223323446](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641223323446.png)

4.

```python
# 字典.items() 获取所有的键值对，类型是dict_items,key,value 组成元组类型
# 1.可以使用list()进行类型转换，即将其转换为列表类型
# 2.可以使用for循环进行遍历
my_dict = {'name': 'fufu', 'age': 18, 123: 888}
print(my_dict.items()) 

for item in my_dict.items():
    print(item[0], item[1])   # 因为遍历它，获得的元素是元组

print('*'* 50)

for k, v in my_dict.items(): # k是元组中的第一个数据，v是元组中的第二个元素
    print(k, v) 
    
-----------------------------------------------------------------------------------------    
dict_items([('name', 'fufu'), ('age', 18), (123, 888)])
name fufu
age 18
123 888
**************************************************
name fufu
age 18
123 888




```



### 15.enumerate()函数

```python
# enumerate将可迭代序列(列表，字符串，元组）中元素所在的下标和具体元素组合在一起，变成元组
my_tuple = (123,789,'aaa')
my_str = 'iloveyou'
my_dict = {'name': 'fufu', 'age': 18, 123: 888}

for j in enumerate(my_tuple):
    print(j)

for i in enumerate(my_str):
    print(i)

for s in enumerate(my_dict):
    print(s)
```

--------------------------------------------------------------------

(0, 123)
(1, 789)
(2, 'aaa')

(0, 'i')
(1, 'l')
(2, 'o')
(3, 'v')
(4, 'e')
(5, 'y')
(6, 'o')
(7, 'u')

enumerate（）取字典中的只有key

(0, 'name')
(1, 'age')
(2, 123)



### 16 公共方法

#### 16.1 运算符

![1641306371836](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641306371836.png)

1.+ 支持字符串，列表，元组进行操作，得到一个新的容器

2.* 整数 复制，支持**以上**

3.in /not in 判断存在或者不存在，支持字符串，列表，元组，字典进行操作， **注意**：如果是字典的话，判断的是key是否存在或不存在

#### 16.2  python内置函数

![1641309361112](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641309361112.png)



字母的比较：a > A   z > a

 ![1641309399601](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641309399601.png)



### 17.全局变量

```python
# 全局变量： 就是在函数外部定义的变量

# 定义全局变量
g_num = 100

# 1.能否在函数内部访问全局变量？
def fun1():
    print(g_num)

# 2.能否在函数内部修改全局变量的值？
def fun2():
    g_num = 200 # 这里不是修改全局变量的值，是定义一个局部变量，只是和全局变量的名字一样
    global g_num1
    g_num1 = 2 # 这里是将g_num1定义为全局变量 global关键字是将变量定义成全局变量
    g_num2 = 4

fun1()  #  返回100  函数内部可以直接访问全局全量的值
fun2()
fun1()   # 返回100 所以函数内部不能直接修改全量变量的值
print(g_num1)  # 返回2  所以函数内定义的全局变量函数外是可以用的
print(g_num2)  # 报错 is not defined 
```



### 18.函数

strip()函数

```python
f = "    aaa \n  "
b=f.strip()  # 这个去空格的函数也可以去\n
print(b)
```

#### 18.1 函数的返回值

函数想要返回一个数据值，给**调用的地方**，需要使用**关键字return**

return关键字的作用：* 将return后面的数据值进行返回 * 程序代码遇到return，会**结束运行**

注意点：return关键字必须写在函数中

```python
def add(a, b):
    c = a + b
    return c  # 想要将计算结果，返回到函数调用的地方
    print(f"返回计算结果{c}") #函数遇到return就结束了，不会执行return后面的代码

result = add(2, 3)
print(result)
```

#### 18.2 函数返回多个数据值



```python 
def func(a,b):
    c = a + b
    d = a - b
    # 需求：想要将c 和 d 都进行返回
    # 思考 ：容器可以保存多个数据值，那就可以将返回值放在容器中进行返回
    # return [c, d]
    # return (c, d) # 和return c,d一样
    # return {0:c, 1:d}   以上三种容器均可
    return c, d  # 默认是组成元组进行返回



result = func(5,2)
print(result)
print(f"求和为{result[0]},求差为{result[1]}")





```

#### 18.3 函数的嵌套

```python
# 打印一条指定长度的横线 
def fun1(n):
    print("-" * n)

# 打印n条指定长度的横线
def fun2(f, n):
    i = 1
    while i <= f:
        fun1(n)
        i += 1
# 调用传参 f,n 为形参  2，50为实参
fun2(2, 50)
```



#### 18.4 函数传参的三种方式·

```python
def fun1(a,b,c):
    print(f"a的值为{a}")
    print(f"b的值为{b}")
    print(f"c的值为{c}")
```

第一种传参方式：**位置传参**

```python
fun1(1,'a',3)  #位置传参，按照形参的位置顺序将实参的值传递给形参
```

第二种传参方式：**关键字传参**，指定**哪个实参**传到**哪个形参**

```python
fun1(a=1, b='a', c=3) #注意：关键字必须是函数的形参名
```

第三种传参方式：**混合传参**

```python
fun1(10, b="go", c=200) #注意：位置参数应该在关键字参数的前面 
                        #注意：同一个形参不可赋多个实参

error:
    
1.fun1(10,b="start",3) # SyntaxError: positional argument follows keyword argument
2.fun1(10,a=20,b='ss',c=6) #TypeError: fun1() got multiple values for argument 'a'
```



#### 18.5 缺省参数（就是一个有默认值的形参）

1.缺省参数属于形参，是在**函数定义**时，给**形参一个默认值**，这个形参就是缺省参数

2.注意点：**缺省参数要写在普通参数的后面**，写在第一个的话，就要将所有参数定义为缺省参数了

3.特点：在函数调用时，如果给缺省参数传递实参值，使用的是传递的实参值，如果没有传递，使用默认值

```python
def fun1(a,b,c=10):
    """   打印函数a,b,c  """
    print(f"a的值为{a}")
    print(f"b的值为{b}")
    print(f"c的值为{c}")

fun1(12,13)
----a的值为12
b的值为13
c的值为10


fun1(12,23,40)
----a的值为12
b的值为23
c的值为40

# def fun1(a,b=20,c):
#     """   打印函数a,b,c  """
#     print(f"a的值为{a}")
#     print(f"b的值为{b}")
#     print(f"c的值为{c}")

报错：SyntaxError: non-default argument follows default argument
```



#### 18.6 不定长参数

1.在普通形参前边加上一个*，该形参变成**不定长元组形参**，可以**接收所有的位置实参**，变量类型为**元组**

2.在普通形参前前加两个*，该形参变成**不定长字典形参**，可以**接收所有的关键字实参**，变量类型是**字典**

这种方式可实现**一个形参**，**接收多个实参值**，**构成一个字典或元组**

```python
def fun1(*args, **kwargs):
    print(args)
    print(kwargs)


fun1(2, 3, 5, name='fu fu', age=19)
```

**tips:**

这里的args & kwargs 都是普通形参变量，只是加了*，使他们具有接收多个实参的能力，可以用任何变量名，习惯定义这两个变量名为此

**eg:**

![1641630828138](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641630828138.png)

#### 18.7 函数形参的完整格式

即：当定义一个函数，要**包含所有的形参类型**时，他们的位置应该如何放置

```python
# 已知缺省参数要放在普通参数的后面，那不定长元组（会接受所有的位置参数）应该如何放
def fun_full1(a,b=1,*args):
    print(a)
    print(b)
    print(args)


fun_full1(1, 'aa', 6, 8)
```

结果为：

1
aa  将aa 传递给了缺省参数
(6, 8)

**but：**如果我并没有想传参给b，而是想让他直接保留默认值的，无法实现了

**so**:

```python
def fun_full2(a, *args, b=1):  # 普通参数 不定长元组参数 缺省参数
    print(a)
    print(b)
    print(args)


fun_full2(1, 2, 'aa', 'fu fu')
```

结果为：

1----a
1-----b

(2, 'aa', 'fu fu')

**but:**这样，位置参数都被不定长元组参数劫走了，缺省参数只能取到默认值

**right：** 传参时，**缺省参数如果传值，需要使用关键字形参**

**正确的格式顺序**

```python
def fun_full3(a, *args, b=1, **kwargs):  # 普通参数 不定长元组参数 缺省参数 不定长字典参数
    print("a:", a)
    print("args:", args)
    print("b:", b)
    print("kwargs:", kwargs)


fun_full3(1, 2, 4, 5, k=123, g='age', b=8) # 这里b虽然位置放在最后，也是可以传过去的
```

结果为：

a: 1
args: (2, 4, 5)
b: 8
kwargs: {'k': 123, 'g': 'age'}



print函数：

```python
def print(self, *args, sep=' ', end='\n', file=None): # known special case of print
    """
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
    """

```



sep是你输入多个值时的分隔符：

```python
print(1, 2, sep=' ', end='\t')
print("i love you")
#结果为：
1 2	i love you
#因为print函数种有不定长元组参数的定义，所有sep，end等参数的传递，在调用print函数时，需要使用关键字传参


```

### 19.拆包 & 组包

```python
# 组包，一个变量接收多个值，默认组成元组
a = 1, 2, 4
print(a)

def fun1():
    return 1, 2, 3


result = fun1()
print(result, type(result))
```

```python
# 拆包： 用多个变量去接收一个容器中的值
# 数据的个数 需要和 变量的个数 保持一致

b, c, d = a
print(b, c, d)

# 列表的拆包
my_list = [1, 'aa', True]
num, d, boo = my_list
print(num) # 1
print(d)   # 'aa'
print(boo) # True

# 字典的拆包
my_dict={'age': 17, 'name': 'fufu', 123: 567 }
jia, min, kan = my_dict
print(jia)    # 'age'  接收的是key值
print(min)    # 'name'
print(kan)    # 123


```

**tips:**  当值的个数与变量的个数不一致时会报的错

```
c, d = a 报错：ValueError: too many values to unpack (expected 2)
```

```
c, d, r, z = a 报错：ValueError: not enough values to unpack (expected 4, got 3)


```

**eg1:**

```python
def fun1():
    return 1, 2, 3  # 默认返回一个元组

result2, result3, result4= fun1() # 用多个变量去接收元组种的值(拆包)
print(result2)
print(result3)
```

**eg2:**

```python
# 交换两个变量的值
a=10
b=20

a, b = b, a  # 1.(b,a)组包为(20,10)
print(a,b)   # 2.a,b 去接收元组(b,a)的值
```

### 20.引用

1.**变量**和**数据**是分开存储的

2.数据是保存在内存中的一个位置

3.变量中记录着**数据在内存中的地址**

4.变量记录数据在内存中地址的这个动作就叫**引用**

5.使用id（）函数可以查看变量中保存**数据所在的内存地址**

6.如果对变量赋新的值，其实就是**修改了数据的引用**（记录其他数据在内存中的位置）（相当于书签）

7.变量改为对新赋值的数据引用



函数的**实参/返回值**都是靠**引用**来传递数据的，（形参会去**记录实参在内存中的数据地址**）

**eg:**

```python
def test(num):
    print("在函数内部%d 对应的内存地址是%d" %(num, id(num)))


# 定义一个数字的变量
a = 10

# 数据地址的本质就是一个数字
print("a变量保存数据的内存地址为%d" %(id(a)))

# 调用test函数，本质上传递的是实参保存的数据的引用，而不是传递的值
test(a)
```

**eg:**

![1641700524435](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641700524435.png)

![1641703234476](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1641703234476.png)

在交互终端中，小整数（-5-255）使用相同的引用地址，否则，开辟新的内存地址



#### 20.1.可变类型 & 不可变类型

1.类型的可变与不可变：在**不改变变量引用**的前提下(**不重新赋值** 变量名= xxx)，能否改变变量中的数据

2.如果能改变的是可变类型，如果不能改变，是不可变类型

3.**不可变类型***：int  float bool str list tuple dict

4.**可变类型**：list dict

**eg:**

```python
my_list = [1,2,'aa']
print(id(my_list)) ----2753848605120

my_list.append('jiajia')
print(id(my_list))-----2753848605120




```

因为变量的引用已经确定了（内存地址已经确定了）所以是可以换里面的元素值的



### 21 递归函数

定义：函数自己嵌套调用自己

![1642222305989](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1642222305989.png)

![1642223234606](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1642223234606.png)

**递归函数**的形成条件：



1.函数自己调用自己

2.函数必须有一个终止条件（总有一次调用能取到值）

3.n 和 n-1 有关系

4.注意一定要有返回值

**缺点：**

大量占用内存

eg：

```python
def multi(num):
    '''计算num的阶乘i:1*2*3*4...num'''
    if num == 1:
        return 1  # 这里即为递归最重要的终止条件
    i=num * multi(num-1)
    return i  # 这里不能用print因为返回值默认为none，调用的地方是取不到值的

print(multi(4))


```



### 22.匿名函数

**定义**：使用lambda关键字定义的函数就是匿名函数

**格式：**lambda 参数列表 ：表达式

**特点**：

1.匿名函数中不能使用**if语句. while循环.for循环**，只能编写**单行表达式**，或函数调用，普通函数都可以

2.匿名函数中返回结果**不需要使用return**，**表达式的运行结果**就是返回结果，普通函数返回结果必须使用return

**和普通函数做对比：**

```python
# 无参数无返回值
def fun1():
    函数代码

lambda:函数代码

# 无参数有返回值
def fun2():
    return 1+2

lambda: 1+2

# 有参数无返回值
def fun3(num):
    print(num)

lambda num:print(num)

# 有参数有返回值
def fun4(a,b):
    return (a+b)

lambda a,b :a+b
```

**应用**

```python
# 将匿名函数作为实参传入函数
def my_calc(a,b,func): # 这里的·func代表传入的形参值是一个函数
    print('**********************')
    num=func(a,b)  # 这里相当于是函数的嵌套
    print(num)

# 当传入的函数是普通参数
def fun_usu(a,b):   # 定义传入的函数
    return(a-b)

my_calc(1,2,fun_usu)

# 当传入的函数是匿名函数
my_calc(1,2,lambda a,b:a+b) # 无需定义，直接在实参中应用
my_calc(1,2,lambda a,b:b-a)



```

**图示解析：**

![1642303880743](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1642303880743.png)

**列表排序：**

![1642327202805](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1642327202805.png)

> ```
> iterable.sort（key=None, reverse=False）   #python 3.x
> 
> key：key指定一个接收一个参数的函数（用来指定根据列表中每个元素的什么进行排序，返回值即为排序的根据），这个函数用于从 每个元素 中提取一个用于比较的关键字。默认值为None。
> ```

**eg:**

```python
#  列表排序 列表中数据的类型要保持一致
my_list = [1,8,9,2,3]
my_list.sort() # 返回值为none
print(my_list) # 结果：[1, 2, 3, 8, 9] 列表有自己的sort方法，其对列表进行原址排序

# 当列表中的元素不是数字时，需要sort函数中key值来指定根据元素中的什么进行排序
my_list = ['ab','c','h','g','Z']
my_list.sort()
print(my_list)  # ['Z', 'ab', 'c', 'g', 'h'] 根据ASICC码进行从小到大排序(默认)
# my_list.sort(key=lambda x: len(x))
my_list.sort(key=len)
print(my_list) # ['Z', 'c', 'g', 'h', 'ab'] 根据列表元素长度进行排序

# 当元素为字典时如何排序
my_list = [{'name':'aa','age':17},{'name':'bb','age':10},{'name':'Z','age':7},{'name':'H','age':56}]
def paidui(n):  # 这里的n默认就是指列表中的元素
    return n['age']

my_list.sort(key=paidui)
print(my_list)

# 使用匿名函数简化步骤
# sort(key=lambda 形参 : (排序规则1，排序规则2.。。。)
# 当第一个规则相同时，会按照第二个规则排序
my_list.sort(key=lambda x : (x['age'],x['name']))
print(my_list) # [{'name': 'Z', 'age': 7}, {'name': 'bb', 'age': 10}, {'name': 'aa', 'age': 17}, {'name': 'H', 'age': 56}]

```

### 23.列表推导式

```python
# 列表推导式， 为了快速的生成一个列表
# 1.变量 = [生成列表元素的格式 for 临时变量 in xxx]
# 每循环一次，就会创建一个列表中元素
my_list = [i for i in range(5)]
print(my_list)
my_list = ['hello' for i in range(5)]
print(my_list)
# my_list = ['num:%d' %(i) for i in range(5)]
my_list = [f"num:{i}" for i in range(5)]
print(my_list)

# 2.变量 = [生成列表元素的格式 for 临时变量 in xxx if xxx]
# 表示元素个数符合for中的i的个数，还要复合if后条件的过滤
# 每循环一次，并且if条件为True，生成一个数据
my_list = [i for i in range(5) if i % 2 == 0]
print(my_list)  # [0, 2, 4]
my_list = ['hello' for i in range(5) if i % 2 == 0]
print(my_list)  # ['hello', 'hello', 'hello']

# 3.变量 = [生成列表元素的格式 for 临时变量 in xxx for j in xxx ]
# 第二个for循环，每循环一次，生成一个数据
my_list4 = [(i,j) for i in range(3) for j in range(3)]
print(my_list4) # [(0, 0), (0, 1), (0, 2), (1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
```



```python
# 字典推导式
# 变量 = {key:value for i in range(3)}
my_dict = {f'num[{i}]':i for i in range(3)}
print(my_dict) # {'num[0]': 0, 'num[1]': 1, 'num[2]': 2}

my_dict = {f'num[{i}]': j for i in range(3) for j in range(3)}
print(my_dict) # {'num[0]': 2, 'num[1]': 2, 'num[2]': 2} 因为当key相同时，相当于修改值

my_dict = {f'num{i}{j}':j for i in range(3) for j in range(3)}
print(my_dict) #{'num00': 0, 'num01': 1, 'num02': 2, 'num10': 0, 'num11': 1, 'num12': 2, 'num20': 0, 'num21': 1, 'num22': 2}
```



### 24.集合

1.集合： 用**set**来定义，使用{}，{数据1,数据2}

2.集合中的数据必须是不可变类型

3.my_set = {1, 3.14, True, 'hello', (1,2)}    type(my_set)  ----->set

4.集合是可变类型，支持的函数有：

```python
my_set = {1, 3.14, True, 'hello', (1,2)}
print(type(my_set))

my_set.add('age')
print(my_set)  # {1, (1, 2), 3.14, 'age', 'hello'}
my_set.remove(3.14)
print(my_set)  # {1, (1, 2), 'age', 'hello'}
my_set.pop()
print(my_set)  # 随机删除 {1, (1, 2), 'age'}
# 从上面几个结果可知，集合是无序的，(数据的定义顺序和输出顺序不是一致的),且不支持下标操作
# my_set = {1, 3.14, True, 'hello', (1,2)，1} # 集合中的数据没有重复数据
print(my_set)  # 报错：SyntaxError: invalid character in identifier
# 集合 列表 元组 三者间可以互相转换
my_list=[1,2,5,8,9,2]
print(set(my_list)) # {1, 2, 5, 8, 9} 转化成集合会过滤掉重复数据
```

### 25.文件

#### 25.1 打开文件

```python
# 1.打开文件，是文件从硬盘中存到内存中

 open(file,mode='r', encoding)
#file要操作的文件名字，r(read)只读模式打开，w(write)只写模式打开 a(append)追加打开
# encoding  文件的编码格式，常见的编码格式有两种，一种是gbk，一种是utf-8
# open()返回值是文件对象，后续所有的文件操作，都需要通过这个文件对象进行


Eg1：
# 以只读的方式打开当前目录中的1.txt文件，文件不存在会报错
f = open('D:\\pycharm\\pyproject\\venv\\cp02.py','r',encoding='utf-8')
# 2.读文件 文件对象.read()
buf = f.read()
print(buf)
# 3.关闭文件 fr:文件.close() 将内存中三大文件同步到硬盘
f.close()

Eg2：
# 以w方式打开文件，文件不存在，会创建文件，文件存在，会覆盖清空原文件
f = open('a.txt','w')
# 写文件，文件对象.write('写入文件内容')
f.write("iloveyou"
# 关闭文件
f.close()



```

![1642556443675](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1642556443675.png)

```python
# 以 a（append） 方式打开文件，追加内容，在文件的末尾写入内容
# 文件不存在，会创建文件
# 注意点：不管是a方式打开文件，还是w方式打开文件，写内容，都是使用write()函数
f = open('a.txt','a',encoding='utf-8')
f.write('eat\n')
f.write('cry\n')
f.close()

f = open('a.txt','a',encoding='utf-8')
f.write('hello\n')
f.write('world贾贾')
f.close()
```



#### 25.2 模拟读取大文件

**1.针对多行大文件**

```python
f = open('a.txt','r',encoding='utf-8')
while True:
    buf = f.readline()
    if buf:    # if len(buf) >0 容器（str）可以直接作为判断条件，容器中有内容，为True，没有数据为false
        print(buf,end='')
    else:
        # 文件读完了
        break
f.close()
```

**2.针对横向大文件**

```python
f = open('a.txt','r',encoding='utf-8')
while True:
    buf = f.read(5)
    if buf:    # if len(buf) >0 容器（str）可以直接作为判断条件，容器中有内容，为True，没有数据为false
        print(buf,end=' ')
    else:
        # 文件读完了
        break
f.close()
```

#### 25.3 文件的应用

##### 25.3.1 文件备份

```python
file_name=input('请输入要备份的文件名')
# 1.用只读的方式打开文件
f = open(file_name,'r')
# 2.用buf接收文件内容
buf = f.read()
# 3.关闭文件
f.close()

# 根据原文件名，找到文件后缀和文件名
index = file_name.rfind('.')
if index != -1:
    new_file_name = file_name[:index] + '_new' + file_name[index:]
print(new_file_name)
# 以只写的模式，打开一个不存在的新文件
f1 = open(new_file_name,'w')
# 把老文件的内容写入新文件
f1.write(buf)
#关闭文件
f1.close()
```

#### 25.4 文件和文件夹的操作

```python
# 对文件和目录的操作，需要导入os模块
import os

# 1.文件重命名 os.rename(原文件路径名，新文件路径名)
# os.rename('a.txt','b.txt')

# 删除文件 os.remove(文件路径名)
# os.remove('a.txt')

#3 .创建目录 os.mkdir(目录路径名) make directory
# 4.获取当前所在目录 os.getcwd() get current working directory
print(os.getcwd())   # D:\pycharm\pyproject\venv
# os.mkdir('test')
# 5.切换到其他目录
os.chdir('test')
print(os.getcwd()) # D:\pycharm\pyproject\venv\test

# 6.删除空目录 os.rmdir remove directory
# os.rmdir('test') # [WinError 2] 系统找不到指定的文件。: 'test'
# 7.修改当前路径到上一层目录
os.chdir('../')
print(os.getcwd())   # D:\pycharm\pyproject\venv
os.rmdir('test') # 在那个目录下是不能删除此目录的，要退到上一层目录



# eg：批量创建文件
def create_file():
    for i in range(5):
        new_file_name= 'py_'+ str(i)+'.txt'
        f=open(new_file_name,'w')
        # f.write()  # 这一步不对，open的时候就已经创建文件了，write()函数一定需要加参数
        f.close()
        print(new_file_name)

create_file()

# eg:批量修改文件名




```

![1643036885591](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1643036885591.png)

**文本文件**：.txt .py .md 扩展名  能够使用记事本打开的

**二进制文件**：具有特殊格式的文件， mp3 mp4 rmvb avi png jpg等

文本文件可以使用文本方式打开，也可以使用二进制的方式打开

二进制文件只能使用二进制的方式打开

二进制打开方式如下：不管读取，还是书写，都需要使用二进制的方式

rb wb ab

注意点：不能指定encoding参数  

### 26.对象 & 类

**类的组成**

1.类的名称

2.类的属性

3.类的方法：**行为/****功能**/函数

具有相同（或者相似）**属性**和**行为**的对象都可以抽象出一个类

#### 26.1 类的定义

包含：类名  属性  方法

在python中，**定义类**使用**关键字class**，语法如下：

class  类名(object):

​    pass

**注意：**

1.object为所有类的**基类**，即最原始的类

2.类名：遵循**大驼峰的命名规范**

3.注意在类的定义前后**空两行**

```python
# 定义方式一
class Dog(object):
    pass


#定义方式二
class Dog1():
    pass


# 定义方式3
class Dog2:
    pass


# 新式类：直接或间接继承object的类，在python3中，所有的类默认继承object类，即python3中所有的类都是新式类
# 旧式类： python2中只有后面加了（object）的显性继承类式新式类，其他的不加（object）的方式都默认不会继承object
          # 已经过时，不推荐使用
```



#### 26.2 创建对象

在代码中，对象式由类具体化的**实例**

```python
# 定义类
class Dog(object):
    # 在类中定义的函数，称为方法，函数的所有知识都可以使用(函数的调用，定义，注释。。。。）
    def play(self):
        print("小狗快乐的生活中")


# 创建对象 fr: 对象名 = 类名()
dog = Dog()
print(id(dog))

dog1 = Dog()
print(id(dog1))

# 可以使用对象调用类中的方法 对象.方法名(即类中定义的函数名)
dog.play() # 可以传参   小狗快乐的生活中

# python中类的应用 这里的my_list是一个对象，变量，列表
```

![1644246247045](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1644246247045.png)

#### 26.3 对象的属性



##### 26.3.1 类外部添加和获取属性

```python
# 定义一个类 类名为Dog()驼峰命名法则
class Dog(object):
    def play(self):
        print('小狗快乐的拆家中')

# 创建对象
dog = Dog()

# 调用类中的方法 ---对象.方法（）
dog.play()

# （类外）给对象添加属性 对象.属性名 = 属性值
dog.name= '大黄' # 给dog对象添加属性，属性值为‘大黄’

#获取对象的属性值 对象.属性值.print
print(dog.name)

# 修改属性值 和添加一样，存在就是修改，不存在就是添加
dog.name = '大白'
print(dog.name)
dog1 =Dog()
dog1.name='花花'
print(dog1.name)

# 每个对象，会保存自己的属性值，不同对象的属性值之间没有关联
```



##### 26.3.2 类内部利用self获取属性值

```python
class Dog(object):
    # self 作为类中方法的第一个形参，在通过对象调用方法的时候，不需要手动的传递实参值
    # python解释器自动将调用该方法的对象传递给self，所以self这个形参代表的是对象
    def play(self):
        print(f'self的id:{id(self)}')
        print(f"小狗{self.name}在快乐的拆家中")


# 创建对象
dog =Dog()
dog.name = '大黄'
dog.play() #self的id:2660173906992  #小狗大黄在快乐的拆家中
print(f'dog的id：{id(dog)}') #dog的id：2660173906992
```



#### 26.4 魔法函数

##### 26.4.1 __init__函数

```python
# __init__()
# 1.调用时机：在创建对象之后，会立即调用
# 2.应用场景：用来给对象添加属性，给对象属性一个初始值(构造函数)
#           代码的业务需求，每创建一个对象，都需要执行的代码可以写在‘__init__’中
# 3.注意点：如果‘__init__方法中，有除了self之外的形参，那么在创建对象时，需要给除self以外的其他形参传递实参值’ 即 '类名(实参值)'

class Dog(object):
    def __init__(self, na):
        print('*'*30)
        self.name = na  # 这里是给对象初始化的属性值 对象.属性 = 属性值

# 创建对象的第一种方式
Dog('大黄')         # ****************************** 创建即调用——init--方法
# 创建对象的第二种方式
dog1 =Dog('大白')   #****************************** 注意创建时需要传入实参值

print(dog1.name)  # 大白  给对象初始的属性值
```

##### 26.4.2 __str__函数

```python
# __str__
class Dog():
    def __str__(self):
        return "f小狗的名字为{self.name}"
    # python中调用print()打印实例化对象时会调用__str__()如果__str__()中有返回值，就会打印其中的返回值。
dog = Dog()
print(dog)  # <__main__.Dog object at 0x0000018A0DA68430>  打印一个实例化对象时，打印的其实时一个对象的地址。
            # 而通过__str__()函数就可以帮助我们打印对象中具体的属性值，或者你想得到的东西。
print(id(dog)) #1692446131248
```

**调用时机**

1.print(对象) ，会自动调用'__str__'方法，打印输出的结果是’__str__'方法的返回值

2.str(对象)，进行类型转换，将**自定义对象转换为字符串**的时候，会自动调用__str__函数(方法)

**应用**

1.打印对象的时候，输出一些**属性信息**

2.需要**将对象转换为字符串类型**的时候

**注意点**：

str方法必须返回一个字符串，只有self一个参数

```python
# __str__
class Dog():
    def __init__(self,name,age):
        self.name= name
        self.age = age
    def __str__(self):
        print('我是str函数，我被调用了')
        return f"小狗的名字为{self.name}"
    # python中调用print()打印实例化对象时会调用__str__()如果__str__()中有返回值，就会打印其中的返回值。

dog = Dog('大黄',2)   #因为上面定义init函数时，有除self以外的其他形参，所以在创建对象的时候需要传入实参值
str(dog)         # ’我是str函数，我被调用了‘  说明str(对象名）的时候就会调用__str__()方法 
# print(dog)   # 小狗的名字为大黄    通过__str__()函数可以帮助我们打印对象中具体的属性值，或者你想得到的东西。
# 这里会再打印一遍’我是str函数，我被调用了‘ 因为print(对象)会调用——str——()方法，并打印返回值
print(id(dog)) #1985408173104
```



***tips***：

字符串.join(列表)

将字符串添加到列表中的每一个元素之间，组成新的字符串

```python
my_list = ['i','love','you']
print('.'.join(my_list))
#i.love.you
```

***tips2***: **查看对象的引用计数**

```python
import sys # 查看当前对象的引用计数，需要提前导入的类
class Dog(object):
    # self 作为类中方法的第一个形参，在通过对象调用方法的时候，不需要手动的传递实参值
    # python解释器自动将调用该方法的对象传递给self，所以self这个形参代表的是对象
    def play(self,name):
        print(f'self的id:{id(self)}')
        self.name=name


# 创建对象
dog =Dog()
print(sys.getrefcount(dog)) # 2 实际为1，是因为getrefcount会再次引用，打印结束即销毁此次引用
dog1 =dog
print(sys.getrefcount(dog)) # 3

print(sys.getrefcount(dog1)) # 3
print(id(dog))
print(id(dog1)) # 是因为id打印的是对象的内存地址，这两个变量dog1 and dog都是使用的同一个内存地址（传递引用）
```





eg:

![1644409886642](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1644409886642.png)

```python
# 定义一个烤地瓜类
class Potato(object):
    def __init__(self):
        '''创建对象的时候即调用'''
        self.status = '生的'
        self.total_time =0
    def cook(self,time):
        '''动作方法，调用： 对象.方法名(实参值)'''
        # 随烧烤时间的增加，状态开始发生变化
        self.total_time += time
        if self.total_time <3:
            self.status = '生的'
        elif self.total_time<6:
            self.status = '半生不熟'
        elif self.total_time<8:
            self.status = '熟了'
        else:
            self.status ='糊了'
    def __str__(self):
        '''在print(对象)的时候会调用，并会输出return后面的值'''
        #输出地瓜的状态和烧烤总时间
        return f"经过{self.total_time},地瓜已经{self.status}"


potato =Potato()
potato.cook(10)
print(potato)  #经过10,地瓜已经糊了
```

##### 26.4.3 __repr__函数

**调用时机**：将对象存入容器，直接打印容器的时候

```python
class Dog(object):
    def __init__(self,name):
        self.name =name
    def __str__(self):
        return (f"{self.name}是狗狗的名字")
    def __repr__(self):
        '''这个函数和__str__差不多的用法，区别在于一般用于打印整个容器时会调用它'''
        '''默认返回的格式“类名+object at+内存地址”，下面的内容是用来重写这个函数'''
        return (f"{self.name}狗名")

dog=Dog('花花')
print(dog)  #花花是狗狗的名字  打印的是str函数的返回值

my_list =['i','love','you']
print(my_list)  #['i', 'love', 'you']
print('*'*50)
my_list = [Dog('TOM'),Dog('john'),Dog('jerry')]
print(my_list) #[TOM狗名, john狗名, jerry狗名]  将自定义对象放在容器中，打印容器时会调用__repr__函数，并打印其返回值，
#[<__main__.Dog object at 0x0000013366B58430>, <__main__.Dog object at 0x0000013366C897C0>, <__main__.Dog object at 0x0000013366C89E50>]
# 如果列表中的元素，是以字定义的类来创建的变量，是无法打印具体元素值的，打印出的是内存地址
# 如果想要打印出来容器中自定义对象具体元素值，需要在自定以的类中加上一个__repr__函数
```



![1644415873190](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1644415873190.png)

#### 26.5 继承

**重要概念：**

**1.单继承**：如果一个类只有一个父类，把这种继承关系称为单继承

**2.多继承：**如果一个类有多个父类，把这种继承关系称为多继承

***3.多层继承***：c继承b，b继承a



eg1：

```python
# 1.定义一个动物类
class Animal(object):
    def __init__(self,type,color):
        self.type = type
        self.color = color
    def play(self):
        print(f"{self.type}是{self.color}")


#2.定义一个宠物类
class Pet(Animal):
    def cry(self):
        print("呜呜叫")

#3.定义一个狗类
class Dog(Pet):
    pass

# 多层继承中，子类可以使用所有继承链中的类中的方法和属性
# 实质相当于在子类中重新定义了父类或者爷爷类的属性和方法，只是省去了步骤
dog = Dog('dog','white')
print(dog.type)   # dog 继承了爷爷的属性
dog.play()        # dog是white 继承了爷爷的方法
dog.cry()         # 继承了爸爸的方法
```



**子类重写父类的同名方法**

1.**概念**：子类定义和父类名字相同的方法

2**.为什么重写**：父类中的方法，不能满足子类对象的需求，所以要重写

3.**重写之后的特点**：子类对象调用子类自己的方法，不再调用父类的方法，父类对象调用父类自己的方法



**子类调用父类中的方法：**

```python
# 1.定义一个动物类
class Animal(object):
    def __init__(self,type,color):
        self.type = type
        self.color = color
    def play(self):
        print(f"{self.type}是{self.color}")


#3.定义一个狗类
# 子类中调用父类的方法
class Dog(Animal):
    def recode(self):
        print("记录宠物的状态和颜色",end=',')
        #子类中调用父类的方法
        # 第一种方法  父类名.方法(self，参数） 
        # 这里务必要传入形参，因为只有对象调
        Animal.play(self)
        # 第二种方法  super().play()
        super().play()

dog =Dog('狗','白的')
dog.recode() # 记录宠物的状态和颜色,狗是白的
```

**子类调用父类中的init方法，添加父类中的属性：**

```python
# 继承中的init方法
# 定义Dog类
class Dog(object):
    def __init__(self,name):
        # 添加属性
        self.age = 0
        self.name = name
    def __str__(self):
        return f"名字为{self.name},年龄为{self.age}"

# 2.定义XTQ类继承Dog类
class XTQ(Dog):
    #如果子类重写了父类的init方法，想继承添加父类中init中的属性，需要下面操作
    # 注意传参的时候，一般是先写父类的形参，再写自己添加的形参
    def __init__(self,name,color):
        # 子类重写了父类的init方法，默认不再调用父类的init方法，
        # 如果想调用父类的init方法，需要在子类的init方法中手动添加调用
        super().__init__(name)
        self.color = color

# 创建哮天犬对象
xtq = XTQ('大黄','yellow') # 创建对象时，需要传入init方法的形参值
print(xtq) # 名字为大黄,年龄为0  print(对象)会默认打印str函数的返回值
```



##### 26.5.1 多继承

**基本eg：**

```python
# 定义一个狗类
class Dog(object):
    def bark(self):
        print('汪汪叫')
    def eat(self):
        print('啃骨头')


#定义一个God类
class God(object):
    def play(self):
        print("在云中飘一会")
    def eat(self):
        print("吃蟠桃仙丹")

#定义一个哮天犬类，继承Dog类和God类两个类
class XTQ(Dog,God): # XTQ有两个父类，这个继承关系称为多继承，XTQ类对象，可以调用两个父类中的属性和方法
    pass

# 创建一个对象，调用XTQ类
xtq=XTQ()
xtq.eat()  #啃骨头 调用Dog类中的方法
xtq.play() # 在云中飘一会  调用God类中的方法
#结论
#当调用的方法两个父类中均存在的时候，调用的是子类定义中的第一个父类中的方法
```

**多继承调用指定父类中的方法：**

```python
# 定义一个狗类
class Dog(object):
    def bark(self):
        print('汪汪叫')
    def eat(self):
        print('啃骨头')


#定义一个God类
class God(object):
    def play(self):
        print("在云中飘一会")
    def eat(self):
        print("吃蟠桃仙丹")

#定义一个哮天犬类，继承Dog类和God类两个类
class XTQ(Dog,God): # XTQ有两个父类，这个继承关系称为多继承，XTQ类对象，可以调用两个父类中的属性和方法
    def eat(self):
        print("子类重写eat方法，调用子类自己的方法")
        # 调用指定父类中的方法
        # 方法一 类名.方法名(self,其他形参）
        God.eat(self)
        # 方法二 super(XTQ,self).eat(其他形参)调用XTQ父类中的方法
        # super(God,self).eat() # 调用的是God父类中的方法

# 创建一个对象，调用XTQ类
xtq=XTQ()
xtq.eat()  #子类重写eat方法，调用子类自己的方法  # 吃蟠桃仙丹 这里调用了指定父类God中的方法

xtq.play() # 在云中飘一会  调用God类中的方法


# tips
# 类名.__mro__ 可以查看当前类的继承顺序链，也叫做方法的继承顺序
print(XTQ.__mro__)
# (<class '__main__.XTQ'>, <class '__main__.Dog'>, <class '__main__.God'>, <class 'object'>)
# 这里是因为定义的时候，将Dog类放在了前面
```

![1644636994584](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1644636994584.png)

#### 26.6 私有权限

私有权限：即在**属性名**和**方法名**前面加上两个下划线

**特点**

1.类的私有属性 和 私有方法，都不**能通过对象直接访问**，只可以在本类内部访问

2.类的私有属性 和 私有方法，都**不会被子类继承**，子类也无法访问和调用

3.私有属性 和 私有方法 往往用来处理类的内部事情，***不通过对象处理***，起到**安全**作用

**eg：**

```python
'''私有属性：只需要在原属性名前加上两个下划线即可
目的：保证数据的相对安全
想要访问和使用私有属性：需要定义一个公有的方法，通过这个方法使用
因为私有属性，只能在类中使用，所以共有的方法是可以使用私有属性的'''

# 案例需求： 定义一个People类，定义属性ICBC_money,属性值指的是你在银行的存款余额
# 余额是不能通过对象去修改的，必须是合法终端才可以
class People(object):
    def __init__(self):
        self.__ICBC_money = 0
    def get_money(self): # 定义共有方法来获取私有属性-余额属性
        return self.__ICBC_money
    def change_money(self,money): # 定义公有方法，来从终端修改余额(即存入余额）
        self.__ICBC_money += money

# 定义一个对象
tt = People()
tt.change_money(1000)
print(tt.get_money()) # 1000
# print(tt.__ICBC_money) # AttributeError: 'People' object has no attribute '__ICBC_money'
# 报错，显示该属性并不存在
# 可知私有属性是不可以通过对象直接访问
tt.__ICBC_money = 200
print(tt.__ICBC_money) # 200
print('*'* 40)
print(tt.get_money()) # 1000
# 从上面可知tt.__ICBC_money = 200 的操作，不是修改了余额属性，而是从新添加了一个名为__ICBC_money的属性

# tips
# 对象.__dict__可以查看对象具有的属性信息，类型是字典，字典的key是属性名，字典的value是属性值
print(tt.__dict__)
# {'_People__ICBC_money': 1000, '__ICBC_money': 200}

# 结论：
# _People__ICBC_money 私有属性名变化了
# python中的私有属性本质是修改了属性的名字，在创建对象的时候，会自动修改属性名
# 在私有属性名称前加上“_"+ 类名 的前缀

```



**私有方法**

```python
'''私有方法：在方法的前边加上两个__,就为私有方法
私有方法，不能在类外部访问，也不能通过实例化对象直接调用
作用：一般作为类内部的方法使用，不能在外部直接使用，保证业务逻辑不被破坏
使用方法：因为私有方法只能在类内部使用，所以可以定义公有方法，在公有方法内部调用
   可以应用在两个方法的发生有先后顺序，一方作为另一方的调用前提时使用，保证不能只调用后者'''

class Dog(object):
    def born(self):
        """生产后要休息30天"""
        print('生了一只小狗。。。。')
        self.__sleep()  # 在公有方法中通过实例调用私有方法
    # def sleep(self):
    #     print("休息30天")
    def __sleep(self):  # 将其定义为私有方法后，就不能在外面调用了
        print("休息30天") # 想使用私有方法就可以通过在公有方法中调用它
# 这种情况，是可以直接调用sleep方法的
dog = Dog()
dog.born() # 生了一只小狗。。。。    休息30天
# dog.sleep() # 休息30天
```



#### 26.7 类方法 & 类属性

**实例对象**

实例对象：通过class定义的类创建的，即通过类实例化来的

实例属性：通过实例对象（self）定义的属性称为实例属性，即 self.name = 'bbb' 

实例属性的特点：每个实例对象都有此属性，但是值可能是不同的

***类对象***

类对象概念：通过class定义的，是python解释器**在创建类的时候**自动创建的

**作用：**1.通过类对象可以定义实例对象（对象创建的实质）

​           2.类对象可以保存一些属性信息，称为类属性

**类属性的定义**：类内部，方法外部定义的变量就是类属性

如果这个属性值对于不同实例是不同的，则定义为实例属性

如果这个属性值对于不同实例是相同的，则定义为类属性

```python
class Dog(object):
    #  定义类属性，类名
    class_name = '狗类'
    def __init__(self,name,age):
        # 通过self.属性名 定义的为实例对象
        self.name = name
        self.age = age
        print(self.class_name) # 定义在实例方法外，但是可以在实例方法内使用

# 创建对象
dog = Dog('大橘',2)
print(dog.__dict__)  # {'name': '大橘', 'age': 2}

# 查看类对象具有的属性
print(Dog.class_name)  # 狗类
```

```python
print(dog.class_name)  # 狗类
# 结论
# 如果实例属性不和类属性重名的话，也是可以通过实例对象调用类属性
```

***类方法***

**实例方法：**类中默认定义的方法，就是实例方法，第一个形参为self，表示实例对象

**类方法**：使用@classmethod装饰的方法，称为类方法，他的第一个参数为cls，代表的是类对象自己

**使用**：如果在方法中使用了实例属性，那么该方法必须定义为实例方法

​          如果不需要使用实例属性，需要使用类属性，**可以**将这个方法定义为类方法(当然实例方法也不会报错)

​         如果既不需要使用实例属性，也不需要使用类属性，可以将这个方法定义为静态方法

```python
class Dog(object):
    #  定义类属性，类名
    class_name = '狗类'
    def __init__(self,name,age):
        # 通过self.属性名 定义的为实例对象
        self.name = name
        self.age = age
        print(self.class_name)

    def play(self):
        print(f"小狗{self.name}在快乐的玩耍")
    # def get_class_name(self): # 是实例方法，但是代码块中没有使用实例属性，可以将其定义为类方法也是可以的
    #     return Dog.class_name  # 返回类属性

    @classmethod
    def get_class_name(cls):  # 这里的默认形参变成了cls
        # return Dog.class_name
        return cls.class_name  # 可以将类名替换成cls
# 创建对象
dog = Dog('大橘',2)
print(dog.__dict__)  # {'name': '大橘', 'age': 2}


print(dog.get_class_name()) # 调用类方法，可以通过对象
print(Dog.get_class_name()) # 狗类 也可以通过类名
```



***静态方法***

概念：使用@staticmethod装饰的方法，称为静态方法

使用前提： 不需要使用实例属性，同时也不需要使用类属性，此时可以将这个方法定义为静态方法

eg：

```python
class Dog(object):
    #  定义类属性，类名
    class_name = '狗类'
    def __init__(self,name,age):
        # 通过self.属性名 定义的为实例对象
        self.name = name
        self.age = age
        print(self.class_name)

    def play(self):
        print(f"小狗{self.name}在快乐的玩耍")

    @staticmethod
    def show_info(name):
        print(f"调用静态方法，hello，{name}") # 静态方法也可以传递参数

# 创建对象
dog = Dog('大橘',2)
print(dog.__dict__)  # {'name': '大橘', 'age': 2}


dog.show_info('jiajia') # 调用静态方法，可以通过对象
Dog.show_info('jiajia') #  也可以通过类名
```



#### 26.8 多态

eg：

```python
"""
多态：在需要使用父类对象的地方，也可以传入子类对象，调用的是类中同名方法，得到不同的结果
实质：定义一个函数，形参类型为实例对象，在函数中通过形参调用子类和父类的同名方法
步骤：1:子类继承父类
     2：子类重写父类中的同名方法
     3：定义一个共同的方法(函数)，参数为对象，在函数代码块中调用父类和子类同名的方法
"""
class Dog(object):
    def __init__(self,name):
        self.name =name
    def play(self):
        print(f"小狗{self.name}在玩耍。。。。。")

class XTQ(Dog):
    # 重写play方法
    def play(self):
        print(f"小狗{self.name}在追云彩。。。")

# 4.定义一个共同的方法：
def play_with_dog(obj_dog):
    obj_dog.play()


# 创建对象
dog = Dog('大黄')
play_with_dog(dog) # 小狗大黄在玩耍。。。。。 函数的传参是上面的对象 如果对象是根据父类创建，调用的方法就是父类的

xtq = XTQ('花花')
play_with_dog(xtq)  # 小狗花花在追云彩。。。   如果对象是根据子类创建，调用的方法就是父类的
```

![1644853584364](C:\Users\宝龟儿\AppData\Roaming\Typora\typora-user-images\1644853584364.png)

### 27.1异常捕获：

```python
num = input("请输入一个数字：")
try:
    n = 10/int(num)
    print(f"计算得到的结果{n}")
except Exception as info:  # 因为Exception是常见ZeroDivisionError等异常类的父类，所以可以用Exception接收所有异常
    print(f"您的代码发生错误，错误信息为：{info}")
"""
请输入一个数字：0
您的代码发生错误，错误信息为:division by zero
"""
```

### 28.模块 & 包

#### 28.1 模块的导入

```python
# 想要使用模块中的内容，必须先导入模块
# 方法一 import 模块名
# 使用： 模块名.功能名
import aa
dog = aa.Dog('大黄')  # 使用aa中的Dog类创建对象
dog.play()    # 使用类中的方法
aa.play_with_dog(dog) # 使用aa模块中的函数play_with_dog

# import imp  # 导入的时候即会将源模块中的代码执行一遍

# 方法二： from 模块名 import 功能名1，功能名2....
# 使用：功能名
# 注意：在使用时因为直接使用功能名(类，函数，变量)，如果导入不同模块有重复的功能名，会被覆盖
from imp import Dog,Dog1
gou = Dog('tom',2)
print(gou.name)
print(Dog.class_get_count())

# 方法三 from 模块名 import *  # 将模块中所有的功能导入
# 使用： 功能名
# 同上
```

```python
# 给模块或者功能名赋别名
# as 起别名
# 注意：如果使用as别名，就不能再使用原来的名字
import imp as i01
dog1 = i01.Dog('tom',2)
print(dog1.age)

```

自己定义的模块名字不要和系统中的已经定义好的模块名有重复

因为在你导入模块时，模块的搜索顺序为：

当前目录---->系统目录------>都没有就会发生报错

查看模块搜索顺序的可以打印环境变量path

import sys

print(sys.path)