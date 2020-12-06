# Matplotlib折线图绘制
- 注：matplotlib不支持中文字体，但可以使用如下方法修改
- 还有echarts，plotly等在线数据图形工具(很好看)
```python
import matplotlib.pyplot as plt
import matplotlib

font = {'family': 'MicroSoft YaHei',
        'weight': 'bold',
        'size': 20}
matplotlib.rc("font", **font)
# 这是一个全局方法，当然还有其它方法，这个比较省事儿
```
### 1、最基础的折线图
```python
import matplotlib.pyplot as plt
import random

x = range(2, 26, 2)
y = [random.randint(2, 20) for x in range(12)]

plt.plot(x, y)
plt.show()
```
### 2、设置折线图大小、像素密度
```python
import matplotlib.pyplot as plt
import random

fig = plt.figure(figsize=(28, 10), dpi=80)
# figsize -> 图片大小
# dpi -> 像素密度
plt.savefig('路径名')
# 保存路径
```
### 3、设置图片的x,y轴的步长，刻度取名，x,y轴的含义，表头等
```python
import matplotlib.pyplot as plt
import random

plt.xticks(range(2, 25))
# 设置x轴的步长
# 同理使用yticks可以设置y轴步长
```
```python
import matplotlib.pyplot as plt
import random

x = range(2, 26, 2)
y = [random.randint(2, 20) for x in range(12)]

x_label = ['名字{}'.format(i) for i in range(2, 26)]
# 中文刻度不显示，最上边有修改方法
plt.xticks(x, x_label)
# 将x轴设置上特殊名称
# 另外，xticks()的rotation=30参数可以将x的刻度旋转30°
```
```python
import matplotlib.pyplot as plt

plt.xlabel('xxx')   # x轴含义解释
plt.ylabel('yyy')   # y轴含义解释
plt.title('ttt')    # 设置表头
```
### 4、折线图网格，同时绘制多条折线，图例
```python
import matplotlib.pyplot as plt

plt.grid()  # 设置网格，疏密程度由xticks和yticks的步长确定
```
```python
import matplotlib.pyplot as plt
import random

x = range(2, 26, 2)
y_1 = [random.randint(2, 20) for x in range(12)]
y_2 = [random.randint(2, 20) for x in range(12)]

plt.plot(x, y_1, label='折线1')
plt.plot(x, y_2, label='折线2')
plt.legend()  # 添加图例

plt.show()
# 绘制多条折线
```
# Matplotlib散点图绘制
```python
import matplotlib.pyplot as plt
import random
import matplotlib

fig = plt.figure(figsize=(28, 10), dpi=80)

font = {'family': 'MicroSoft YaHei',
        'weight': 'bold',
        'size': 20}
matplotlib.rc("font", **font)

y_3 = [random.randint(3, 17) for i in range(0, 31)]
y_10 = [random.randint(25, 35) for j in range(0, 31)]

x = range(0, 31)
plt.scatter(x, y_3)
plt.scatter(x, y_10)

plt.show()

# 其它的美化方法和折线图相同
```
# Matplotlib条形图
```python
import matplotlib.pyplot as plt
import matplotlib

fig = plt.figure(figsize=(28, 10), dpi=80)

font = {'family': 'MicroSoft YaHei',
        'weight': 'bold',
        'size': 20}
matplotlib.rc("font", **font)

x = ['张三', '李四', '王五']
y = [77,66,88]

plt.bar(x, y)
plt.show()

# 其它美化方法和折线图相同
```
