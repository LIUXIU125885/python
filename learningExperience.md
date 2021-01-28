 ### Python的发展历史：

  Python 是由 Guido van Rossum 在八十年代末和九十年代初，在荷兰国家数学和计算机科学研究所设计出来的。Python 本身也是由诸多其他语言发展而来的,这包括 ABC、Modula-3、C、C++、Algol-68、SmallTalk、Unix shell和其他的脚本语言等等。
 
### 一.python基本语法
#### 1.1 基本语法

     1.严格区分大小写
     2.一行一个语句，以换行结尾
     3.每行不要超过80字符，不要过长
     4.一条语句可以以多行，以\结尾
     5.不要随便缩进，严格执行
     6.注释（# 后的内容属于注释）
     
     命名规范
       下划线命名法，单词之间用_连接
       帕斯卡命名法（大驼峰命名），首字母大写，每个单词开头大写
#### 1.2 数据类型

     1.数值类型
         整数（int）无限制，可以无限大（如果数值长度过大，可以用下划线分割），二进制0b,八进制0o,十六进制0x，十进制不能以0开头x
         浮点数（float）,对浮点数进行运算，可能结果不太准确0.1+0.2
         复数
     2.字符串
         ', "只能在一行中使用\进行多行
         ''', """三重引号可以保留字符串格式
         转义字符:\u2255表示万国码unicode中的字符
         字符串不能和其他类型进行加法运算，不能拼接，print（'a='+a）不常用，print('a=',a);print(f'a={a}');print('a=%s'%a)常用，b='hellow %s'%'李旭'；b='hellow %s %s'%('李旭','ss'); %3.5s限制填充字符串在3到5之间
         %s字符串站位；%f浮点数；%d数字
         'abc'*2会重复abc两次'abcabc'
     3.布尔值（True,False）
     4.空值(None)
     
     类型检查 type(xx)
     
#### 1.3 对象

     每个对象保存的三种数据
     1.id（标识），不可变id（xx）查看内存地址
     2.type(类型）,不可变type(xx)查看类型
     3.value（值）
     
### 1.4 类型转换  

     int()
     float()
     str()
     bool()
     
### 1.5 运算符
#### 1.5.1 算术运算符

    +
    -
    *，**求幂运算  16**0.5
    /， //整除
    %
    
#### 1.5.2 赋值运算符

    =
    +=
    -=
    *=
    **=
    /=
    //=
    %=
    
#### 1.5.3 关系运算符
    
     >
     >=
     <
     <=
     ==
     !=
     is 比较id
     is not 
     字符串比较为逐位unicode比较
     
#### 1.5.4 逻辑运算符

     not 逻辑非 !
     and 逻辑与 &&  如果第一个是false则短路，直接返回false,否则在执行下一个  True and print('1')
     or 逻辑或 ||    如果第一个是true则短路，直接返回true,否则在执行下一个 False or print('1')
     非布尔值进行逻辑运算，会返回原值    
     
#### 1.5.5 条件运算符（三元运算符）
     
     语句1 if 条件表达式 else 语句2  print('1') if a>1 else print('2')
     
#### 1.5.6 运算符的优先级
    
    看官方文档表格
    input() 输入，可阻止文件结束，返回结果是字符串
     
### 1.6 流程控制语句 
     1.if语句
     
     if 表达式 : 
         代码块
     elif 表达式 ：
         代码块
     else:
         代码块
     
     代码块以缩进开始，恢复缩进结束  
     
     2.循环语句：
     while 条件表达式 :
         代码块
     else :
         代码块
     
     break：终止循环，直接退出
     continue：跳过当次循环
     pass：占位
     
     for s in my_list :
       print(s)

### 1.7 序列

    my_list = []
    len(my_list) 获取列表my_list的长度     
    my_list[1:4:1] 列表切片 
    'key' in my_list 检查key是否在my_list
    'key' not my_list
    min(my_list) 获取my_list列表中最小值
    max(my_list)
    my_list.index('key',1,5) 获取key在my_lsit列表中的索引
    my_list.count('key')  统计key在my_list中出现的次数 

#### 1.7.1 列表（可变序列）
   
   del my_list[1] 删除指定索引元素
   del my_list[0:2] 删除指定索引元素
   my_list[0:2]=['aa','bb','cc']  替换插入元素
   my_list[0:0] = ['aa','bb','cc'] 插入元素
   my_list.append('key') 列表最后添加元素
   my_list.insert(index,key) 向列表插入索引为insex的key
   my_list.extend(list) 添加序列list到my_list中
   my_list.clear() 清空序列
   my_list.pop(index) 删除指定元素并返回被删除元素或者最后元素 
   my_list.remove(key) 删除列表第一个指定元素
   my_list.reverse() 反转列表
   my_list.sort() 列表排序，默认升序排列  sort(reverse=true)降序
   
   range() 用于生成一个自然的序列 rang(起点,终点，步长)
   for i in range(30):
     print(i)
   
    
#### 1.7.2 字符串str（不可变序列）

   序列是python中最基本的一种数据结构
   数据结构是指计算机中数据存储的方式
   
#### 1.7.3 元组tuple（不可变序列）
     
   my_tuple = ()
   
   a,b,c,d = my_table  元组的解包 a,b =b,a交互a,b的值
     
     
### 1.8 字典（dict）
   
   和列表类似，是一种新的数据结构，称为映射
   
   {'name':'张三','age':18}
   dict(name='张三',age=15,sex='男')
   dict([('name','张三'),('age',18)])
   
   len(xx)
   in  检查字典中是否包含指定的键 
   not in
   
   dict_name['key'] 获取值
   dict_name.get('key','默认值')
   dict_name.setdefault('key',value) 如果dict_name存在key则返回当前值，否则返回设定值
   dict_name.update() 添加其他字典到dict_name,如果有重复的,则替换
   del dict_name(key) 删除指定的键
   dict_name.popitem() 删除最后一个，返回删除的键值元组
   dict_name.pop(key) 根据指定的key删除键值对，返回当前值，不存在会报错，可以指定默认值
   dict_name.clear() 清空字典
   dict_name.copy() 对字典进行浅复制，字典里面的对象会直接复制地址id
   
   for key in dict_name.keys :
      print(key, dict_name[key])
   
   for value in dict_name.values :
     print(value)
     
   for k,v in dict_name.items :
     print(k,'=',v)  
     

### 1.9 集合（set）
    
    1.只能存储不可变对象
    2.存储的对象是无序的
    3.不能出现重复的元素，唯一性
    
    {1,2,3,4,5,6}
    set_name = set() 创建一个空集合
    len()
    in
    not in
    set_name.add() 添加元素到集合
    set_name.update()
    set_name.pop() 随机删除并返回集合中的一个元素
    set_name.remove(value) 删除指定的值
    set_name.clear()
    set_name.copy()
    
    集合运算
     s1 & s2 交集运算&
     s1 | s2 并集运算|
     s1 - s2 差集运算-
     s1 ^ s2 异或集合 ^  去掉相同的元素生成的集合
     s1 <= s2 检查s1是不是s2的子集， s2是s1的超集 返回boolr类型
     s1 < s2 检查s1是不是s2的真子集， s2有s1所有元素并有其没有的元素
     s1 >= s2 检查s1是不是s2的超集
     s1 > s2 检查s1是不是s2的真超集
     

 
### 1.10 函数
 
   def 函数名（[参数]）：
      代码块
   
   函数名（） #调用
   
   位置参数fn（a,b）和关键字参数fn（a=5,b=6）,混合使用位置参数在前面
   
   不定长的参数fn(*a) 获取的a为元组接收所有的参数， 不定长参数后如果还有参数必须使用关键字传参
   **a参数 会直接保存到a字典中
   
   help()可以查询某个函数的用法，可以展示出方法文档字符串（''' '''） def fn(a:int,b:str="hellow")->str """这是文档字符串"""
   
   作用域：
   
   局部作用域修改全局使用global 变量
   
   命名空间：
    loacls() 获取当前命名空间中所有数据
    globals() 获取全局命名空间
    
  递归：
     def jc(n) :
    '''阶乘递归'''
    # 基线条件
    if n == 1 :
        return 1
    # 递归条件
    else:
        return n * jc(n-1)

# print(jc(5))
def power(n,i):
    '''幂运算'''
    # 基线条件
    if i == 1:
        return  n
    # 递归条件
    else:
        return n*power(n,i-1)


# print(power(6,2))

def hw(str):
    '''检查字符串是否是回文'''
    # 基线条件
    if len(str) < 2:
        return True
    elif str[0] != str[-1]:
        return False
    # 递归条件
    else:
        return hw(str[1:-1])

print(hw('sssssssssssssadfdsssssssssss'))


  函数式编程：
    
    高阶函数：把函数作为参数传递
      filter()过滤序列 filter(lambda a,b: a+b, value) 
      map()可以对对象进行制定操作后返回 map(lambda i : i+1, value)
      匿名函数 lambda 参数列表 ：返回值
      l.sort(key=len), l.sort(key=int)
      sorted()可以对任意序列进行排序，不会影响原来的对象; sort只能对列表排序
      
      闭包
        1.函数嵌套
        2.将内部函数作为返回值返回
        3.内部函数使用到外部函数变量
  
      装饰器方法
       @装饰器方法
    
    
