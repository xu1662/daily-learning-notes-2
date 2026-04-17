# 我的每日学习记录

## 📅 2026年4月9日

**📖 今天学了什么**
- 学会了在 GitHub 上创建 README.md 文件
- 了解了 Markdown 的基本语法
- 线性代数第一章一小节

**💻 代码/笔记**
- Markdown 的基本语法
# 一级标题（最大）
## 二级标题
### 三级标题
#### 四级标题

- 无序列表
- 香蕉
  - 子项目（前面加两个空格）

- 有序列表
1. 第一步
2. 第二步
3. 第三步

**加粗文字**
*斜体文字*
***加粗斜体***

[百度](https://baidu.com)

![我的截图](https://github.com/xxx/screenshot.png)
在 GitHub 编辑框里，直接拖拽图片进去会自动上传并生成链接。

> 这是一段引用文字
> 可以写多行

---

- 代码块


1 ```python
2 print("Hello World")
3 def add(a, b):
4     return a + b


- 三个反引号后面可以加语言名称（python、javascript、bash等），会有语法高亮。


- 用 Python 写一个快速排序


      1 def quick_sort(arr):
      2     if len(arr) <= 1:
      3         return arr
      4     
      5     pivot = arr[len(arr) // 2]
      6     left = [x for x in arr if x < pivot]
      7     middle = [x for x in arr if x == pivot]
      8     right = [x for x in arr if x > pivot]
      9     
     10     return quick_sort(left) + middle + quick_sort(right)
     11 
     12 
     13 # 示例
     14 arr = [3, 6, 8, 10, 1, 2, 1]
     15 print(quick_sort(arr))  # [1, 1, 2, 3, 6, 8, 10]

第 1 行
def quick_sort(arr):

def	定义（define）的缩写，意思是"我要开始定义一个函数了"
quick_sort	函数的名字，叫"快速排序"
(arr)	括号里的 arr 是参数，意思是"这个函数需要你给它一个列表，这个列表暂时叫做 arr"
:	冒号，表示函数定义结束了，下面的缩进代码是函数要做的内容

第 2-3 行
    if len(arr) <= 1:
        return arr
（前面4个空格）	缩进，表示这几行代码属于上面的 quick_sort 函数
if	如果，表示一个条件判断
len(arr)	len 是长度（length），len(arr) 意思是"列表 arr 里面有几个元素"
<=	小于等于
1	数字一
:	冒号，表示如果条件成立，就执行下面缩进的代码
return	返回，意思是"把后面的东西作为结果送回去"
arr	就是原来的那个列表
整句翻译：如果这个列表的长度小于等于 1（也就是空的或者只有一个元素），那就直接把这个列表原样返回（因为它已经有序了，不用排）。

第 5 行
    pivot = arr[len(arr) // 2]
pivot	基准值，这是快速排序里的一个名字
=	赋值，把右边算出来的结果存到左边这个名字里
arr[...]	取列表中的某个位置的元素
len(arr) // 2	len(arr) 是列表长度，// 是整除（去掉余数），// 2 就是除以2取整数
比如长度是 7，7 // 2 = 3，取索引 3 的元素
整句翻译：找到列表中间位置的那个元素，把它叫做 pivot（基准）。

第 6 行
    left = [x for x in arr if x < pivot]
这是列表推导式，拆开看：
left	左边，这个名字表示"所有比基准小的元素"
=	赋值
[ ... ]	方括号表示要创建一个新列表
for x in arr	对于 arr 列表中的每一个元素，暂时把它叫做 x
if x < pivot	如果这个 x 小于 pivot（基准值）
<	小于号
整句翻译：从 arr 列表里，把每一个小于 pivot 的元素挑出来，放到一个叫 left 的新列表里。

第 7 行
    middle = [x for x in arr if x == pivot]
middle	中间，这个名字表示"所有等于基准的元素"
==	等于号（两个等号是比较是否相等，一个等号是赋值）
整句翻译：从 arr 列表里，把每一个等于 pivot 的元素挑出来，放到一个叫 middle 的新列表里。

第 8 行
    right = [x for x in arr if x > pivot]
right	右边，这个名字表示"所有大于基准的元素"
>	大于号
整句翻译：从 arr 列表里，把每一个大于 pivot 的元素挑出来，放到一个叫 right 的新列表里。

第 10 行
    return quick_sort(left) + middle + quick_sort(right)
return	返回
quick_sort(left)	调用 quick_sort 函数，把 left 列表传给它排序（这就是递归，自己调用自己）
+	加号，这里是拼接的意思，把三个列表连成一个
middle	中间的那个列表（已经是排好序的，因为所有值都相等）
quick_sort(right)	调用 quick_sort 函数，把 right 列表传给它排序
整句翻译：先把左边的部分排序，再把中间的部分（已经有序）放中间，再把右边的部分排序，最后把这三部分拼接成一个完整的列表返回。

第 13 行
# 示例
#	井号，后面写的是注释，给人看的，计算机不执行

第 14 行
python
arr = [3, 6, 8, 10, 1, 2, 1]
arr	变量名，我们叫它"数组"或"列表"
=	赋值
[3, 6, 8, 10, 1, 2, 1]	一个列表，里面有 7 个数字：3,6,8,10,1,2,1

第 15 行
print(quick_sort(arr))
print	打印，意思是把结果显示在屏幕上
(...)	括号，print 要打印的东西写在里面
quick_sort(arr)	调用快速排序函数，把 arr 传进去排序
整句翻译：把 arr 这个乱序的列表排好序，然后把结果打印出来。

🎬 完整翻译
text
定义 一个叫"快速排序"的 函数，它需要一个 列表：
    如果 这个列表 的 长度 小于等于 1：
        直接 返回 这个列表
    
    找到 这个列表 中间位置的元素，叫它"基准"
    
    创建 一个叫"左边"的列表 = 从原列表中 挑出 所有 小于 基准的 元素
    创建 一个叫"中间"的列表 = 从原列表中 挑出 所有 等于 基准的 元素
    创建 一个叫"右边"的列表 = 从原列表中 挑出 所有 大于 基准的 元素
    
    返回 = 对"左边"进行快速排序 后，再 拼接上"中间"，再 拼接上 对"右边"进行快速排序 的结果

例子：
    创建一个列表，里面有：3,6,8,10,1,2,1
    打印 对这个列表 进行快速排序 的结果


