# work1
## vim 学习
首先是关于Ubuntu终端的一些命令。ls为查看当前目录下的文件夹，cd+文件名为进入每一个文件，rm+文件名为删除文件，cd ..返回到上一级目录，mkdir+文件名为创建。vim test.c创建（打开）一个文件。
vim编辑器的常用命令：
插入模式：i（光标前），I（当前行的第一个非空白符前），a（光标后插入），A（当前行的末尾插入），o（打开新的一行插入），O（当前行的上方打开新的一行）
跳转：gg文件第一行，G文件最后一行，nG文件第n行
esc退出插入模式，进入命令模式
删除：x删除当前光标下的字符，dw删除一个词，dd删除一行，d$删除光标到行尾，d0删除光标到行首（不包括行首空格）
复制：yy复制当前行，yw复制一个词，p粘贴
u撤销，Ctrl+r撤销“撤销”操作
/test从光标向后搜索，？test从光标向前搜索test字符串，n重复向前搜索，N重复向后搜索
J当前行与下一行合并
