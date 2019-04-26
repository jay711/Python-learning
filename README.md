## 常用函数的用法
### sort()和sorted()函数
    sort是应用在list上的方法，sorted可以对所有可迭代的对象进行排序操作。
    list的sort方法返回的是对已存在的列表操作后的结果，而内建函数sorted方法返回的是一个新的list，而不是在原来的基础上进行的操作。
    sorted用法：sorted(iterable,cmp=None,key=None,reverse=False)
    sort用法：sort(cmp=None,key=None,reverse=False)
   <https://www.cnblogs.com/brad1994/p/6697196.html>
### str.isalpha()和str.lower()函数,str.upper()函数
    str.isalpha()：检测字符串是否只由字符组成，如果字符串至少有一个字符并且所有字符都是字母则返回 True,否则返回 False。
    str.lower()：转换字符串中所有大写字符为小写
    str.upper()：转换字符串中所有小写字符为大写
### enumerate()函数
    如果对一个列表，既要遍历索引又要遍历元素时，首先可以这样写：
```python
list1 = ["这", "是", "一个", "测试"]
for i in range (len(list1)):
    print (i,list1[i])
```
    用enumerate()函数，可以写成：
```python
list1 = ["这", "是", "一个", "测试"]
for index,item in enumerate(list1):
    print(index,item)
```
    enumerate 还可以接收第二个参数，用于指定索引起始值.
### join()函数
    语法：  'sep'.join(seq)
    参数说明
    sep：分隔符。可以为空
    seq：要连接的元素序列、字符串、元组、字典
    上面的语法即：以sep作为分隔符，将seq所有的元素合并成一个新的字符串
    返回值：返回一个以分隔符sep连接各个元素后生成的字符串
### index()函数
    index()函数的完整语法是这样的：
    str.index(str, beg=0, end=len(string))
    str – 指定检索的字符串 
    beg – 开始索引，默认为0。 
    end – 结束索引，默认为字符串的长度。
### bin()函数
    是将整型转换为二进制数组成的字符串，注意它的结果是个字符串，
    且转换后的最高位非零（如bin（1）=‘0b1’，而非‘0b01’），并在前面加上0b，表示这是一个二进制
    括号中需要是一个整型，或者括号中返回一个整型。
    bin(0)-0b0;
    bin(1)-0b1;
    bin(2)-0b10;
    bin(4)-0b110
### replace()函数
    replace() 方法把字符串中的 old（旧字符串） 替换成 new(新字符串)，如果指定第三个参数max，则替换不超过 max 次。
    语法
    replace()方法语法：
    str.replace(old, new[, max])
    参数
    old -- 将被替换的子字符串。
    new -- 新字符串，用于替换old子字符串。
    max -- 可选字符串, 替换不超过 max 次
    返回值
    返回字符串中的 old（旧字符串） 替换成 new(新字符串)后生成的新字符串，如果指定第三个参数max，则替换不超过 max 次。
### rjust()函数
    rjust() 返回一个原字符串右对齐,并使用空格填充至长度 width 的新字符串。如果指定的长度小于字符串的长度则返回原字符串。
    str.rjust(width[, fillchar])
    width -- 指定填充指定字符后中字符串的总长度；
    fillchar -- 填充的字符，默认为空格。
