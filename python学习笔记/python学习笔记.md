<!-- TOC -->

- [1. python学习笔记](#1-python%e5%ad%a6%e4%b9%a0%e7%ac%94%e8%ae%b0)
  - [1.1. 规范](#11-%e8%a7%84%e8%8c%83)
  - [1.2. “\”用法](#12-%e7%94%a8%e6%b3%95)
  - [1.3. "+"](#13-%22%22)
  - [1.4. 占位符](#14-%e5%8d%a0%e4%bd%8d%e7%ac%a6)
  - [1.5. 格式化字符串](#15-%e6%a0%bc%e5%bc%8f%e5%8c%96%e5%ad%97%e7%ac%a6%e4%b8%b2)
  - [1.6. 变量,对象特性](#16-%e5%8f%98%e9%87%8f%e5%af%b9%e8%b1%a1%e7%89%b9%e6%80%a7)
    - [1.6.1. 输出](#161-%e8%be%93%e5%87%ba)
    - [1.6.2. 输入](#162-%e8%be%93%e5%85%a5)
  - [1.7. 强制类型转换](#17-%e5%bc%ba%e5%88%b6%e7%b1%bb%e5%9e%8b%e8%bd%ac%e6%8d%a2)
  - [1.8. for 循环](#18-for-%e5%be%aa%e7%8e%af)
    - [1.8.1. range()](#181-range)
  - [1.9. 表，序列](#19-%e8%a1%a8%e5%ba%8f%e5%88%97)
    - [1.9.1. [:::]](#191)
    - [1.9.2. 基本函数](#192-%e5%9f%ba%e6%9c%ac%e5%87%bd%e6%95%b0)
  - [1.10. 元组](#110-%e5%85%83%e7%bb%84)
  - [1.11. 交换两个变量的值](#111-%e4%ba%a4%e6%8d%a2%e4%b8%a4%e4%b8%aa%e5%8f%98%e9%87%8f%e7%9a%84%e5%80%bc)
  - [1.12. == != is](#112---is)
  - [1.13. 字典（dict）](#113-%e5%ad%97%e5%85%b8dict)
    - [1.13.1. 命名空间](#1131-%e5%91%bd%e5%90%8d%e7%a9%ba%e9%97%b4)
  - [1.14. 集合](#114-%e9%9b%86%e5%90%88)
  - [1.15. 函数](#115-%e5%87%bd%e6%95%b0)
  - [1.16. 不定长求和函数](#116-%e4%b8%8d%e5%ae%9a%e9%95%bf%e6%b1%82%e5%92%8c%e5%87%bd%e6%95%b0)
  - [1.17. 参数解包](#117-%e5%8f%82%e6%95%b0%e8%a7%a3%e5%8c%85)
  - [1.18. 文档字符串](#118-%e6%96%87%e6%a1%a3%e5%ad%97%e7%ac%a6%e4%b8%b2)
  - [1.19. 匿名函数](#119-%e5%8c%bf%e5%90%8d%e5%87%bd%e6%95%b0)
  - [1.20. 不定参的函数加装饰函数](#120-%e4%b8%8d%e5%ae%9a%e5%8f%82%e7%9a%84%e5%87%bd%e6%95%b0%e5%8a%a0%e8%a3%85%e9%a5%b0%e5%87%bd%e6%95%b0)
  - [1.21. 类](#121-%e7%b1%bb)
  - [1.22. 特殊方法](#122-%e7%89%b9%e6%ae%8a%e6%96%b9%e6%b3%95)
  - [1.23. 封装](#123-%e5%b0%81%e8%a3%85)
    - [1.23.1. 装饰器](#1231-%e8%a3%85%e9%a5%b0%e5%99%a8)
  - [1.24. 继承](#124-%e7%bb%a7%e6%89%bf)
    - [1.24.1. 函数覆盖](#1241-%e5%87%bd%e6%95%b0%e8%a6%86%e7%9b%96)
  - [1.25. 多重继承](#125-%e5%a4%9a%e9%87%8d%e7%bb%a7%e6%89%bf)
  - [1.26. 多态](#126-%e5%a4%9a%e6%80%81)
  - [1.27. 类中的属性和方法总结](#127-%e7%b1%bb%e4%b8%ad%e7%9a%84%e5%b1%9e%e6%80%a7%e5%92%8c%e6%96%b9%e6%b3%95%e6%80%bb%e7%bb%93)
  - [1.28. import](#128-import)
    - [1.28.1. 包 package](#1281-%e5%8c%85-package)
    - [1.28.2. \__pycache__文件夹](#1282-pycache%e6%96%87%e4%bb%b6%e5%a4%b9)
    - [1.28.3. sys包](#1283-sys%e5%8c%85)
    - [1.28.4. os模块](#1284-os%e6%a8%a1%e5%9d%97)
  - [1.29. try](#129-try)
  - [1.30. 抛出异常](#130-%e6%8a%9b%e5%87%ba%e5%bc%82%e5%b8%b8)
  - [1.31. 文件读取](#131-%e6%96%87%e4%bb%b6%e8%af%bb%e5%8f%96)
    - [1.31.1. 打开文件](#1311-%e6%89%93%e5%bc%80%e6%96%87%e4%bb%b6)
    - [1.31.2. 读取文件](#1312-%e8%af%bb%e5%8f%96%e6%96%87%e4%bb%b6)
      - [1.31.2.1. 文件读取编码处理](#13121-%e6%96%87%e4%bb%b6%e8%af%bb%e5%8f%96%e7%bc%96%e7%a0%81%e5%a4%84%e7%90%86)
      - [1.31.2.2. 读取二进制文件](#13122-%e8%af%bb%e5%8f%96%e4%ba%8c%e8%bf%9b%e5%88%b6%e6%96%87%e4%bb%b6)
  - [1.32. 文件读取进度](#132-%e6%96%87%e4%bb%b6%e8%af%bb%e5%8f%96%e8%bf%9b%e5%ba%a6)
  - [1.33. 文件写入](#133-%e6%96%87%e4%bb%b6%e5%86%99%e5%85%a5)
  - [1.34. 其他调用操作](#134-%e5%85%b6%e4%bb%96%e8%b0%83%e7%94%a8%e6%93%8d%e4%bd%9c)
  - [1.35. python加入数据库](#135-python%e5%8a%a0%e5%85%a5%e6%95%b0%e6%8d%ae%e5%ba%93)

<!-- /TOC -->
# 1. python学习笔记

>这个笔记主要是用来记录与其他语言的区别之处

## 1.1. 规范

1. 类或函数定义后有2个空行  

2. 例如：，：之类的字符需要紧贴前一个字符串与后一个字符串之间保持一个空格

3. 类名用单词首字母大写命名法如：class MyClass  
方法名用小写如：hello()

4. ``print("内容")``打印函数默认会换行，若不想换行可改写为
``print("内容", end=" ")``

## 1.2. “\”用法

一行能写下代码时可用"\"，可以连接上下行

## 1.3. "+"

两个字符串用"+"连接可以形成一个完整的字符串，也可对连接后字符串进行赋值验证

## 1.4. 占位符

”%s“在字符串中表示任意字符或字符串

“%f”表示浮点数

%d表示整数

>用法：``b = "Hello %S" % "world" #字符串外用“%”后表示填充元素``  
%3s 表示限制最少三个字符串，若少于三个则在前面用空格填充  
%3.5s 表示限制字符个数为3-5个  
%.2f  表示保留两位小数

## 1.5. 格式化字符串

{}表示内容为变量
例如：

```python
a = 123
b = "Hello"
c = f'{b} world {a}'
print(c)
#输出为：Hello world 123
```

## 1.6. 变量,对象特性

一切皆对象
对象有三个属性id(地址) type(类型) value(值)
python中变量是给对象起的别名，并不是存储对象的值，而是存储对象所在的地址

```python
a = [1,2,3]
print("a",a,id(a))
b = a
b[0] = 10
print("a",a,id(a))
print("b",b,id(b))
a = [20,30]
print("a",a,id(a))
```

### 1.6.1. 输出

```python
a [1, 2, 3] 1934094215240
a [10, 2, 3] 1934094215240
b [10, 2, 3] 1934094215240
a [20, 30] 1754187955208
```

>&emsp;&emsp;可以看到变量a,b指向同一个地址（id()函数可用用来看地址），修改b的元素，a也会随之修改，但是用索引方式修改不会改变变量指向的地址，重新给a赋值，a所指向的地址才会改变。

### 1.6.2. 输入

input函数
>input函数每次只能接收一个值，而且是字符串，而且显示出来的类型为字符串类型
>因此在一行中，输入几个数字成了一个难点，因为虽然可以用input函数接收一个数字，然后类型转换成字符串  
但是在引用一次input函数，就只你能按回车结束上一个input函数的输入，不能用空格间隔输入两个数字

解决办法：``a,b,... = map(int, input().split())``
更严谨的用法：``map(int input().strip().split())``

Python split() 通过指定分隔符对字符串进行切片，有两个参数，第一个是str就是分隔符，第二个是分割次数。默认为 -1, 即分隔所有。返回分割后的字符串列表。(注意是返回列表)(且返回的列表中没有分割符)

例如：

```python
str = "Line1-abcdef \nLine2-abc \nLine4-abcd";
print str.split( );       # 以空格为分隔符，包含 \n
print str.split(' ', 1 ); # 以空格为分隔符，分隔成两个
```

strip() 方法用于移除字符串头尾指定的字符（默认为空格）。

map() 会根据提供的函数对指定序列做映射。  
第一个参数 function 以参数序列中的每一个元素调用 function 函数，返回包含每次 function 函数返回值的新列表。
(这里是将返回的值，改为int类型)
例如：

```python
>>> map(square, [1,2,3,4,5])   # 计算列表各个元素的平方
[1, 4, 9, 16, 25]
>>> map(lambda x: x ** 2, [1, 2, 3, 4, 5])  # 使用 lambda 匿名函数
[1, 4, 9, 16, 25]
```

***

## 1.7. 强制类型转换

python强制类型转换用函数
int()  float()  str()   bool()

## 1.8. for 循环

```python
for i in range(5):
# range()用来生成一个自然数的序列
    print(i)
#输出为 0 1 2 3 4
```

>当range(n),当参数为一个变量，而range的参数需要的是一个int类型，所以需要先使变量类型转换，应写为：range(int(n))

```python
for s in "hello":
    print(s)
    #输出为 h e l l o
```

### 1.8.1. range()

range()用来生成一个自然数的序列

有三个参数：
第一个表示开始第二个表示结束（不包含） 第三个表示间隔

```python
a = range(1, 5, 2)
print(a)
for i in a :
    print(i)
for i in range(2,6):
    print(i)
```

输出为：

```python
1
3
2
3
4
5
```

## 1.9. 表，序列

表和序列是一个意思

a = [1,2,3,4,5]  
有点像其他语言里面的数组和广义表的结合版  
表的元素可以为不同的类型  
用重0开始的索引查找  

```python
a = [1,2,[3,8],4,5]
print(a[0])
print(a[2])
```

输出为:

```python
1
[3, 8]
```

### 1.9.1. [:::]

```python
a =[1, 2, 3, 4, 5, 6, 7]
print(a[1:5])
print(a[1:6:2])

```

输出为：

```python
[2, 3, 4, 5]
[2, 4, 6]
```

>有三个参数：
第一个表示开始第二个表示结束（不包含） 第三个表示间隔

### 1.9.2. 基本函数

stus = [1, 3,4 ,5 ,6, 7, 5]

- clear()
  - 清空序列
  - 用法：stus.clear()
- pop()
  - 根据索引删除并返回被删除的元素
  - 用法：stus.pop()
- remove()
  - 删除指定的元素，如果相同值的元素有多个，只删除第一个
  - 用法：stus.remove()
- reverse()
  - 反转列表
  - 用法：stus.reverse()
- sort()
  - 用来对列表进行排序
  - 用法：stus.sort()
  
## 1.10. 元组

a = (10,20,30)
这就是一个元组  

- 注意
  - 元组内的值不能修改
  - 当元组不为空时，括号可以省略
  - 如果元组的值只有一个后面也要加一个逗号
  
```python
a = (10,20,30,40,50)
b , c , *d = a
#在变量前添加一个*，这样的变量或获得元组剩余的元素
#一个组只能出现一个*
print(a)
print(b)
print(c)
print(b)
```

输出为：

```python
(10, 20, 30, 40, 50)
10
20
[30, 40, 50]
```

***

## 1.11. 交换两个变量的值

```python
a = 10
b = 20
a , b = b , a
#用到的是元组的解包
```

## 1.12. == != is

== 只是比较对象的值是否相等

is is not 比较的是对象的id(地址)和value值是否相等(是否是同一个对象)

```python
a = [1,2,3]
b = [1,2,3]
c = a
print(a == b)
print(a is b)
print(a is c)
```

输出为：

```python
True
False
True
```

## 1.13. 字典（dict）

就是一个键值对，构成的一个集合（有点像PHP中的数组key可以为一个字符串）  
**键是不可变量，不能重复**

```python
d = {"name":"j" ,
"age":18 ,
"gender":"man"
}
print(d,type(d))
print(d["name"])
print("name" in d)#检查字典中是否含有某个键用 in
print("key" in d)
print(d.get("key"))#获取键值也可以get
print(d.get("key","nihao"))#若获取的键没有值可以指定一个值
```

输出为：

```python
{'name': 'j', 'age': 18, 'gender': 'man'} <class 'dict'>
j
True
False
None
nihao
```

### 1.13.1. 命名空间

全局变量都放在一个字典里面

局部变量（例如函数里的变量），一个函数也单独放在一个字典里面

可以在全局变量中定义一个变量

```python
space = locals()
print(space)
```

就可以看到当前空间内的键值对，函数查看原理相同  
用globals()可在任意位置看到全局命名空间
***

## 1.14. 集合

python的集合与数学中的集合有点像  
不能有重复元素

```python
s = {1, 2, 3, 4, 5}
s1 = {1,3,4,5,6}
s1.add(10)#像集合内添加元素
print(s1)
result = s & s1#求交集
print(result)
result = s | s1#求并集
print(result)
result = s - s1#求差集
print(result)
result = s <= s1#是否为子集
print(result)
```

输出为：

```python
{1, 3, 4, 5, 6, 10}
{1, 3, 4, 5}
{1, 2, 3, 4, 5, 6, 10}
{2}
False
```

## 1.15. 函数

>定义函数：  
def 函数名(参数):  
&emsp;&emsp;函数体
***
>注意：与其他语言不同的是传递实参给形参时，传递的是地址 ，  
也就是改变形参的值也会直接改变实参的值！
>python内的函数可以嵌套定义

python函数返回多个值  
直接return a,n,d #a,n,d是需要返回的值  
这个利用了python，这时a,n,d，自动类型转换成为了一个元组

```python
def hanshu()
    return a,n,d

b,c,v = hanshu()
#利用元组的解包
```

## 1.16. 不定长求和函数

```python
def sum(*a):
    result = 0
    for i in a:
        result +=i
    print(result)
sum(1, 2, 3, 4)
#输出为：10
```

方法利用了元组
这种方法使用时，若函数还有其他参数，需要用到关键字参数
例如：

```python
def p(a,*b,c):
    print("a=", a)
    print("b=", b)
    print("c=", c)


p(2, 3, 4, 5, c=6)
```

输出为：

```python
a= 2
b= (3, 4, 5)
c= 6
```

*形参只能接收位置形参，不能接收关键字形参

## 1.17. 参数解包

```python
def e(a, b, c):
    print("a=", a)
    print("b=", b)
    print("c=", c)


c = (1, 2, 3) #元组
d = {"a": 1, "b": 2, "c": 3} #字典
e(*c)
e(**d)
```

输出为：

```python
a= 1
b= 2
c= 3
a= 1
b= 2
c= 3
```

*对元组进行解包将其个值赋给形参

\**对字典进行解包将其**值**赋给形参
>注意：元组或字典内元素个数要和形参个数一致

## 1.18. 文档字符串

``def(a:int, b:float, c:int)``
>可以对函数的参数进行描述，其需要一个什么类型的值，但是不是强制要求

用'''这里面写文档，会保留文档格式'''

在函数内写对函数进行描 述
用help(函数名)可查看

## 1.19. 匿名函数

用lambda来定义一般函数定义用的是def
这种函数一般用于一个函数的参数，简单的函数计算等

```python
a = 7
# f是参数 f>5是返回值
b = (lambda f: f > 5)(a) #传参
print(b)
#输出为：true
```

## 1.20. 不定参的函数加装饰函数

```python
def add(c, d):
    print(c + d)


def fn():
    return print("你好")


def begin(han):
    def f(*a, **b):
        shu = han(*a, **b)
        print("over")
        return shu
    return f


print("-"*10)
ww = begin(add)
nn = begin(fn)
nn()
ww(2, 3)
```

>python 支持嵌套定义函数
用begin定义一个新的函数，在不改变原函数的前提下，在函数后输出了``print("over")``,为了使不同参数都适用，使用(*a, **b)取参数。

## 1.21. 类

isinstance()#检查一个实例，用的类是不是那个

```python
class MyClass():
    pass


my = MyClass()
result = isinstance(my, MyClass)
print(result)
#输出为 true
```

***
python调用类中的方法时，每一个方法每次被调用时，解析器都会自动的传递第一个实参，第一个实参就是调用方法的对象本身

假如有同一个类的两个实例p1,p2，如果p1调用的，则第一个参数就是p1对象，如果p2调用的，则第一个参数就是p2对象

类中的每一个方法一般第一个参数命名为self

## 1.22. 特殊方法

特殊方法都是以__开始,以__结束(前后两个下划线)
\__init__()#类似c++的构造函数

```python
class MyClass:
    def __init__(self,name):
        self.name = name

    def hello(self):
        print("world")


my = MyClass("jj")
print(my.name)
my.hello()
#输出为：jj world
```

>\__init__(self)方法，在实例创建是自动执行

\__del__(self)方法，相当于c++的析构函数，在对象使用完被回收时，使用

## 1.23. 封装

>为类中每一个变量设置get，set两个函数，使类封装起来，来得到或设置变量，不想让别人直接调用变量修改，个人认为利于界面化操作，接触不到底层代码时使用。

```python
class MyClass:
    def __init__(self,name):
        self._name = name

    def get_name(self):
        return self._name

    def set_name(self, name):
        self._name = name

    def hello(self):
        print("word")


my = MyClass("jj")

print(my.get_name())
my.set_name("yy")
print(my.get_name())
#输出：jj yy
```

>修改name属性为_name告诉别人，不允许修改，但是只是告诉想修改还是可以的，给出get_name , set_name 方法给用户，用来查看和修改.

### 1.23.1. 装饰器

```python
class MyClass:
    def __init__(self, age, name):
        self._age = age
        self._name = name

    @property
    def age(self):
        return self._age

    @age.setter
    def age(self, age):
        self._age = age


my = MyClass(22, "jj")
print(my.age)
my.age = 18
print(my.age)
#输出：22 18
```

>每个get方法前面加@property，每个set方法前面加@方法名.setter，在进行函数调用时，可以省略（），看着像是在调用变量一样，使用时@property，@方法名.setter，需要同时出现，或者只出现第一个

## 1.24. 继承

```python
class Animal(object):
    def run(self):
        print("它会跑")

    def eat(self):
        print("它会吃")


class Dog(Animal):
    pass


d = Dog()
d.run()
print(isinstance(d, Dog))
print(isinstance(d, Animal))
print(issubclass(Dog, Animal))
print(issubclass(Animal, object))

```

输出为：

```python
它会跑
True
True
True
True
```

>继承在定义类时后加括号加入父类  
所有类的父类都是object可以省略
>>isinstance()验证某个实例是不是来源于某个类  
issubclass()验证某个类的是不是它的父类

### 1.24.1. 函数覆盖

子类中定义了与父类同名的方法，通过子类实例调用方法时，会调用子类的方法，发生了函数覆盖。

**注意：**
>当子类继承了父类的一个方法，但是方法的参数有很多，子类只有新增的一些参数需要修改，用函数覆盖，写函数时，不像再初始化那些不变的参数，这时可以调用父类的参数来初始化属性。

```python
class Animal:
    def __init__(self, name, age, height):
        self._name = name
        self._age = age
        self._height = height

    def run(self):
        print("它会跑")

    def eat(self):
        print("它会吃")


class Dog(Animal):
    def __init__(self, name, age, height, play):
        super().__init__(name,age,height)
        self._play = play


d = Dog("jj", 18, 175, "happy")
d.run()
print(d._name)
print(d._play)
#输出为：它会跑 jj happy
```

>super()可以获取当前类的父类

## 1.25. 多重继承

>多重继承中，子类可以继承所有父类中的属性，但是当多个父类有了同一个方法，此时，子类先继承第一个父类，第一个父类没有才会继承第二个父类。  
写法：
``class Dog(Animal, Quan)``

## 1.26. 多态

面向对象中，多态性，指只要你还有某种属性就可以调用
不在意类型，体现多态的灵活性

## 1.27. 类中的属性和方法总结

>类属性：直接在类中定义的属性  
属性可以通过类或类的实例访问到  
但是类属性只能通过类对象来修改，无法通过实例对象修改  
***
>实例属性：通过实例对象添加的属性
实例属性只能通过实例对象来访问和修改，类对象无法访问和修改
***
>实例方法：在类的定义中，以self为第一参数的方法都是实例方法  
实例方法在调用时，python会调用实例对象作为self传入  
当通过类调用时，不会自动传递self，此时需要手动传递一个实例对象在类对象的参数中
***
>类方法：在类的内部使用@classmethod来修饰的方法属于类方法  
类方法的第一个参数是cls，也会自动传递，cls就是当前的类对象
***
>类方法和实例方法的区别，实例方法的第一个参数是self，类方法的第一个参数是cls  
类方法可以通过类去调用也可以通过实例调用，没有区别
***
>静态方法：在类中使用@staticmethod来修饰的方法  
静态方法不需要指定任何默认参数，静态方法可以通过类和实例对象去调用  
静态方法，基本与的当前类无关，就是一个保存到当前类的一个函数

```python
class Animal:
    count = 0

    def __init__(self, name, age, height):
        self._name = name
        self._age = age
        self._height = height

    def play(self):
        print("我是一个实例方法",self)

    @classmethod
    def happy(cls):
        print("我是：", cls)


    @staticmethod
    def aa():
        print("我是一个静态方法")


d = Animal("jj", 18, 175, )
print(Animal.count)
print(d.count)
Animal.count = 10
d.count = 20  #只是向实例对象中添加了一个count的属性，并没有修改原对象中类对象
print(Animal.count)
print(d.count)
d.play()
Animal.play(d)#类对象调用实例方法时，需要传一个实例对象
d.happy()
Animal.happy()
d.aa()
Animal.aa()
print(d._name)
print(Animal._name) #报错：AttributeError: type object 'Animal' has no attribute '_name'
```

输出为：

```python
0
0
10
20
我是一个实例方法 <__main__.Animal object at 0x000002520DB16248>
我是一个实例方法 <__main__.Animal object at 0x000002520DB16248>
我是： <class '__main__.Animal'>
我是： <class '__main__.Animal'>
我是一个静态方法
我是一个静态方法
jj
AttributeError: type object 'Animal' has no attribute '_name'
```

## 1.28. import

import 后可引人第三方库或文件(去掉后缀.py)

import 模块名 as 别名

每个模块内部都有一个名字  
``print(__name__)``  
``print(模块名.__name__)``  
``print(别名.__name__)``  
都可以
name 为__main__为主模块

访问模块中的变量用模块名.变量名\对象名

- 引入莫块中的部分内容  
语法：from 模块名 import 对象，对象，对象....
注意：这种引入方式可以直接使用变量，不加模块名

- 引入模块中的所有内容  
from 模块名 import * 引入模块中的所有内容
注意：被引入模块中有以_开头的变量不会包含其中

- 若引入的内容与现文档内文件对象名重复
from 模块名 import 对象 as

- ``if __name__ == __main__:``只有当当前模块为主模块才会使用

### 1.28.1. 包 package

代码过多时，一个模块可以分解为多个部分，或一些功能相近的模块放到包里

普通模块是一个文件，包是一个文件夹
包中必须要有一个__init__.py,这个文件可以包含包中的主要内容

可以用from 文件夹名 import 文件名，文件名.....

### 1.28.2. \__pycache__文件夹

该文件为模块的缓存文件避免重复编译

### 1.28.3. sys包

![sys](sys模块.png "sys模块")

### 1.28.4. os模块

![os](os模块.png "os模块")

## 1.29. try

try:
    代码块（有可能出现错误）

except：
    代码块（出现错误以后的处理方式）
else：
    代码块（没出错时执行的语句）
finally:
    代码块（一定要执行的）

>else可省略 try必须存在 except、finally至少存在一个

## 1.30. 抛出异常

>python在报错时，实际是调用了，执行对象时，每个对象内内置了特殊方法，来应对错误，发出提示  
自己也可以做一个抛错机制。

raise用于向外抛出异常，后跟一个一行类型或异常实例

raise Exception("抛错内容")

此时会终止程序运行

也可以建立一个实例抛出异常

class MyEorr(Exception):
    pass
    raise MyEorr("抛错内容")

***

## 1.31. 文件读取

### 1.31.1. 打开文件

![打开文件](打开文件.png "打开文件")

### 1.31.2. 读取文件

![读取文件](读取文件.png "读取文件")

![读取文件](读取大文件1.png "读取大文件")

![读取大文件](读取大文件2.png "读取大文件")

![读取大文件](读取大文件3.png "读取大文件")

#### 1.31.2.1. 文件读取编码处理

![文件读取编码处理](文件读取编码处理.png "文件读取编码处理")

#### 1.31.2.2. 读取二进制文件

>python中除了文本文件，就是二进制文件

![读取二进制文件](读取二进制文件.png "读取二进制文件")

## 1.32. 文件读取进度

![文件读取位置](文件读取位置.png "文件读取位置")
![文件读取位置](文件读取位置2.png "文件读取位置")

## 1.33. 文件写入

![文件写入](文件写入.png "文件写入")

## 1.34. 其他调用操作

![其他调用操作](其他调用操作.png "其他调用操作")

![其他调用操作](其他调用操作2.png "其他调用操作")

## 1.35. python加入数据库

```python
    try:
        # 打开数据库连接
        db = pymysql.connect(host='localhost', port=3308, user='root', passwd='', db='car', charset='utf8')
        #这里最好用关键字输入，方便定位，我尝试不加关键字的话，会报错
    except:
        print("数据库连接失败")
        return
    # 使用cursor()方法获取操作游标
    cursor = db.cursor()
    # SQL 修改语句
#增
    sql = "INSERT INTO cars(id,\
       carNumber, c_type, state, in_t, out_t) \
       VALUES (null, '%s', '%s', '%s', '%s', '%s')" % \
          (carNumber, m_type, state, int_t, out_t)
#改
    sql ="update cars set state='go',out_t='%s' \
    where '%s'=carNumber and state='in'" % (out_t, carNumber)

    # 关闭数据库连接
    db.close()
    try:
        # 执行sql语句
        cursor.execute(sql)
        # 提交到数据库执行
        db.commit()
        print("数据库写入成功")
    except:
        # 如果发生错误则回滚
        db.rollback()
        print("数据库写入失败")
```

```python
    try:
        # 打开数据库连接
        db = pymysql.connect(host='localhost', port=3308, user='root', passwd='', db='car', charset='utf8')
    except:
        print("数据库连接失败")
        return
    # 使用cursor()方法获取操作游标
    cursor = db.cursor()
#查
    sql = "select id from cars where '%s'=carNumber and state='in'" % carNumber
    cursor.execute(car_sql)
    car_card = cursor.fetchone()
    #返回的是一个列表
    # fetchone(): 该方法获取下一个查询结果集。结果集是一个对象
    # fetchall(): 接收全部的返回结果行.
    # rowcount: 这是一个只读属性，并返回执行execute()方法后影响的行数。
    result_id = int(car_card[0])
     # 关闭数据库连接
    db.close()
```
