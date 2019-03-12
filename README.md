# EasyStereoCamera
这是一个入门的程序，仅限于测试使用，更深入的学习，请自行学习相关理论

使用说明：
1、自行度娘安装OPENCV4.0
2、自行安装VS2015企业版
3、解压源代码EasyStereoCamera.rar
4、运行ConsoleApplication3.sln打开项目工程，如遇到问题，应该是环境配置问题，请
   根据自己的实际环境排查
5、GetImages是用来采集图像的程序
   标定板摆好一个位置后点击一下键盘S键即可采集一次左右图像；
   总共会采集15次，供30张图片
   图片位于imgs文件夹下
6、SingleCalib是单目标定程序，为了方便使用，我已经将程序里的L和R分别编译成两个不同的程序，
   执行SingleCalibL可获得L.XML（镜头的内参及畸变参数等数据）    
   执行SingleCalibR可获得R.XML（镜头的内参及畸变参数等数据）
7、Calib3D是双目标定程序，运行之后可获得 extrinsics.yml和 intrinsics.yml文件 供后续 BM匹配程序使用
8、解压pythonBM程序.rar
9、 将7中获得的 extrinsics.yml和 intrinsics.yml 复制到 次目录中
    将内参参数文件里的参数节点名称依次改为ML ，DL，MR，DR
10、在自己的python开发环境中打开 StereoBM.py
11、运行程序，正常应该就能看到原始左右目图片、校正对齐之后的图像以及深度图
12、调节NUM 和block参数至合适数值
13、用鼠标点击深度图中的不同位置，其对应的空间坐标数据就会显示在输出窗口上

好了，就这么多了，祝大家玩得开心
