---
layout: post
title: 办公自动化实战七天训练营笔记
date: 2019-01-13
tag: 学习笔记
---

# 第二天
- 解析器是与python程序在同一个目录的，名称比python多一个w选择pythonw.exe
- if 条件语句后面用冒号不是分号
- 中文括号不识别
- for 语句最后也用分号

![image.png](https://upload-images.jianshu.io/upload_images/10043074-71a8902452b56cef.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/10043074-c01d065c4b6738f1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 函数内部使用的变量只能在函数内部使用，不能在外部调用

![image.png](https://upload-images.jianshu.io/upload_images/10043074-1dba219581f4b46e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 安装第三方库到shell中运行pip 安装，但是报错不是系统指令

- 配置环境变量方法：https://jingyan.baidu.com/article/676629978bcd8054d41b8444.html


```
a = "abc"
b = 1
e = 3.454656546
f= input("请输入F的值")
# 梯形面积的计算函数def trapezoid_area(base_up,base_down,height):    
            area = (base_up + base_down) * height /2                               print(area)
 # xlrd 库 ：对excel 文档进行读取的库
 import xlrd
 xlsx = xlrd.open_workbook("d:7月下旬入库表.xlsx")
 
 trapezoid_area(base_up=3,base_down=2,height=4)
 trapezoid_area(base_up=3,base_down=4,height=2)
 trapezoid_area(3,2,5)
 
 print(type(str(b)))
 print(len(a))
 print(round(e,3))
 print(f)
 
 # 结果
请输入F的值11
10.0
7.0
12.5
<class 'str'>
3
3.455
11
进程已结束,退出代码0
```


- 第三方库使用


```
import xlrd
xlsx = xlrd.open_workbook("d:/7月下旬入库表.xlsx")
# 使用 .sheet_by_index(0) 打开第一个工作表 
sheettable = xlsx.sheet_by_index(0)
# 使用 .cell_value(4,3) 打印第四行第三列的那个单元格
a = table.cell_value(4,3)
print(a)

#打印整个表里第2,4,5 列的每一行内容
for n in range (1, table.nrows):    
print(table.cell(n,1).value)    
print(table.cell(n,3).value)   
print(table.cell(n,4).value)

```


# 往excel写入内容


```
# xlutils能将xlrd.Book转为xlwt.Workbook，从而得以在现有xls的基础上修改数据，并创建一个新的xls，实现修改
from xlutils.copy import copy  
import xlrd
# 定义模板文件
tem_excel = xlrd.open_workbook("d:/日统计.xls")
# 定义新建文件
new_excel = copy(tem_excel)

# 定义要操作的表格
new_sheet = new_excel.get_sheet(0)
# 对表格执行写入指令，横坐标，纵坐标，值
new_sheet.write(2,1,12)
new_sheet.write(3,1,18)
new_sheet.write(4,1,33)
new_sheet.write(5,1,34)

# 保存为新的文件名称及路径
new_excel.save("d:/日统计改.xls")
```


# 统计excel表格中数据导出本地


```
from xlutils.copy import copy
import xlrd

xlsx = xlrd.open_workbook("d:/7月下旬入库表.xlsx")

table = xlsx.sheet_by_index(0)

all_data = []
for n in range(1,table.nrows):
    company = table.cell(n,1).value
    price = table.cell(n,3).value
    weight = table.cell(n,4).value

    data = (company,weight,price)
    all_data.append(data) # 向列表中添加一个元素

a_weight = []
a_total_price = []
b_weight = []
b_total_price = []
c_weight = []
c_total_price = []
d_weight = []
d_total_price = []

for i in all_data:
    if i[0] == "张三粮配":
        a_weight.append(i[1])
        a_total_price.append(i[1] * i[2])
    if i[0] == "李四粮食":
        b_weight.append(i[1])
        b_total_price.append(i[1] * i[2])
    if i[0] == "王五小麦":
        c_weight.append(i[1])
        c_total_price.append(i[1] * i[2])
    if i[0] == "赵六麦子专营":
        d_weight.append(i[1])
        d_total_price.append(i[1] * i[2])

tem_excel = xlrd.open_workbook("d:/统计表_模板.xls")
new_excel = copy(tem_excel)
new_sheet = new_excel.get_sheet(0)

new_sheet.write(2,1,len(a_weight))
new_sheet.write(2,2,round(sum(a_weight),2))
new_sheet.write(2,3,round(sum(a_total_price),2))
new_sheet.write(3,1,len(b_weight))
new_sheet.write(3,2,round(sum(b_weight),2))
new_sheet.write(3,3,round(sum(b_total_price),2))
new_sheet.write(4,1,len(c_weight))
new_sheet.write(4,2,round(sum(c_weight),2))
new_sheet.write(4,3,round(sum(c_total_price),2))
new_sheet.write(5,1,len(d_weight))
new_sheet.write(5,2,round(sum(d_weight),2))
new_sheet.write(5,3,round(sum(d_total_price),2))

new_excel.save("d:/xinbiaoge4.xls")
```


