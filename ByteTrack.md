# ByteTrack :Multi-Object Tracking by Associating Every Detection Box

## Introduce

### 传统方法存在的缺陷

​		SOTA需要处理真阳性和假阳性检测框以消除低置信度的检测框，但是低置信度检测框有时表明了物体存在（被遮挡的物体），简单过滤低置信度检测框会造成轨迹丢失，但是如果考虑每一个检测框，会引入背景，造成更多假阳性误报。

### 本文提出的改进支持

​		**轨迹的相似度提供了区别背景和目标的信息**

​		1、对于高分的检测框，采用卡尔曼滤波预测轨迹下一帧的位置，利用**IoU特征（运动相似度）**或者**Re-ID（外观相似度）**特征计算预测框和检测框之间的相似度；

​		2、对于没有匹配的轨迹(遮挡、运动模糊或者尺寸变化)和低分检测框，利用**运动相似度**进行二次匹配。

****

## Related Work

## BYTE（Association Method）

![屏幕截图 2023-10-24 155905](C:\Users\zhangbo\Pictures\Screenshots\屏幕截图 2023-10-24 155905.png)

![ByteTrack_Algorithm](E:\Papers\ByteTrack\ByteTrack_Algorithm.png)

## Experiments



## Conclusion

