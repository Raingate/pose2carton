# Pose2Carton 

EE228 课程大作业，利用3D骨架控制3D卡通人物。



# Maya 环境配置

这里请简单描述你配置Maya环境的过程。



# 匹配流程

首先，对fbx文件作解析。调用fbx-parser将fbx文件分解为obj格式的mesh文件，以及包含skeleton关键点信息和其余点的受控信息(skin weight)。

然后，调用transfer.py脚本，第一次空缺匹配字典mapping，将main函数中transfer_one_sequence函数的传入参数分别改为parse出的.obj文件和obj-seq-5.pkl。运行后控制台会输出解析出的运动学树和各关键节点索引。利用这些索引，结合Blender中对关键点位置的查看，一一匹配卡通人物和human的关键点，匹配映射填入匹配字典，再次运行transfer.py脚本，可以得到447帧匹配结果，存储在3d_model文件夹中。 

随后，如果需要对蒙皮结果可视化，应该将表皮.png文件和.mtl文件一同放入3d_model文件夹中。  

最后，运行vis.py脚本，在Open3D视窗中会逐一播放匹配结果。播放完毕后关闭视窗，vis.py脚本将自动转换为.mp4文件，与每帧图像一起储存在vis文件夹下。  

这里请简单描述你熟悉/使用 匹配代码的流程，可以简述对代码的理解/各个函数作用等。



# 新增脚本说明

如果你写了自己的脚本来处理数据或进行可视化，请在这里进行相关说明(如何使用等)； 如果没有，请忽略该模块。



# 项目结果

这里放置来自你最终匹配结果的截图， 如

![image](../img/pose2carton.png)





# 协议 
本项目在 Apache-2.0 协议下开源

所涉及代码及数据的最终解释权归倪冰冰老师课题组所有

Group xx
