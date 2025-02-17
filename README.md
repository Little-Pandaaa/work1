# Linux
## vim (Nano)学习
首先是关于Ubuntu终端的一些命令。ls为查看当前目录下的文件夹，cd+文件名为进入每一个文件，rm+文件名为删除文件，cd ..返回到上一级目录，mkdir+目录为创建。vim test.c创建（打开）一个文件。  
**vim编辑器的常用命令**：  
插入模式：i（光标前），I（当前行的第一个非空白符前），a（光标后插入），A（当前行的末尾插入），o（打开新的一行插入），O（当前行的上方打开新的一行）  
跳转：gg文件第一行，G文件最后一行，nG文件第n行  
esc退出插入模式，进入命令模式  
删除：x删除当前光标下的字符，dw删除一个词，dd删除一行，d$删除光标到行尾，d0删除光标到行首（不包括行首空格）  
复制：yy复制当前行，yw复制一个词，p粘贴  
u撤销，Ctrl+r撤销“撤销”操作  
/test从光标向后搜索，？test从光标向前搜索test字符串，n重复向前搜索，N重复向后搜索  
J当前行与下一行合并  
**Nano**  
alt+6复制一整行，CTRL+u粘贴  
##ssh远程连接服务器  
安装openssh-server,ifconfig查看地址，sudo systemctl status ssh检查ssh服务器状态（active），**问题**防火墙sudo ufw status的结果一直是不活跃，但好像没影响，ssh username@ip进行远程连接，输入密码，看到![image](https://github.com/user-attachments/assets/77824fac-01f3-41cb-a349-0e8b2fc78594)
exit退出连接

##Linux命令行基本操作  
#列出当前目录下所有文件和目录  
ls
#复制文件到目录dest  
cp filename.txt dest/  
#重命名文件  
mv oldname.txt newname.txt  
#删除文件
rm filename.txt
#新建文件
touch filename.txt
#查看文件
cat filename.txt
#搜索文件中的内容
grep pattern example.txt
#打开一个文件
cd filename  
#回到上一级  
cd ..
#创建目录
mkdir newdir  
#切换到另一个目录
cd dirname  
#删除一个空目录
rmdir dirname
#屏幕上显示hello  
echo "hello"  
[image][.(https://www.runoob.com/wp-content/uploads/2015/02/011500266295799.jpg).  

#SLAM
##世界坐标系，相机坐标系，像素坐标系转换关系  
**世界坐标系**是一个用于描述真实世界中物体位置的参考坐标系。它是一个全局性的、固定的坐标系统，用于确定场景中所有物体的绝对位置和方向。  
  （全局性：它是一个全局性的坐标系统，能够描述场景中的所有物体。   
    固定性：相对于其他坐标系（如相机坐标系、像素坐标系等），世界坐标系是固定的，不会随着观察者的移动而改变。  
    三维性：世界坐标系通常是三维的，能够描述物体在三维空间中的位置和方向。  
    单位：世界坐标系的单位通常是实际度量单位，如米（m）、厘米（cm）等，这使得我们可以更直观地理解物体之间的相对位置和距离。）  
**相机坐标系**是一个以相机的光心（也称为镜头中心或投影中心）为原点的三维坐标系统。这个坐标系统用于描述物体相对于相机的位置和方向。  
  （原点位于相机的光心，即镜头的物理中心。  
    Z轴通常与相机的观察方向一致，指向相机前方，也就是从相机光心到场景中物体的方向。  
    X轴和Y轴则定义在相机的成像平面上，通常与相机的传感器平面平行。这两个轴确定了图像的水平和垂直方向。）    
**像素坐标系**是一个二维的直角坐标系统，它用于描述数字图像中每个像素的位置。  
  （原点通常位于图像的左上角。这意味着图像的左上角被定义为坐标(0, 0)。  
    X轴沿着图像的水平方向（从左到右）延伸。  
    Y轴沿着图像的垂直方向（从上到下）延伸。  
    每个像素在像素坐标系中都有一个唯一的坐标，该坐标由两个整数组成，分别代表像素在X轴和Y轴上的位置。这些坐标值通常以像素为单位进行测量。）    
1.世界坐标系转换到相机坐标系    
  世界坐标系到相机坐标系，需要先旋转对齐，再平移回去。旋转的表示有很多种，旋转矩阵，欧拉角，四元数，轴角，李群与李代数  
  ![image](https://github.com/user-attachments/assets/8fddc097-9db5-4fb4-a54a-dae9f9541f6e)
  ![image](https://github.com/user-attachments/assets/98c4caa6-3c6c-49d5-b70a-7818a72aec7c)  
  旋转矩阵R（3x3）描述相机的旋转。
  平移向量T（3x1）描述相机在世界坐标系中的位置。
  转换公式为：P_c = R * (P_w - C)，其中P_c是相机坐标系中的点，P_w是世界坐标系中的点，C是相机在世界坐标系中的位置。
*世界坐标系与相机坐标系的关系就是相机的外参*
2.相机坐标系转换到像素坐标系
![image](https://github.com/user-attachments/assets/3c48d01a-7f9e-43fe-9260-d9d7253a39a0)
![image](https://github.com/user-attachments/assets/fbb890d8-0a4d-46b4-8acb-85f2204e942b)
![image](https://github.com/user-attachments/assets/881bad6f-7adb-4059-a9cc-0aca009b0308)





