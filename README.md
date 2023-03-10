# plotCSVbyEcharts
## 一句话介绍
To plot test data in a multi yAxis chart from a *.CSV format file, with Apache Echarts.
## 起因
做机械试验台架测试，试验机会生成测试数据，需要将试验数据可视化，生成图表。python,matlab都需要装软件，而测试数据结构都比较简单，而且要生成的图表格式也比较固定，所以也不用到像matlab或基于python的matplotlib等比较高级的可视化工具。而百度的Echarts,只需要一个最小js文件，有google内核的浏览器就可以一键生成了。


# 要处理什么样的数据  
* 机械试验设备，测试数据以CSV格式保存
* CSV前几行是测试相关信息，但不一定有注释行的标识
* 试验开始，结束，中间暂停、中断继续会纪录为单独的信息行，在数据行的开始、结尾和中间
* 数据行为时序排列，即在传感器每多采集一次数据就在数据里新增加一行
* 列数可能是固定的，也可能是根据试验人员指定生成
* 通常前几列会包涵时间、时长、测试步等信息；剩余不同列对应不同传感器纪录的数据
* 时间或测试步通常会作为图表的x轴的值，而不同传感器纪录的数据会对应不同的y轴绘于图中

# 需要什么工具
* 文本编辑，微软记事本，notepad++等都可以
* google内核的浏览器
* 百度Echarts的一个[js文件](https://github.com/apache/echarts/blob/2e1fbbefabafa5bd2c4698aa705490d5c64aec18/dist/echarts.min.js)

# 可视化图表的效果
* 一个多y轴的多曲线图
* 横轴为时间
* 有多个纵轴，对应不同类型的数据

# 使用方法
* 把百度Echarts的一个[js文件](https://github.com/apache/echarts/blob/2e1fbbefabafa5bd2c4698aa705490d5c64aec18/dist/echarts.min.js)和这个html文件放在同一目录下，在html中指向这个[js文件](https://github.com/apache/echarts/blob/2e1fbbefabafa5bd2c4698aa705490d5c64aec18/dist/echarts.min.js)
* 用浏览器打开文件
* 打开要可视化的数据，曲线自动生成
* 点保存可生成曲线图片
