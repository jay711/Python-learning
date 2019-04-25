## 字符串排序
### 1.编写一个程序，将输入字符串中的字符按如下规则排序(一个测试用例可能包含多组数据，请注意处理)。
    规则 1 ：英文字母从 A 到 Z 排列，不区分大小写。如，输入： Type 输出： epTy
    规则 2 ：同一个英文字母的大小写同时存在时，按照输入顺序排列。如，输入： BabA 输出： aABb
    规则 3 ：非英文字母的其它字符保持原来的位置。如，输入： By?e 输出： Be?y 
    样例：
    输入：
    A Famous Saying: Much Ado About Nothing(2012/8).
    输出：
    A aaAAbc dFgghh : iimM nNn oooos Sttuuuy (2012/8).
### 代码实现
```python
def f(s):
    a,L = [],len(s)
    for i in range(L):
        if s[i].isalpha():  # 检测字符串是否只由字符组成，如果字符串至少有一个字符并且所有字符都是字母则返回 True,否则返回 False
            a.append((s[i], s[i].lower(), i))  # str.lower():转换字符串中所有大写字符为小写
    b = sorted(a, key=lambda x:(x[1], x[2], x[0])) # a:可迭代对象；按x(1)来排序
    result = ''
    for i in range(L):
        if s[i].isalpha():
            result += b[0][0]
            del b[0]
        else:
            result += s[i]
    return result
      
try:
    while 1:
        print(f(input()))
except:
    pass
