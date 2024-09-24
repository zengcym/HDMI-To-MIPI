# HDMI驱动MIPI屏幕

基于稚晖君HDMI-PI项目的东芝TC358870XBG方案，他本人做出了龙迅方案，但代码是没有开源的，而东芝方案有一版硬件，软件没有进行相关调试。开源链接：https://github.com/peng-zhihui/HDMI-PI

# 软硬件
![image](https://github.com/zengcym/HDMI-To-MIPI/blob/main/Images/HDMI%20to%20MIPI_v1.JPG)
PCB文件使用Pads 9.5 Layout。
>
项目的硬件部分参考了稚晖君的原理图，PCB部分同样采用核心板加转接板的方式，这样可以灵活匹配不同接口的显示屏，同时严格按原版接口和控制脚位定义，方便不同版本软硬调试应用。
>
增加了音频部分，板上放置了一个3W单声道CLASS-D功放，现在有声音了。
>
硬件已经经过排雷和验证，更新到v1，修改了一些手工焊接不方便的地方，比如IC和FPC座引脚上大面积地铜箔的分割，预留了外接按键或者扩展的接口，相信没有大的功能改进的情况下，这是最终的版本了。
>
文档含很多艰难收集和整理更新的资料，可供参考。
>
点亮的屏幕：
>
LT070ME05000       7寸        1200*1920
>
ILI9881C+BOE     10.1寸       800*1280
>
BV050HDM-N00       5寸        720*1280
>
TV080WUM-NL0       8寸        1200*1920
>
TV101WUM-NM0     10.1寸       1200*1920
>
P101KDA-AB0      10.1寸     1200*1920 （转接板同TV101WUM-NM0）
>
>2021.8.16 更新
>
>修改PCB版本到V2,EA3036更改为SOT23-5封装3路独立DC-DC（封装相同，FB为0.6V都可以使用），8Mhz晶振和48Mhz有源晶振封装修改为常规3225封装，同时预留STM32的MCO，通过调整代码有机会省掉48Mhz有源晶振。 
>
>2021.5.31 更新
>
>增加JDI 7寸 LT070ME05000屏软硬件及相关资料
>
>2021.5.18 更新
>
>增加一款国产10.1屏软硬件及相关资料
>
>2021.3.31 更新
>
>软件
>
>所有代码更新休眠唤醒状态
>
>2021.3.29 更新
>
>软件
>
>更新P101KDA-AB0 配合v1版本转接板 实现休眠和插拔HDMI线待机和唤醒.hex 
>
>2021.3.27 更新
>
>硬件
>
>TV101WUM-NM0(P101KDA-AB0)和TV080WUM-NL0 转接板PCB更新为v1版本，增加LCDVCC 3.3V PMOS关断电路，因为调试发现上电时序需要配合关断屏的供电，否则会出现休眠闪屏问题。
>
>BV050HDM-N00 因为屏供电的DC-DC在转接板上，所以不需要做更改。
>
>软件
>
>更新TV101WUM-NM0 配合v1版本转接板 实现休眠和插拔HDMI线待机和唤醒.hex


# 方案不足
方案不支持HDMI不同分辨率缩放适应及竖屏转横屏，只能作为树莓派或者电脑系统副屏使用,使用面略窄。

# 交流学习
QQ群：879256453 欢迎交流学习
