# Python的条件和循环
## 一、if语句
1.语法
```
if 条件1:
    代码块1
elif 条件2:
    代码块2
else:
代码块3
```
2.！！！缩进：缩进就是在语句前的空格数量（通常一个tab键 == 四个空格），在 Python 中，缩进是至关重要的。 if、elif 和 else 语句都是根据缩进来寻找匹配对象的。为了规范：一个程序中的缩进应当只用一种形式，即只用tab键 或者 只用空格，不要混用
3.可以使用逻辑运算符（如 and、or 和 not）来构建更复杂的条件
## 二、While语句
1.语法
while 条件:
    # 循环体，当条件为 True 时执行
    # ...
2.要小心避免无限循环。如果条件永远为 True，程序将永远执行循环体，这可能导致程序无响应。要确保在循环体内适当地更新循环控制变量，能够使条件最终变为 False。（即：要在循环体中，设置能改变条件结果的值）
3.使用continue语句，直接结束本次循环，开启下一次循环
4.使用 break 语句提前退出循环。break只能跳出本层循环
## 三、for语句
1.语法
```
for 变量 in 可迭代对象:
           循环体
```
四、Range()函数
1.语法：range() 是 Python 内置函数，用于生成一个整数范围的序列
2.range(起始值, 终止值, 步长)，不包含终止值，到终止值之前。start 默认为 0，step 默认为 1
## 五、程序结构
（一）顺序结构：从上到下，依次执行每条语句的程序
（二）选择结构
1．单分支结构if的语法结构：
```
if   表达式:
       语句块

number=eval(input('请输入您的号码：'))
if number==123456:
print('恭喜您中奖了！')
```
2．双分支结构if…else…语法结构：
```
if   表达式:
       语句1
else:
        语句2

number=eval(input('请输入您的号码：'))
if number==123456:
    print('中奖了')
else:
print('没有中奖')
```
3．多分支结构：
```
if 表达式1:
      语句块1
elif 表达式2:
       语句块2
elif 表达式n:
      语句块n
else:
       语句块n+1

#成绩等级划分
score=eval(input('请输入您的成绩：'))
if score<0 or score>100:
    print('您的成绩有误')
elif 0<=score<60:
    print('E')
elif 60<=score<70:
    print('D')
elif 70<=score<80:
    print('C')
elif 80<=score<90:
    print('B')
else:
print('A')
```
4．还可互相嵌套使用，但最多不超过三层
```
#酒驾判断
answer=input('请问您喝酒了吗：')
if answer=='yes':
    proof=eval(input('请输入酒精含量：'))
    if proof<20:
        print('不构成酒驾')
    elif 20<=proof<80:
        print('酒驾')
    else :
        print('醉驾')
else:
    print('没事，可以走了')
```
（三）循环结构
1．在Python中循环结构分两类，一类是遍历循环结构for，一类是无限循环结构while
2．For循环：
（1）遍历循环for的语句结构：
```
for 循环变量 in 遍历对象:
        语句块
```
（2）for…else…结构
```
for 循环变量 in 遍历对象:
    语句块1
else:
语句块2

s=0
for i in range(101):
    s=s+i
else:
    print(s)
```
3．while循环的四个步骤：初始化变量，条件判断，执行语句块，改变变量
（1）无限循环while的语句结构：
```
while 表达式:
     语句块

answer=input('今天上课吗？Y/S:')
while answer=='Y':
    print('好好上课')
    answer=input('今天上课吗？Y/S')
```
（2）while…else…结构
```
while 表达式:
语句块1
else:
语句块2
```
（四）空语句pass：在语法结构中只起到占位符作用，使语法结构完整，不报错
（五）Match ...case..结构
```
score=input('请输入成绩等级:')
match score:
    case 'A':
        print('优秀')
    case 'B':
        print('良好')
    case 'C':
        print('中等')
    case 'D':
        print('及格')
    case 'E':
        print('不及格')
```

