# ESP32_printer_miaomiaoji

基于esp32的热敏打印机


原理图及pcb见：https://oshwhub.com/blueskyer/re-min-da-yin-jiv3-0   

QQ技术群：801516857

arduino库文件需要更新一下
解压Mao喵喵机修改库.zip，将此文件夹内的BluetoothSerial文件夹复制到C:\Users\你的用户名\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.6\libraries进行覆盖。
覆盖之前把原本的BluetoothSerial文件夹备份一下。

原理图基于V1，增加了一个按键走纸功能，其他无变化
pcb上就新增一个按键，一个电阻和一个电容，其他无变化。
程序使用文件夹内的，也是基于V1版本程序，加了按键走纸功能

注意：立创eda上原理图和PCB图都不要导入更新，以免封装有变化造成线路异常，直接使用即可。


特别重要：
1，esp32一定要买esp32 wrover e类型的，4m或者8m都行，其他型号未测试过不保证没问题。
2，上传代码时，需要先用镊子等工具将boot引脚接地，再连上usb转ttl上电，不然没法进入下载模式，上传完后断开。


其他：

1，元器件注意根据原理图进行购买，不要一键购买，特别是电阻和电容等经常被错误识别成其他商品
图中的pt4056其实就是tp4056
2，fpc的座子不要焊接反了
3，BR8205其他渠道购买注意是6p的，不要买8p的
4，如果用的带保护电路的18650或者锂电池，电池保护电路部分的元器件不要焊接
5，电池一定不要接反了，否则可能会烧毁线路。防止反接的话，tp4056可以换tp4056x。
6，元器件不要买重复了，蜂鸣器买1个就行，S8050和S8050J3Y是一个东西
7，如果用的186502p，X8821WV-02K-N0SN 这个接线端子不用购买，这是给锂电池包用的。

8，ss34二极管，有白色线的一端是负极
9，排针，只用焊接4个就行了，3.3V,GND,RX,TX
10，需要订货的元器件尽量换成同样值的其他型号，订货时间是不确定的

 

不匹配的一些东西这里罗列一下

1u R0603，这个是电容 1uf，0603规格的，而不是默认识别的什么USB头

330 R0603，这个是电阻，0603规格的，而不是什么电感

3.3uh，这个是3.3uh的电感，找这个值的电感去买，不要用默认匹配的22uh的电感，根本就不同。

 

高清视频见：https://www.bilibili.com/video/bv1WA411F73D

欢迎点赞和收藏

 

华丽丽的分割线------------------------------------------------------------------------------------------------------------------------------------------------------

 

20210915更新

1，修正原理图，需要元器件的bom表的根据原理图进行配件即可，不要用pcb的bom表。除了18650电池盒外，其他类型全部匹配不会再有元器件错误了，有的可能没现货了，需要你自己调整一下同值型号即可。（pcb没改是因为变更太多，布线什么的会出问题，所以尽量不动，打板还是直接打pcb即可）

 

 

 

20210928更新

1，增加了3d外壳

2，购买元器件直接参考“立创商城购物车详情.xls”里面内容即可，不再有类型错误重复之类的问题
