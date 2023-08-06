# Python-23-
Python学习笔记()
# p74 集合的数据操作
#(1)交集
s1={10,20,30,40}
s2={20,30,40,50,60}
print(s1.intersection(s2))  #输出为：20,30,40 注意这里是无序的
print(s1&s2)  #intersection()与&等价，交集操作

#(2)并集操作
print(s1.union(s2))
print(s1|s2)  #union与|等价，并集操作

#(3)差集操作
print(s1.difference(s2))  #  a-b集合，输出为10

#(4)对称差集
print(s1.symmetric_difference(s2))
print(s1 s2)  #输出为10，50，60



# p75 集合生成式
#列表生成式
lst=[i*i for i in range(6)]
print(lst)

#集合生成式
lst={i*i for i in range(6)}
print(lst)



# p76 字符串的创建与驻留机制
#字符串的驻留机制
a='Pyhon'
b="Python"
c='''Pyhon'''
print(a,id(a))
print(b,id(b))
print(c,id(c))  #这些id都相同
#Python的驻留机制对相同的字符串只保留一份拷贝，后续创建相同字符串时，不会开辟新的空间，而是把该字符串的id赋给新创建的变量
#符合驻留机制的条件(交互模式)
#1.字符串长度为0或1
#2.符合标识符的字符串
#3.字符串只在编译阶段时进行驻留，而非运行时
#4.[-5,256]之间的整数数字

#驻留的优点：提升效率、节约内存

#在进行字符串相加时，建议使用join而非+,因为join他只new一次对象，效率更高
