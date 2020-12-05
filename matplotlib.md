# Matplotlib绘图
- 注：matplotlib不支持中文字体，但可以使用如下方法修改
```python
import matplotlib.pyplot as plt
import matplotlib

font = {'family': 'MicroSoft YaHei',
        'weight': 'bold',
        'size': 20}
matplotlib.rc("font", **font)
```
## 1、最基础的折线图
```python
import matplotlib.pyplot as plt
import random

x = range(2, 26, 2)
y = [random.randint(2, 20) for x in range(12)]

plt.plot(x, y)
plt.show()
```
## 2、设置折线图大小、像素密度
```python
import matplotlib.pyplot as plt
import random

fig = plt.figure(figsize=(28, 10), dpi=80)
# figsize -> 图片大小
# dpi -> 像素密度
plt.savefig('路径名')
# 保存路径
```
## 3、设置图片的x,y轴的步长，刻度取名
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
