2.1.4 举例

wc.exe -s -a *.c

返回当前目录及子目录中所有.c 文件的代码行数、空行数、注释行数。

wc.exe -s -a –c -w *.c–e stop.txt –o output.txt

返回当前目录及子目录中所有.c 文件的字符数、单词总数、代码行数、空行数、注释行数，并将结果保存在output.txt中，且统计单词时忽略stop.txt中的单词。

2.1.5 输出结果的格式

输出结果格式形如：

[文件名], [统计标志]: [总数]
举例如下：

wc.exe –c file.c，则输出结果保存在result.txt中，内容格式如下（注意大小写）：

file.c, 字符数: 50

wc.exe –w file.c，则输出结果保存在result.txt中，内容格式如下（注意大小写）：

file.c, 单词数: 30

wc.exe –l file.c，则输出结果保存在result.txt中，内容格式如下（注意大小写）：

file.c, 行数: 10

 如果同时涉及多项统计，如同时需要统计字符、单词和行数，则按照字符-->单词-->行数-->代码行数/空行数/注释行的顺序，依次分行显示。显示顺序与输入参数的次序无关。例如：

wc.exe –l –c file.c，则统计file.c中的字符数和行数，输出结果保存在result.txt中，内容格式如下：

file.c, 字符数: 50

file.c, 行数: 10

 例如：

wc.exe -s -a –c -w *.c–e stop.txt –o –output.txt

输出结果保存在output.txt中，内容格式为：

file1.c, 字符数: 50

file1.c, 单词数: 30

file1.c, 代码行/空行/注释行: 5/2/3

file2.c, 字符数: 40

file2.c, 单词数: 26

file2.c, 代码行/空行/注释行: 6/2/1# wc
