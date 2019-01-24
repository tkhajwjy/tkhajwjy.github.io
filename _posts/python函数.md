
# Map

map将一个函数apply到`list_of_inputs`输入列表的所有元素上

`map(function,list_of_inputs)`


```python
items = [1,2,3,4,5]
s = list(map(lambda x:x**2,items))
s
```




    [1, 4, 9, 16, 25]



lambda经常配合map使用


```python
def squared(x):
    return x**2
s1 = list(map(squared,items))
s1
```




    [1, 4, 9, 16, 25]




```python
def multiply(x):
    return (x*x)
def add(x):
    return (x+x)
funcs = [multiply,add]
for i in range(5):
    value = map(lambda x:x(i),funcs)
    print(list(value))
```

    [0, 0]
    [1, 2]
    [4, 4]
    [9, 6]
    [16, 8]


# Filter

filter 过滤


```python
number_list = range(-5,5)
less_than_zero = filter(lambda x:x<0,number_list)
list(less_than_zero)
```




    [-5, -4, -3, -2, -1]



# Reduce

对列表进行一些计算并且返回结果，比如列表数的连乘、连加


```python
from functools import reduce
sum = reduce((lambda x,y:x+y),[1,2,3,4])
sum
```




    10



[书籍地址《python进阶》](https://github.com/eastlakeside/interpy-zh)