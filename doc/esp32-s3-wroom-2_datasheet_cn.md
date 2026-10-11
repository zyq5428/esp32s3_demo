ESP32-S3-WROOM-2
技术规格书 版本 1.7

2.4 GHz Wi-Fi (802.11b/g/n) + 蓝牙 ® 5 模组
内置 ESP32-S3 系列芯片，Xtensa® 双核 32 位 LX7 处理器
Flash 最大可选 32 MB (Octal)，PSRAM 最大可选 16 MB (Octal)
33 个 GPIO，丰富的外设
板载 PCB 天线

ESP32-S3-WROOM-2

www.espressif.com

1 模组概述

1 模组概述

说明：

点击链接或扫描二维码确保您使用的是最新版本的文档：

https://www.espressif.com/documentation/esp32-s3-wroom-2_datasheet_cn.pdf

1.1 特性

CPU 和片上存储器

• 内置 ESP32-S3 芯片，Xtensa® 双核 32 位 LX7
微处理器（支持单精度浮点运算单元），支持高

达 240 MHz 的时钟频率

• 384 KB ROM

• 512 KB SRAM

• 16 KB RTC SRAM

• 最大 16 MB PSRAM

Wi-Fi

• 802.11b/g/n

• 802.11n 模式下数据速率高达 150 Mbps

• 帧聚合 (TX/RX A-MPDU, TX/RX A-MSDU)

• 0.4 µs 保护间隔

• 工作信道中心频率范围：2412 ~ 2484 MHz

蓝牙

• 低功耗蓝牙 (Bluetooth LE)：Bluetooth 5、

Bluetooth mesh

外设

• 33 个 GPIO

– 4 个作为 strapping 管脚

• SPI、LCD 接口、Camera 接口、UART、I2C、

I2S、红外遥控、脉冲计数器、LED PWM、全速
USB 2.0 OTG、USB 串口/JTAG 控制器、
MCPWM、SD/MMC 主机控制器、GDMA、
TWAI® 控制器（兼容 ISO 11898-1）、ADC、触摸
传感器、温度传感器、定时器和看门狗

模组集成元件

• 40 MHz 集成晶振

• 最大 32 MB Octal SPI flash

天线选型

• 板载 PCB 天线

工作条件

• 工作电压/供电电压：3.0 ~ 3.6 V

• 工作环境温度：–40 ~ 65 °C

• 速率支持 125 Kbps、500 Kbps、1 Mbps、2

认证

Mbps

• 广播扩展 (Advertising Extensions)

• 多广播 (Multiple Advertisement Sets)

• RF 认证：见 证书

• 环保认证：RoHS/REACH

• 信道选择 (Channel Selection Algorithm #2)

测试

• Wi-Fi 与蓝牙共存，共用同一个天线

• HTOL/HTSL/uHAST/TCT/ESD

乐鑫信息科技

2
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

1 模组概述

1.2 型号对比

ESP32-S3-WROOM-2 是通用型 Wi-Fi + 低功耗蓝牙 MCU 模组，具有丰富的外设接口，强大的神经网络运算能
力和信号处理能力，是专为人工智能和 AIoT 市场打造的一款模组，适用于多种应用场景，例如唤醒词检测和语
音命令识别、人脸检测和识别、智能家居、智能家电、智能控制面板、智能扬声器等。

ESP32-S3-WROOM-2 采用 PCB 板载天线，模组配置 ESP32-S3R8V 或 ESP32-S3R16V 芯片，可选 16/32 MB
flash、8/16 MB PSRAM。请注意，若开启 PSRAM ECC 功能，模组最大环境温度可以提高到 85 °C，但是
PSRAM 的可用容量将减少 1/16。

模组的系列型号对比如下表所示：

表 1-1. ESP32-S3-WROOM-2 系列型号对比

物料编号

Flash1, 2

PSRAM2

ESP32-S3-WROOM-2-N32R16V
32 MB (Octal SPI)
ESP32-S3-WROOM-2-N16R8V（停产） 16 MB (Octal SPI)
ESP32-S3-WROOM-2-N32R8V（停产） 32 MB (Octal SPI)

16 MB (Octal SPI)

8 MB (Octal SPI)

环境温度3

模组尺寸4

(°C)

(mm)

–40 ∼ 65

18.0 × 25.5 × 3.1

1 默认情况下，模组 SPI flash 支持的最大时钟频率为 120 MHz，且不支持自动暂停功能。
2 该模组使用封装在芯片中的 PSRAM。更多关于存储器规格的信息，请参考章节 6.5 存储器规格。
3 环境温度指乐鑫模组外部的推荐环境温度。
4 更多关于模组尺寸的信息，请参考章节 10 模组尺寸.

模组采用的是 ESP32-S3 系列芯片。芯片搭载 Xtensa® 32 位 LX7 双核处理器 (支持单精度浮点运算单元)，工作
频率高达 240 MHz。CPU 电源可被关闭，利用低功耗协处理器监测外设的状态变化或某些模拟量是否超出阈
值。

说明：

关于 ESP32-S3 的更多信息请参考 《ESP32-S3 系列芯片技术规格书》。

关于芯片版本识别、特定芯片版本的 ESP-IDF 支持版本以及其他芯片版本信息，请参考 《ESP32-S3 系列芯片勘误表》
> 章节 芯片版本标识。

1.3 应用

• 智能家居

• 工业自动化

• 医疗保健

• 消费电子产品

• 智慧农业

• POS 机

• 服务机器人

• 音频设备

乐鑫信息科技

• 通用低功耗 IoT 传感器集线器

• 通用低功耗 IoT 数据记录器

• 摄像头视频流传输

• USB 设备

• 语音识别

• 图像识别

• Wi-Fi + 蓝牙网卡

• 触摸和接近感应

3
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

目录

目录

1 模组概述
特性
1.1
1.2 型号对比
1.3 应用

2 功能框图

3 管脚定义
3.1 管脚布局
3.2 管脚描述

4.2

4 启动配置项
4.1 芯片启动模式控制
VDD_SPI 电压控制
ROM 日志打印控制
JTAG 信号源控制
4.4
4.5 芯片上电和复位

4.3

5 外设
5.1 外设概述
5.2 外设描述

5.2.1 通讯接口

5.2.1.1

5.2.1.2

5.2.1.3

UART 控制器
I2C 接口
I2S 接口
LCD 与 Camera 控制器

5.2.1.4
5.2.1.5 串行外设接口 (SPI)
5.2.1.6 双线汽车接口 (TWAI®)
USB 2.0 OTG 全速接口
5.2.1.7
USB 串口/JTAG 控制器
SD/MMC 主机控制器
LED PWM 控制器

5.2.1.8

5.2.1.9

5.2.1.10
5.2.1.11 电机控制脉宽调制器 (MCPWM)
5.2.1.12 红外遥控 (RMT)
5.2.1.13 脉冲计数控制器 (PCNT)

5.2.2 模拟信号处理

SAR ADC

5.2.2.1
5.2.2.2 温度传感器
5.2.2.3 触摸传感器

6 电气特性
6.1 绝对最大额定值
6.2 建议工作条件

乐鑫信息科技

2

2

3

3

8

9

9

9

12

13

14

14

14

15

16

16

16

16

16

17

17

17

18

19

20

21

21

22

22

23

23

24

24

24

24

25

25

25

4
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

目录

6.3 直流电气特性 (3.3 V, 25 °C)
6.4 功耗特性

Active 模式下的功耗

6.4.1
6.4.2 其他功耗模式下的功耗

6.5 存储器规格

7 射频特性
Wi-Fi 射频
7.1

7.1.1

7.1.2

Wi-Fi 射频发射器 (TX) 特性
Wi-Fi 射频接收器 (RX) 特性

7.2 低功耗蓝牙射频

7.2.1 低功耗蓝牙射频发射器 (TX) 特性
7.2.2 低功耗蓝牙射频接收器 (RX) 特性

8 模组原理图

9 外围设计原理图

10 模组尺寸

11 PCB 布局建议
PCB 封装图形
11.1
PCB 设计中的模组位置摆放

11.2

12 产品处理
12.1 存储条件
12.2 静电放电 (ESD)
12.3 回流焊温度曲线
12.4 超声波振动

技术规格书版本号管理

相关文档和资源

修订历史

25

26

26

26

28

29

29

29

30

31

31

33

36

37

38

39

39

40

41

41

41

41

42

43

44

45

乐鑫信息科技

5
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

表格

表格

ESP32-S3-WROOM-2 系列型号对比

1-1
3-1 管脚定义
4-1 Strapping 管脚的默认配置
4-2 Strapping 管脚的时序参数说明
4-3 芯片启动模式控制
4-4 VDD_SPI 电压控制
4-5 JTAG 信号源控制
4-6 上电和复位时序参数说明
6-1 绝对最大额定值
6-2 建议工作条件
6-3 直流电气特性 (3.3 V, 25 °C)
6-4 Active 模式下的射频功耗
6-5 Modem-sleep 模式下的功耗
6-6 低功耗模式下的功耗
6-7 Flash 规格
6-8 PSRAM 规格
7-1 Wi-Fi 射频规格
7-2 频谱模板和 EVM 符合 802.11 标准时的发射功率
7-3 发射 EVM 测试1
7-4 接收灵敏度
7-5 最大接收电平
7-6 接收邻道抑制
7-7 低功耗蓝牙射频规格
7-8 低功耗蓝牙 - 发射器特性 - 1 Mbps
7-9 低功耗蓝牙 - 发射器特性 - 2 Mbps
7-10 低功耗蓝牙 - 发射器特性 - 125 Kbps
7-11 低功耗蓝牙 - 发射器特性 - 500 Kbps
7-12 低功耗蓝牙 - 接收器特性 - 1 Mbps
7-13 低功耗蓝牙 - 接收器特性 - 2 Mbps
7-14 低功耗蓝牙 - 接收器特性 - 125 Kbps
7-15 低功耗蓝牙 - 接收器特性 - 500 Kbps

3

10

12

13

13

14

14

15

25

25

25

26

27

27

28

28

29

29

29

30

31

31

31

31

32

32

32

33

33

34

34

乐鑫信息科技

6
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

插图

插图

2-1 功能框图
3-1 管脚布局（顶视图）
4-1 Strapping 管脚的时序参数图
4-2 上电和复位时序参数图
8-1 原理图
9-1 外围设计原理图
10-1 模组尺寸
11-1 推荐 PCB 封装图
12-1 回流焊温度曲线

8

9

13

15

36

37

38

39

41

乐鑫信息科技

7
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

2 功能框图

2 功能框图

图 2-1. 功能框图

说明：

关于芯片与封装内 PSRAM 的管脚对应关系，请参考 《ESP32-S3 系列芯片技术规格书》 > 表格 芯片与封装内 flash/
PSRAM 的管脚对应关系。

乐鑫信息科技

8
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

ESP32-S3R8VESP32-S3R16VRF Matching40 MHzCrystal3V3ESP32-S3-WROOM-2UENGPIOsAntennaRF Matching40 MHzCrystal3V3ESP32-S3-WROOM-2ENGPIOsAntennaOSPI FlashSPICS0SPICLKSPIDSPIQSPIHDSPIWPVDD_SPIOSPI FlashSPICS0SPICLKSPIDSPIQSPIHDSPIWPVDD_SPIOSPI PSRAMSPIIO4OSPI PSRAMSPIIO5SPIIO6SPIIO7SPIDQSSPIIO4SPIIO5SPIIO6SPIIO7SPIDQSESP32-S3R8VESP32-S3R16V3 管脚定义

3 管脚定义

3.1 管脚布局

管脚布局图显示了模组上管脚的大致位置。按比例绘制的实际布局请参考图 10 模组尺寸。

图 3-1. 管脚布局（顶视图）

说明：

关于底板上模组天线净空区的更多信息，请查看 《ESP32-S3 硬件设计指南》 > 章节 基于模组的版图设计通用要点。

3.2 管脚描述

模组共有 41 个管脚，具体描述参见表 3-1 管脚定义。

管脚名称释义、管脚功能释义、以及外设管脚分配请参考 《ESP32-S3 系列芯片技术规格书》。

乐鑫信息科技

9
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

GND3V3ENIO4IO5IO6IO7IO204039383736353433323130292827GNDIO1IO2TXD0RXD0IO42IO41IO40IO39IO38NCNCNCIO041GNDKeepout ZoneGNDGNDGNDGNDGNDGNDGNDGND181920IO10IO11IO12212223IO13IO14IO21151617IO3IO46IO9242526IO47IO48IO451234567891011121314IO15IO16IO17IO18IO8IO193 管脚定义

名称 序号 类型 1 功能

表 3-1. 管脚定义

GND

3V3

EN

IO4

IO5

IO6

IO7

IO15

IO16

IO17

IO18

IO8

IO19

IO20

IO3

IO46

IO9

IO10

IO11

1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

16

17

18

19

P

P

I

接地

供电

高电平：芯片使能；

低电平：芯片关闭；

注意不能让 EN 管脚浮空。

I/O/T

RTC_GPIO4, GPIO4, TOUCH4, ADC1_CH3

I/O/T

RTC_GPIO5, GPIO5, TOUCH5, ADC1_CH4

I/O/T

RTC_GPIO6, GPIO6, TOUCH6, ADC1_CH5

I/O/T

RTC_GPIO7, GPIO7, TOUCH7, ADC1_CH6

I/O/T

RTC_GPIO15, GPIO15, U0RTS, ADC2_CH4, XTAL_32K_P

I/O/T

RTC_GPIO16, GPIO16, U0CTS, ADC2_CH5, XTAL_32K_N

I/O/T

RTC_GPIO17, GPIO17, U1TXD, ADC2_CH6

I/O/T

RTC_GPIO18, GPIO18, U1RXD, ADC2_CH7, CLK_OUT3

I/O/T

RTC_GPIO8, GPIO8, TOUCH8, ADC1_CH7, SUBSPICS1

I/O/T

RTC_GPIO19, GPIO19, U1RTS, ADC2_CH8, CLK_OUT2, USB_D-

I/O/T

RTC_GPIO20, GPIO20, U1CTS, ADC2_CH9, CLK_OUT1, USB_D+

I/O/T

RTC_GPIO3, GPIO3, TOUCH3, ADC1_CH2

I/O/T

GPIO46

I/O/T

RTC_GPIO9, GPIO9, TOUCH9, ADC1_CH8, FSPIHD, SUBSPIHD

I/O/T

RTC_GPIO10, GPIO10, TOUCH10, ADC1_CH9, FSPICS0, FSPIIO4,

SUBSPICS0

I/O/T

RTC_GPIO11, GPIO11, TOUCH11, ADC2_CH0, FSPID, FSPIIO5, SUBSPID

IO12

20

I/O/T

RTC_GPIO12, GPIO12, TOUCH12, ADC2_CH1, FSPICLK, FSPIIO6,

SUBSPICLK

IO13

IO14

IO21

IO47

IO48

IO45

IO0

NC

NC

NC

IO38

IO39

IO40

IO41

IO42

RXD0

21

22

23

24

25

26

27

28

29

30

31

32

33

34

35

36

I/O/T

RTC_GPIO13, GPIO13, TOUCH13, ADC2_CH2, FSPIQ, FSPIIO7, SUBSPIQ

I/O/T

I/O/T

I/O/T

I/O/T

I/O/T

RTC_GPIO14, GPIO14, TOUCH14, ADC2_CH3, FSPIWP, FSPIDQS,

SUBSPIWP

RTC_GPIO21, GPIO21
SPICLK_P_DIFF, GPIO472, SUBSPICLK_P_DIFF
SPICLK_N_DIFF,GPIO482, SUBSPICLK_N_DIFF
GPIO45

I/O/T

RTC_GPIO0, GPIO0

—

—

—

空管脚

空管脚

空管脚

I/O/T

GPIO38, FSPIWP, SUBSPIWP

I/O/T MTCK, GPIO39, CLK_OUT3, SUBSPICS1

I/O/T MTDO, GPIO40, CLK_OUT2

I/O/T MTDI, GPIO41, CLK_OUT1

I/O/T MTMS, GPIO42

I/O/T

U0RXD, GPIO44, CLK_OUT2

乐鑫信息科技

10
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

见下页

3 管脚定义

名称 序号 类型 1 功能

表 3-1 – 接上页

TXD0

IO2

IO1

GND

EPAD

37

38

39

40

41

I/O/T

U0TXD, GPIO43, CLK_OUT1

I/O/T

RTC_GPIO2, GPIO2, TOUCH2, ADC1_CH1

I/O/T

RTC_GPIO1, GPIO1, TOUCH1, ADC1_CH0

P

P

接地

接地

1 P：电源；I：输入；O：输出；T：可设置为高阻。加粗字体为管脚的默认功能。
2 由于 ESP32-S3R8V 和 ESP32-S3R16V 芯片的 VDD_SPI 电压已设置为 1.8 V，所以，不同于其他

GPIO，在 VDD_SPI 电源域中的 GPIO47 和 GPIO48 的工作电压也为 1.8 V。

乐鑫信息科技

11
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

4 启动配置项

4 启动配置项

说明：

以下内容摘自 《ESP32-S3 系列芯片技术规格书》 > 章节 启动配置项。芯片 Strapping 管脚与模组管脚的对应关系，可
参考章节 8 模组原理图。

芯片在上电或硬件复位时，可以通过 Strapping 管脚和 eFuse 位配置如下启动参数，无需微处理器的参
与：

• 芯片启动模式

– Strapping 管脚：GPIO0 和 GPIO46

• VDD_SPI 电压

– Strapping 管脚：GPIO45

– eFuse 参数：EFUSE_VDD_SPI_FORCE 和 EFUSE_VDD_SPI_TIEH

• ROM 日志打印

– Strapping 管脚：GPIO46

– eFuse 参数：EFUSE_UART_PRINT_CONTROL 和 EFUSE_DIS_USB_SERIAL_JTAG_ROM_PRINT

• JTAG 信号源

– Strapping 管脚：GPIO3

– eFuse 参数：EFUSE_DIS_PAD_JTAG、EFUSE_DIS_USB_JTAG 和 EFUSE_STRAP_JTAG_SEL

上述 eFuse 参数的默认值均为 0，也就是说没有烧写过。eFuse 只能烧写一次，一旦烧写为 1，便不能恢复为
0。有关烧写 eFuse 的信息，请参考 《ESP32-S3 技术参考手册》 > 章节 eFuse 控制器。

上述 strapping 管脚如果没有连接任何电路或连接的电路处于高阻抗状态，则其默认值（即逻辑电平值）取决于
管脚内部弱上拉/下拉电阻在复位时的状态。

表 4-1. Strapping 管脚的默认配置

Strapping 管脚 默认配置 值

GPIO0

GPIO3

GPIO45

GPIO46

弱上拉

浮空

1

–

弱下拉 0

弱下拉 0

要改变 strapping 管脚的值，可以连接外部下拉/上拉电阻。如果 ESP32-S3 用作主机 MCU 的从设备，
strapping 管脚的电平也可通过主机 MCU 控制。

所有 strapping 管脚都有锁存器。系统复位时，锁存器采样并存储相应 strapping 管脚的值，一直保持到芯片掉
电或关闭。锁存器的状态无法用其他方式更改。因此，strapping 管脚的值在芯片工作时一直可读取，strapping
管脚在芯片复位后作为普通 IO 管脚使用。

Strapping 管脚的信号时序需遵循表 4-2 和图 4-1 所示的 建立时间和 保持时间。

乐鑫信息科技

12
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

4 启动配置项

表 4-2. Strapping 管脚的时序参数说明

参数 说明

tSU 建立时间，即拉高 EN 激活芯片前，电源轨达到稳定所需的时间

tH

保持时间，即 EN 已拉高、strapping 管脚变为普通 IO 管脚开始工
作前，可读取 strapping 管脚值的时间

最小值 (ms)

0

3

tSU

tH

EN

图 4-1. Strapping 管脚的时序参数图

4.1 芯片启动模式控制

复位释放后，GPIO0 和 GPIO46 共同决定启动模式。详见表 4-3 芯片启动模式控制。

表 4-3. 芯片启动模式控制

启动模式

GPIO0 GPIO46

SPI Boot
Joint Download Boot 2

1

0

任意值

0

1 加粗表示默认值和默认配置。
2 Joint Download Boot 模式下支持以下下载

方式：

• USB Download Boot：

– USB-Serial-JTAG Download Boot

– USB-OTG Download Boot

• UART Download Boot

在 SPI Boot 模式下，ROM 引导加载程序通过从 SPI flash 中读取程序来启动系统。

在 Joint Download Boot 模式下，用户可通过 USB 或 UART0 接口将二进制文件下载至 flash，或将二进制文件
下载至 SRAM 并运行 SRAM 中的程序。

除了 SPI Boot 和 Joint Download Boot 模式，ESP32-S3 还支持 SPI Download Boot 模式，详见
《ESP32-S3 技术参考手册》 > 章节 芯片 Boot 控制。

乐鑫信息科技

13
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

Strapping pinVIL_nRSTVIH4 启动配置项

4.2 VDD_SPI 电压控制

电压有两种控制方式，具体取决于 EFUSE_VDD_SPI_FORCE 的值。

表 4-4. VDD_SPI 电压控制

电压 EFUSE_VDD_SPI_FORCE GPIO45

EFUSE_VDD_SPI_TIEH

VDD_SPI 电源 2
VDD3P3_RTC 通过 RSP I 供电 3.3 V
Flash 稳压器
1.8 V

Flash 稳压器
1.8 V
VDD3P3_RTC 通过 RSP I 供电 3.3 V

0

1

0

1

忽略

忽略

0

1

1 加粗表示默认值和默认配置。
2 请参考章节 《ESP32-S3 系列芯片技术规格书》 > 章节 电源管理。

4.3 ROM 日志打印控制

系统启动过程中，ROM 代码日志可打印至：

•（默认）UART0 和 USB 串口/JTAG 控制器

• USB 串口/JTAG 控制器

• UART0

通过配置寄存器和 eFuse 可分别关闭 UART 和 USB 串口/JTAG 控制器的 ROM 代码日志打印功能。详细信息请
参考 《ESP32-S3 技术参考手册》 > 章节 芯片 Boot 控制。

4.4 JTAG 信号源控制

在系统启动早期阶段，GPIO3 可用于控制 JTAG 信号源。该管脚没有内部上下拉电阻，strapping 的值必须由不
处于高阻抗状态的外部电路控制。

如表 4-5 所示，GPIO3 与 EFUSE_DIS_PAD_JTAG、EFUSE_DIS_USB_JTAG 和 EFUSE_STRAP_JTAG_SEL 共同
控制 JTAG 信号源。

JTAG 信号源

EFUSE_DIS_PAD_JTAG EFUSE_DIS_USB_JTAG EFUSE_STRAP_JTAG_SEL GPIO3

表 4-5. JTAG 信号源控制

USB 串口/JTAG 控制器

JTAG 管脚 2

JTAG 关闭

0

0

1

0

0

1

1 加粗表示默认值和默认配置。
2 即 MTDI、MTCK、MTMS 和 MTDO。

0

0

0

0

1

1

0

1

忽略

1

忽略

忽略

忽略

1

忽略

0

忽略

忽略

乐鑫信息科技

14
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

4 启动配置项

4.5 芯片上电和复位

芯片上电后，其电源轨需要一点时间方可稳定。之后，用于上电和复位的管脚 EN 拉高，激活芯片。更多关于
EN 及上电和复位时序的信息，请见图 4-2 和表 4-6。

tST BL

tRST

2.8 V

VDDA,
VDD3P3,
VDD3P3_RTC,
VDD3P3_CPU

EN

图 4-2. 上电和复位时序参数图

表 4-6. 上电和复位时序参数说明

参数 说明

tST BL

tRST

EN 管脚拉高激活芯片前，VDDA、VDD3P3、VDD3P3_RTC 和
VDD3P3_CPU 达到稳定所需的时间
EN 电平低于 VIL_nRST（具体数值参考表 6-3）从而复位芯片的时
间

最小值 (µs)

50

50

乐鑫信息科技

15
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

VIL_nRST5 外设

5 外设

5.1 外设概述

ESP32-S3 集成了丰富的外设，包括 SPI、LCD、Camera 接口、UART、I2C、I2S、红外遥控、脉冲计数器、LED
PWM、USB 串口/JTAG、MCPWM、SD/MMC 主机控制器、TWAI® 控制器（兼容 ISO 11898-1，即 CAN 规范
2.0）、ADC、触摸传感器和温度传感器。此外，ESP32-S3 还有一个全速 USB 2.0 On-The-Go (OTG) 接口用于
USB 通讯。

关于模组外设的详细信息，请参考《ESP32-S3 系列芯片技术规格书》 > 章节 功能描述。

说明：

以下内容出自 《ESP32-S3 系列芯片技术规格书》 > 章节 外设。并非所有 IO 信号都在模组上引出，因此这些信息不完
全适用于 ESP32-S3-WROOM-2。
关于外设信号的更多信息，可参考《ESP32-S3 技术参考手册》 > 章节 GPIO 交换矩阵外设信号列表。

5.2 外设描述

本章节介绍了芯片上的外设接口，包括扩展芯片功能的通信接口和片上传感器。

5.2.1 通讯接口

本章节介绍了芯片与外部设备和网络进行通信和交互的接口。

5.2.1.1 UART 控制器

ESP32-S3 有三个 UART（通用异步收发器）控制器，即 UART0、UART1、UART2，支持异步通信（RS232 和
RS485）和 IrDA，通信速率可达到 5 Mbps。

特性

• 支持三个可预分频的时钟源

• 可编程收发波特率

• 三个 UART 的发送 FIFO 以及接收 FIFO 共享 1024 x 8-bit RAM

• 全双工异步通信

• 支持输入信号波特率自检功能

• 支持 5/6/7/8 位数据长度

• 支持 1/1.5/2/3 个停止位

• 支持奇偶校验位

• 支持 AT_CMD 特殊字符检测

• 支持 RS485 协议

• 支持 IrDA 协议

• 支持 GDMA 高速数据通信

乐鑫信息科技

16
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

• 支持 UART 唤醒模式

• 支持软件流控和硬件流控

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 UART 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.2 I2C 接口

ESP32-S3 有两个 I2C 总线接口，根据用户的配置，总线接口可以用作 I2C 主机或从机模式。

特性

• 标准模式 (100 Kbit/s)

• 快速模式 (400 Kbit/s)

• 速度最高可达 800 Kbit/s，但受制于 SCL 和 SDA 上拉强度

• 7 位寻址模式和 10 位寻址模式

• 双地址（从机地址和从机寄存器地址）寻址模式

用户可以通过 I2C 硬件提供的指令抽象层更方便地控制 I2C 接口。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 I2C 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.3 I2S 接口

ESP32-S3 有两个标准 I2S 接口，可以以主机或从机模式，在全双工或半双工模式下工作，并且可被配置为 I2S
串行 8/16/24/32 位的收发数据模式，支持频率从 10 kHz 到 40 MHz 的 BCK 时钟。

I2S 接口有专用的 DMA 控制器。支持 TDM PCM、TDM MSB 对齐、TDM LSB 对齐、TDM Phillips、PDM 接
口。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 I2S 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.4 LCD 与 Camera 控制器

ESP32-S3 的 LCD 与 Camera 控制器包含独立的 LCD 模块和 Camera 模块。

LCD 模块用于发送并行视频数据信号，其总线 8 位 ~ 16 位并行 RGB、I8080、MOTO6800 接口，支持的时钟频
率小于 40 MHz。支持 RGB565、YUV422、YUV420、YUV411 之间的互相转换。

乐鑫信息科技

17
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

Camera 模块用于接收并行视频数据信号，其总线支持 8 位 ~ 16 位 DVP 图像传感器接口，支持的时钟频率小于
40 MHz。支持 RGB565、YUV422、YUV420、YUV411 之间的互相转换。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 LCD 与 Camera 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.5 串行外设接口 (SPI)

ESP32-S3 具有以下 SPI 接口：

• SPI0，供 ESP32-S3 的 GDMA 控制器与 Cache 访问封装内或封装外 flash/PSRAM

• SPI1，供 CPU 访问封装内或封装外 flash/PSRAM

• SPI2，通用 SPI 控制器，通过 GDMA 分配 DMA 通道进行访问

• SPI3，通用 SPI 控制器，通过 GDMA 分配 DMA 通道进行访问

特性

• SPI0 和 SPI1：

– 支持 SPI、Dual SPI、Quad SPI、Octal SPI、QPI 和 OPI 模式

– 八线 SPI 模式支持单倍数据速率 (SDR) 和双倍数据速率 (DDR)

– 时钟频率可配置，八线 SPI SDR/DDR 模式下最高可达 120 MHz

– 数据传输以字节为单位

• SPI2：

– 支持主机或从机模式

– 通过 GDMA 分配 DMA 通道进行访问

– 支持 SPI、Dual SPI、Quad SPI、Octal SPI、QPI 和 OPI 模式

– 时钟极性 (CPOL) 和相位 (CPHA) 可配置

– 时钟频率可配置

– 数据传输以字节为单位

– 读写数据位序可配置：最高有效位 (MSB) 优先，或最低有效位 (LSB) 优先

– 主机模式

* 支持双线全双工通信，时钟频率最高可达 80 MHz

* 八线 SPI 全双工模式仅支持单倍数据速率 (SDR)

* 支持单线、双线、四线和八线半双工通信，时钟频率最高可达 80 MHz

* 八线 SPI 半双工模式支持单倍数据速率（最高 80 MHz）和双倍数据速率（最高 40 MHz）

* 具有六个 SPI_CS 管脚，可与六个独立 SPI 从机相连

* CS 建立和保持时间可配置

乐鑫信息科技

18
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

– 从机模式

* 支持双线全双工通信，时钟频率最高可达 60 MHz

* 支持单线、双线和四线半双工通信，时钟频率最高可达 60 MHz

* 八线 SPI 全双工和半双工模式仅支持单倍数据速率 (SDR)

• SPI3：

– 支持主机或从机模式

– 通过 GDMA 分配 DMA 通道进行访问

– 支持 SPI、Dual SPI、Quad SPI 和 QPI 模式

– 时钟极性 (CPOL) 和相位 (CPHA) 可配置

– 时钟频率可配置

– 数据传输以字节为单位

– 读写数据位序可配置：最高有效位 (MSB) 优先，或最低有效位 (LSB) 优先

– 主机模式

* 支持双线全双工通信，时钟频率最高可达 80 MHz

* 支持单线、双线和四线半双工通信，时钟频率最高可达 80 MHz

* 具有三个 SPI_CS 管脚，可与三个独立 SPI 从机相连

* CS 建立和保持时间可配置

– 从机模式

* 支持双线全双工通信，时钟频率最高可达 60 MHz

* 支持单线、双线和四线半双工通信，时钟频率最高可达 60 MHz

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 SPI 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.6 双线汽车接口 (TWAI®)

双线汽车接口 (Two-Wire Automotive Interface, TWAI®) 协议是一种多主机、多播的通信协议，具有检测错误、
发送错误信号以及内置报文优先仲裁等功能。ESP32-S3 带有一个 TWAI 控制器。

特性

• 兼容 ISO 11898-1 协议（CAN 规范 2.0）

• 标准帧格式（11 位 ID）和扩展帧格式（29 位 ID）

• 1 Kbit/s 到 1 Mbit/s 比特率

• 多种操作模式：

– 工作模式

乐鑫信息科技

19
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

– 监听模式

– 自检模式（传输无需确认）

• 64 字节接收 FIFO

• 数据接收过滤器（支持单过滤器和双过滤器模式）

• 错误检测与处理：

– 错误计数器

– 可配置的错误中断阈值

– 错误代码记录

– 仲裁丢失记录

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 双线汽车接口。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.7 USB 2.0 OTG 全速接口

ESP32-S3 带有一个集成了收发器的全速 USB OTG 外设，符合 USB 2.0 规范。

通用特性

• 支持全速和低速速率

• 主机协商协议 (HNP) 和会话请求协议 (SRP)，均可作为 A 或 B 设备

• 动态 FIFO (DFIFO) 大小

• 支持多种存储器访问模式

– Scatter/Gather DMA 模式

– 缓冲 (Buffer) DMA 模式

– Slave 模式

• 可选择集成收发器或外部收发器

• 当仅使用集成收发器时，可通过时分复用技术，和 USB 串口/JTAG 控制器共用集成收发器

• 当集成收发器和外部收发器同时投入使用时，支持 USB OTG 和 USB 串口/JTAG 控制器两外设各自挑选不

同的收发器使用

设备模式 (Device mode) 特性

• 端点 0 永远存在（双向控制，由 EP0 IN 和 EP0 OUT 组成）

• 6 个附加端点 (1 ~ 6)，可配置为 IN 或 OUT

• 最多 5 个 IN 端点同时工作（包括 EP0 IN）

• 所有 OUT 端点共享一个 RX FIFO

乐鑫信息科技

20
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

• 每个 IN 端点都有专用的 TX FIFO

主机模式 (Host mode) 特性

• 8 个通道（管道）

– 由 IN 与 OUT 两个通道组成的一个控制管道，因为 IN 和 OUT 必须分开处理。仅支持控制传输类型。

– 其余 7 个管道可被配置为 IN 或 OUT，支持批量、同步、中断中的任意传输类型。

• 所有通道共用一个 RX FIFO、一个非周期性 TX FIFO、和一个周期性 TX FIFO。每个 FIFO 大小可配置。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 USB OTG。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.8 USB 串口/JTAG 控制器

ESP32-S3 集成了一个 USB 串口/JTAG 控制器。

特性

• USB 全速标准

• 可配置为使用 ESP32-S3 内部 USB PHY 或通过 GPIO 交换矩阵使用外部 PHY

• 固定功能。包含连接的 CDC-ACM（通信设备类抽象控制模型）和 JTAG 适配器功能

• 共 2 个 OUT 端点、3 个 IN 端点和 1 个控制端点 EP_0，可实现最大 64 字节的数据载荷

• 包含内部 PHY，基本无需其他外部组件连接主机计算机

• CDC-ACM 的虚拟串行功能在大多数现代操作系统上可实现即插即用

• JTAG 接口可使用紧凑的 JTAG 指令实现与 CPU 调试内核的快速通信

• CDC-ACM 支持主机控制芯片复位和进入下载模式

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 USB 串口/JTAG 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.9 SD/MMC 主机控制器

ESP32-S3 集成一个 SD/MMC 主机控制器。

特性

• SD 卡 3.0 和 3.01 版本

• SDIO 3.0 版本

• CE-ATA 1.1 版本

乐鑫信息科技

21
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

• 多媒体卡（MMC 4.41 版本、eMMC 4.5 版本和 4.51 版本）

• 高达 80 MHz 的时钟输出

• 3 种数据总线模式：

– 1 位

– 4 位（可支持两个 SD/SDIO/MMC 4.41 卡，以及一个以 1.8 V 电压工作的 SD 卡）

– 8 位

说明：

在 80 MHz 工作条件下，时钟相位调节能力受限，仅支持 0° 和 180° 两种相位配置。PCB 布局设计时应充分考虑该限

制，以确保时序收敛。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 SD/MMC 主机控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.10 LED PWM 控制器

LED PWM 控制器可以用于生成八路独立的数字波形。

特性

• 波形的周期和占空比可配置，在信号周期为 1 ms 时，占空比精确度可达 14 位

• 多种时钟源选择，包括：APB 总线时钟、外置主晶振时钟

• 可在 Light-sleep 模式下工作

• 支持硬件自动步进式地增加或减少占空比，可用于 LED RGB 彩色梯度发生器

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 LED PWM 控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.11 电机控制脉宽调制器 (MCPWM)

ESP32-S3 包含两个 MCPWM，可以用于驱动数字马达和智能灯。每个 MCPWM 外设都包含一个时钟分频器
（预分频器）、三个 PWM 定时器、三个 PWM 操作器和一个捕捉模块。PWM 定时器用于生成定时参考。PWM 操
作器将根据定时参考生成所需的波形。通过配置，任一 PWM 操作器可以使用任一 PWM 定时器的定时参考。不
同的 PWM 操作器可以使用相同的 PWM 定时器的定时参考来产生 PWM 信号。此外，不同的 PWM 操作器也可
以使用不同的 PWM 定时器的值来生成单独的 PWM 信号。不同的 PWM 定时器也可进行同步。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 电机控制脉宽调制器。

乐鑫信息科技

22
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.12 红外遥控 (RMT)

红外遥控 (RMT) 支持红外控制信号的发射和接收。

特性

• 四个通道支持发送

• 四个通道支持接收

• 可编程配置多个通道同时发送

• RMT 的八个通道共享 384 x 32-bit 的 RAM

• 发送脉冲支持载波调制

• 接收脉冲支持滤波和载波解调

• 乒乓发送模式

• 乒乓接收模式

• 发射器支持持续发送

• 发送通道 3 支持 DMA 访问

• 接收通道 7 支持 DMA 访问

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 红外遥控。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.1.13 脉冲计数控制器 (PCNT)

脉冲计数器 (PCNT) 通过多种模式捕捉脉冲并对脉冲边沿计数。

特性

• 四个脉冲计数控制器（单元），各自独立工作，计数范围是 1 ~ 65535

• 每个单元有两个独立的通道，共用一个脉冲计数控制器

• 所有通道均有输入脉冲信号（如 sig_ch0_un）和相应的控制信号（如 ctrl_ch0_un）

• 滤波器独立工作，过滤每个单元输入脉冲信号（sig_ch0_un 和 sig_ch1_un）控制信号（ctrl_ch0_un 和

ctrl_ch1_un）的毛刺

• 每个通道参数如下：

1. 选择在输入脉冲信号的上升沿或下降沿计数

2. 在控制信号为高电平或低电平时可将计数模式配置为递增、递减或停止计数

乐鑫信息科技

23
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5 外设

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 脉冲计数控制器。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.2 模拟信号处理

本小节描述芯片上感知和处理现实世界数据的组件。

5.2.2.1 SAR ADC

ESP32-S3 集成了两个 12 位 SAR ADC，共支持 20 个模拟通道输入。为了实现更低功耗，ESP32-S3 的 ULP 协
处理器也可以在睡眠方式下测量电压，此时，可通过设置阈值或其他触发方式唤醒 CPU。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 片上传感器与模拟信号处理。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

5.2.2.2 温度传感器

温度传感器生成一个随温度变化的电压。内部 ADC 将传感器电压转化为一个数字量。

温度传感器的测量范围为–40 °C 到 125 °C。温度传感器适用于监测芯片内部温度的变化，该温度值会随着微控
制器时钟频率或 IO 负载的变化而变化。一般来讲，芯片内部温度会高于外部温度。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 片上传感器与模拟信号处理。

5.2.2.3 触摸传感器

ESP32-S3 提供了多达 14 个电容式传感 GPIO，能够探测由手指或其他物品直接接触或接近而产生的电容差异。
这种设计具有低噪声和高灵敏度的特点，可以用于支持使用相对较小的触摸板。设计中也可以使用触摸板阵列

以探测更大区域或更多点。ESP32-S3 的触摸传感器同时还支持防水和数字滤波等功能来进一步提高传感器的
性能。

说明：

ESP32-S3 触摸传感器目前尚无法通过射频抗扰度测试系统 (CS) 认证，应用场景有所限制。

更多信息，请参考 《ESP32-S3 技术参考手册》 > 章节 片上传感器与模拟信号处理。

管脚分配

详见 《ESP32-S3 系列芯片技术规格书》 > 章节 外设管脚分配。

乐鑫信息科技

24
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

6 电气特性

6 电气特性

6.1 绝对最大额定值

超出表 6-1 绝对最大额定值 可能导致器件永久性损坏。这只是强调的额定值，不涉及器件在这些或其它条件下
超出表 6-2 建议工作条件 技术规格指标的功能性操作。长时间暴露在绝对最大额定条件下可能会影响模组的可
靠性。

表 6-1. 绝对最大额定值

符号

参数

最小值 最大值 单位

VDD33 电源管脚电压

TST ORE 存储温度

–0.3

–40

3.6

105

V

°C

6.2 建议工作条件

表 6-2. 建议工作条件

符号

参数

最小值 典型值 最大值 单位

VDD33 电源管脚电压

IV DD

TA

外部电源的供电电流

工作环境温度

3.0

0.5

–40

3.3

—

—

3.6

—

65

V

A

°C

6.3 直流电气特性 (3.3 V, 25 °C)

表 6-3. 直流电气特性 (3.3 V, 25 °C)

参数

说明

最小值

典型值

最大值

单位

CIN

VIH

VIL

IIH

IIL

2

2

VOH

VOL

IOH

IOL

RP U

管脚电容

高电平输入电压

低电平输入电压

高电平输入电流

低电平输入电流

高电平输出电压

低电平输出电压
高电平拉电流 (VDD 1 = 3.3 V, VOH >= 2.64 V,
PAD_DRIVER = 3)
低电平灌电流 (VDD 1 = 3.3 V, VOL = 0.495 V,
PAD_DRIVER = 3)

内部弱上拉电阻

—
0.75 × VDD 1
–0.3

—

—
0.8 × VDD 1
—

—

—

—

内部弱下拉电阻

RP D
—
VIH_nRST 芯片复位释放电压（EN 管脚应满足电压范围） 0.75 × VDD 1
VIL_nRST 芯片复位电压（EN 管脚应满足电压范围）
–0.3
1 VDD – 各个电源域电源管脚的电压。
2 VOH 和 VOL 为负载是高阻条件下的测试值。

2

—
VDD 1 + 0.3
—
— 0.25 × VDD 1
50
—

—

—

—

40

28

45

50

—
0.1 × VDD 1

—

—

—

45

—
VDD 1 + 0.3
—
— 0.25 × VDD 1

pF

V

V

nA

nA

V

V

mA

mA

kΩ

kΩ

V

V

乐鑫信息科技

25
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

6 电气特性

6.4 功耗特性

6.4.1 Active 模式下的功耗

因使用了先进的电源管理技术，模组可以在不同的功耗模式之间切换。关于不同功耗模式的描述，详见
《ESP32-S3 系列芯片技术规格书》 > 电源管理单元章节。

下列功耗数据是基于 3.3 V 供电电源、25 °C 环境温度的条件下测得。

所有发射功耗数据均基于 100% 占空比测得。

所有接收功耗数据均是在外设关闭、CPU 空闲的条件下测得。

表 6-4. Active 模式下的射频功耗

工作模式

描述

Active（射频工作）

802.11b, 1 Mbps, @20.5 dBm

802.11g, 54 Mbps, @18 dBm

802.11n, HT20, MCS7, @17.5 dBm

802.11n, HT40, MCS7, @17 dBm

802.11b/g/n, HT20

802.11n, HT40

TX

RX

说明：

以下内容摘自 《ESP32-S3 系列芯片技术规格书》 的 其他功耗模式下的功耗章节。

6.4.2 其他功耗模式下的功耗

请注意，若模组内置芯片封装内有 PSRAM，功耗数据可能略高于下表数据。

峰值 (mA)

355

297

286

285

95

97

乐鑫信息科技

26
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

6 电气特性

表 6-5. Modem-sleep 模式下的功耗

工作模式

频率

(MHz)

说明

典型值1

典型值2

(mA)

(mA)

WAITI（双核均空闲）
单核执行 32 位数据访问指令，另一个核空闲
双核执行 32 位数据访问指令
单核执行 128 位数据访问指令，另一个核空闲
双核执行 128 位数据访问指令

WAITI
单核执行 32 位数据访问指令，另一个核空闲
双核执行 32 位数据访问指令
单核执行 128 位数据访问指令，另一个核空闲
双核执行 128 位数据访问指令

WAITI
单核执行 32 位数据访问指令，另一个核空闲
双核执行 32 位数据访问指令
单核执行 128 位数据访问指令，另一个核空闲
双核执行 128 位数据访问指令

WAITI
单核执行 32 位数据访问指令，另一个核空闲
双核执行 32 位数据访问指令
单核执行 128 位数据访问指令，另一个核空闲
双核执行 128 位数据访问指令

40

80

160

240

13.2

16.2

18.7

19.9

23.0

22.0

28.4

33.1

35.1

41.8

27.6

39.9

49.6

54.4

66.7

32.9

51.2

66.2

72.4

91.7

18.8

21.8

24.4

25.4

28.8

36.1

42.6

47.3

49.6

56.3

42.3

54.6

64.1

69.2

81.1

47.6

65.9

81.3

87.9

107.9

Modem-sleep3

1 所有外设时钟关闭时的典型值。
2 所有外设时钟打开时的典型值。实际情况下，外设在不同工作状态下电流会有所差异。
3 Modem-sleep 模式下，Wi-Fi 设有时钟门控。该模式下，访问 flash 时功耗会增加。若 flash 速率为 80 Mbit/s，

SPI 双线模式下 flash 的功耗为 10 mA。

表 6-6. 低功耗模式下的功耗

说明

典型值 (µA)

工作模式
Light-sleep1

Deep-sleep

VDD_SPI 和 Wi-Fi 掉电，所有 GPIO 设置为高阻状态

ULP-FSM

ULP-RISC-V

ULP 协处理器处于
工作状态2
超低功耗传感器监测模式3
RTC 存储器和 RTC 外设上电
RTC 存储器上电，RTC 外设掉电

240

170

190

18

8

7

1

关闭

EN 管脚拉低，芯片关闭

1 Light-sleep 模式下，SPI 相关管脚上拉。封装内有 PSRAM 的芯片请在典型值的基础上添加相

应的 PSRAM 功耗：8 MB 8 线 PSRAM (3.3 V) 为 140 µA；8 MB 8 线 PSRAM (1.8 V) 为 200 µA；
2 MB 4 线 PSRAM 为 40 µA。

2 Deep-sleep 模式下，仅 ULP 协处理器处于工作状态时，可以操作 GPIO 及低功耗 I2C。
3 当系统处于超低功耗传感器监测模式时，ULP 协处理器或传感器周期性工作。触摸传感器以 1%

占空比工作，系统功耗典型值为 18 µA。

乐鑫信息科技

27
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

6 电气特性

6.5 存储器规格

本节数据来源于存储器供应商的数据手册。以下数值已在设计阶段和/或特性验证中得到确认，但未在生产中进
行全面测试。设备出厂时，存储器均为擦除状态。

表 6-7. Flash 规格

参数 说明

最小值 典型值 最大值 单位

VCC

FC

—

电源电压 (1.8 V)
电源电压 (3.3 V)

最大时钟频率

编程/擦除周期

TRET 数据保留时间
TP P 页编程时间
TSE 扇区擦除时间 (4 KB)
TBE1 块擦除时间 (32 KB)
TBE2 块擦除时间 (64 KB)

TCE

芯片擦除时间 (16 Mb)
芯片擦除时间 (32 Mb)
芯片擦除时间 (64 Mb)
芯片擦除时间 (128 Mb)
芯片擦除时间 (256 Mb)

1.65

2.7

80

100,000

20

—

—

—

—

—

—

—

—

—

1.80

3.3

2.00

3.6

V

V

—

—

—

0.8

70

0.2

0.3

7

20

25

60

70

— MHz

— 次

— 年

5 ms

500 ms

2

3

20

60

100

200

300

s

s

s

s

s

s

s

表 6-8. PSRAM 规格

参数 说明

最小值 典型值 最大值 单位

VCC

电源电压 (1.8 V)
电源电压 (3.3 V)

FC

最大时钟频率

1.62

2.7

80

1.80

3.3

—

1.98

3.6

V

V

— MHz

乐鑫信息科技

28
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

7 射频特性

本章提供产品的射频特性表。

射频数据是在天线端口处连接射频线后测试所得，包含了射频前端电路带来的损耗。

工作信道中心频率范围应符合国家或地区的规范标准。软件可以配置工作信道中心频率范围，具体请参

考《ESP 射频测试指南》。

除非特别说明，射频测试均是在 3.3 V (±5%) 供电电源、25 °C 环境温度的条件下完成。

7.1 Wi-Fi 射频

表 7-1. Wi-Fi 射频规格

名称

工作信道中心频率范围

无线标准

描述

2412 ~ 2484 MHz

IEEE 802.11b/g/n

7.1.1 Wi-Fi 射频发射器 (TX) 特性

表 7-2. 频谱模板和 EVM 符合 802.11 标准时的发射功率

速率

802.11b, 1 Mbps

802.11b, 11 Mbps

802.11g, 6 Mbps

802.11g, 54 Mbps

802.11n, HT20, MCS 0

802.11n, HT20, MCS 7

802.11n, HT40, MCS 0

802.11n, HT40, MCS 7

最小值 典型值 最大值

(dBm)

(dBm)

(dBm)

—

—

—

—

—

—

—

—

20.5

20.5

20.0

18.0

19.0

17.5

18.5

17.0

—

—

—

—

—

—

—

—

表 7-3. 发射 EVM 测试1

速率

802.11b, 1 Mbps, @20.5 dBm

802.11b, 11 Mbps, @20.5 dBm

802.11g, 6 Mbps, @20 dBm

802.11g, 54 Mbps, @18 dBm

802.11n, HT20, MCS 0, @19 dBm

802.11n, HT20, MCS 7, @17.5 dBm

802.11n, HT40, MCS 0, @18.5 dBm

最小值 典型值 标准限值

(dB)

—

—

—

—

—

—

—

(dB)

–24.5

–24.5

–23.0

–29.5

–24.0

–30.5

–25.0

(dB)

–10

–10

–5

–25

–5

–27

–5
见下页

乐鑫信息科技

29
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

速率

表 7-3 – 接上页

最小值 典型值 标准限值

(dB)

(dB)

(dB)

802.11n, HT40, MCS 7, @17 dBm

—

–30.0

–27

1 发射 EVM 的每个测试项对应的发射功率为表 7-2 频谱模板和 EVM 符

合 802.11 标准时的发射功率 中提供的典型值。

7.1.2 Wi-Fi 射频接收器 (RX) 特性

802.11b 标准下的误包率 (PER) 不超过 8%，802.11g/n 标准下不超过 10%。

速率

802.11b, 1 Mbps

802.11b, 2 Mbps

802.11b, 5.5 Mbps

802.11b, 11 Mbps

802.11g, 6 Mbps

802.11g, 9 Mbps

802.11g, 12 Mbps

802.11g, 18 Mbps

802.11g, 24 Mbps

802.11g, 36 Mbps

802.11g, 48 Mbps

802.11g, 54 Mbps

802.11n, HT20, MCS 0

802.11n, HT20, MCS 1

802.11n, HT20, MCS 2

802.11n, HT20, MCS 3

802.11n, HT20, MCS 4

802.11n, HT20, MCS 5

802.11n, HT20, MCS 6

802.11n, HT20, MCS 7

802.11n, HT40, MCS 0

802.11n, HT40, MCS 1

802.11n, HT40, MCS 2

802.11n, HT40, MCS 3

802.11n, HT40, MCS 4

802.11n, HT40, MCS 5

802.11n, HT40, MCS 6

802.11n, HT40, MCS 7

表 7-4. 接收灵敏度

最小值 典型值 最大值

(dBm)

(dBm)

(dBm)

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

–98.2

–95.6

–92.8

–88.5

–93.0

–92.0

–90.8

–88.5

–85.5

–82.2

–78.0

–76.2

–93.0

–90.6

–88.4

–84.8

–81.6

–77.4

–75.6

–74.2

–90.0

–87.5

–85.0

–82.0

–78.5

–74.4

–72.5

–71.2

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

乐鑫信息科技

30
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

表 7-5. 最大接收电平

速率

802.11b, 1 Mbps

802.11b, 11 Mbps

802.11g, 6 Mbps

802.11g, 54 Mbps

802.11n, HT20, MCS 0

802.11n, HT20, MCS 7

802.11n, HT40, MCS 0

802.11n, HT40, MCS 7

速率

802.11b, 1 Mbps

802.11b, 11 Mbps

802.11g, 6 Mbps

802.11g, 54 Mbps

802.11n, HT20, MCS 0

802.11n, HT20, MCS 7

802.11n, HT40, MCS 0

802.11n, HT40, MCS 7

最小值 典型值 最大值

(dBm)

(dBm)

(dBm)

—

—

—

—

—

—

—

—

5

5

5

0

5

0

5

0

—

—

—

—

—

—

—

—

表 7-6. 接收邻道抑制

最小值 典型值 最大值

(dB)

(dB)

(dB)

—

—

—

—

—

—

—

—

35

35

31

14

31

13

19

8

—

—

—

—

—

—

—

—

7.2 低功耗蓝牙射频

表 7-7. 低功耗蓝牙射频规格

名称

工作信道中心频率范围

射频发射功率范围

描述

2402 ~ 2480 MHz

–24.0 ~ 20.0 dBm

7.2.1 低功耗蓝牙射频发射器 (TX) 特性

表 7-8. 低功耗蓝牙 - 发射器特性 - 1 Mbps

参数

载波频率偏移和漂移

n=0, 1, 2, ..k 最大值

描述
|fn|
|f0 − fn| 最大值
|fn − fn−5| 最大值
|f1 − f0|

最小值 典型值 最大值

单位

—

—

—

—

2.50

2.00

1.40

1.00

—

—

—

—

kHz

kHz

kHz

kHz
见下页

乐鑫信息科技

31
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

参数

描述

最小值 典型值 最大值

表 7-8 – 接上页

调制特性

带内杂散发射

∆ f 1avg
∆ f 2max 最小值

（至少 99.9% 的 ∆ f 2max）

∆ f 2avg/∆ f 1avg
± 2 MHz 偏移
± 3 MHz 偏移
> ± 3 MHz 偏移

—

—

—

—

—

—

249.00

198.00

0.86

–37.00
–42.00
–44.00

表 7-9. 低功耗蓝牙 - 发射器特性 - 2 Mbps

单位

kHz

kHz

—

—

—

—

— dBm

— dBm

— dBm

参数

载波频率偏移和漂移

调制特性

带内杂散发射

n=0, 1, 2, ..k 最大值

描述
|fn|
|f0 − fn| 最大值
|fn − fn−5| 最大值
|f1 − f0|
∆ f 1avg
∆ f 2max 最小值

（至少 99.9% 的 ∆ f 2max）

∆ f 2avg/∆ f 1avg
± 4 MHz 偏移
± 5 MHz 偏移
> ± 5 MHz 偏移

最小值 典型值 最大值

单位

—

—

—

—

—

—

—

—

—

—

2.50

2.00

1.40

1.00

499.00

416.00

0.89

–42.00
–44.00
–47.00

—

—

—

—

—

—

—

kHz

kHz

kHz

kHz

kHz

kHz

—

— dBm

— dBm

— dBm

表 7-10. 低功耗蓝牙 - 发射器特性 - 125 Kbps

参数

载波频率偏移和漂移

调制特性

带内杂散发射

n=0, 1, 2, ..k 最大值

描述
|fn|
|f0 − fn| 最大值
|fn − fn−3|
|f0 − f3|
∆ f 1avg
∆ f 1max 最小值

（至少 99.9% 的 ∆ f 1max）

± 2 MHz 偏移
± 3 MHz 偏移
> ± 3 MHz 偏移

最小值 典型值 最大值

单位

—

—

—

—

—

—

—

—

—

0.80

1.00

0.30

1.00

248.00

222.00

–37.00
–42.00
–44.00

—

—

—

—

—

—

kHz

kHz

kHz

kHz

kHz

kHz

— dBm

— dBm

— dBm

表 7-11. 低功耗蓝牙 - 发射器特性 - 500 Kbps

参数

载波频率偏移和漂移

n=0, 1, 2, ..k 最大值

描述
|fn|
|f0 − fn| 最大值
|fn − fn−3|
|f0 − f3|

最小值 典型值 最大值

单位

—

—

—

—

0.80

1.00

0.85

0.34

—

—

—

—

kHz

kHz

kHz

kHz
见下页

乐鑫信息科技

32
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

参数

描述

最小值 典型值 最大值

表 7-11 – 接上页

调制特性

带内杂散发射

∆ f 2avg
∆ f 2max 最小值

（至少 99.9% 的 ∆ f 2max）

± 2 MHz 偏移
± 3 MHz 偏移
> ± 3 MHz 偏移

—

—

—

—

—

213.00

196.00

–37.00
–42.00
–44.00

7.2.2 低功耗蓝牙射频接收器 (RX) 特性

表 7-12. 低功耗蓝牙 - 接收器特性 - 1 Mbps

单位

kHz

kHz

—

—

— dBm

— dBm

— dBm

参数

灵敏度 @30.8% PER

最大接收信号 @30.8% PER

共信道抑制比 C/I

邻道选择性抑制比 C/I

镜像频率

邻道镜像频率干扰

带外阻塞

互调

参数

灵敏度 @30.8% PER

最大接收信号 @30.8% PER

共信道干扰 C/I

邻道选择性抑制比 C/I

描述

—

—

F = F0 MHz

F = F0 + 1 MHz

F = F0 – 1 MHz

F = F0 + 2 MHz

F = F0 – 2 MHz

F = F0 + 3 MHz

F = F0 – 3 MHz
F > F0 + 3 MHz
F > F0 – 3 MHz

—

F = Fimage + 1 MHz
F = Fimage – 1 MHz

30 MHz ~ 2000 MHz

2003 MHz ~ 2399 MHz

2484 MHz ~ 2997 MHz

3000 MHz ~ 12.75 GHz

—

最小值 典型值 最大值 单位

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

—

–96.5

8

9

–3
–3
–28
–30
–31
–33
–32
–36

–32

–39
–31

–9
–18
–15
–5

–29

— dBm

— dBm

—

—

—

—

—

—

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

— dBm

— dBm

— dBm

— dBm

— dBm

表 7-13. 低功耗蓝牙 - 接收器特性 - 2 Mbps

描述

—

—

F = F0 MHz

F = F0 + 2 MHz

F = F0 – 2 MHz

F = F0 + 4 MHz

F = F0 – 4 MHz

F = F0 + 6 MHz

最小值 典型值 最大值 单位

—

—

—

—

—

—

—

—

–92.5

3

10

–8
–5
–31
–33
–37

— dBm

— dBm

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB
见下页

乐鑫信息科技

33
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

参数

镜像频率

邻道镜像频率干扰

带外阻塞

互调

参数

灵敏度 @30.8% PER

最大接收信号 @30.8% PER

共信道抑制比 C/I

邻道选择性抑制比 C/I

镜像频率

邻道镜像频率干扰

表 7-13 – 接上页

描述

F = F0 – 6 MHz
F > F0 + 6 MHz
F > F0 – 6 MHz

—

F = Fimage + 2 MHz
F = Fimage – 2 MHz

30 MHz ~ 2000 MHz

2003 MHz ~ 2399 MHz

2484 MHz ~ 2997 MHz

3000 MHz ~ 12.75 GHz

—

最小值 典型值 最大值 单位

—

—

—

—

—

—

—

—

—

—

—

–37
–40
–40

–31

–37
–8

–15
–19
–15
–6

–29

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB

— dBm

— dBm

— dBm

— dBm

— dBm

表 7-14. 低功耗蓝牙 - 接收器特性 - 125 Kbps

描述

—

—

F = F0 MHz

F = F0 + 1 MHz

F = F0 – 1 MHz

F = F0 + 2 MHz

F = F0 – 2 MHz

F = F0 + 3 MHz

F = F0 – 3 MHz
F > F0 + 3 MHz
F > F0 – 3 MHz

—

F = Fimage + 1 MHz
F = Fimage – 1 MHz

最小值 典型值 最大值 单位

—

—

—

—

—

—

—

—

—

—

—

—

—

—

–103.5

8

6

–6
–5
–32
–39
–35
–45
–35
–48

–35

–49
–32

— dBm

— dBm

—

—

—

—

—

—

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

dB

表 7-15. 低功耗蓝牙 - 接收器特性 - 500 Kbps

参数

灵敏度 @30.8% PER

最大接收信号 @30.8% PER

共信道抑制比 C/I

邻道选择性抑制比 C/I

描述

—

—

F = F0 MHz

F = F0 + 1 MHz

F = F0 – 1 MHz

F = F0 + 2 MHz

F = F0 – 2 MHz

F = F0 + 3 MHz

最小值 典型值 最大值 单位

—

—

—

—

—

—

—

—

–100

8

4

–5
–5
–28
–36
–36

— dBm

— dBm

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB
见下页

乐鑫信息科技

34
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

7 射频特性

参数

镜像频率

邻道镜像频率干扰

表 7-15 – 接上页

描述

F = F0 – 3 MHz
F > F0 + 3 MHz
F > F0 – 3 MHz

—

F = Fimage + 1 MHz
F = Fimage – 1 MHz

最小值 典型值 最大值 单位

—

—

—

—

—

—

–38
–37
–41

–37

–44
–28

—

—

—

—

—

—

dB

dB

dB

dB

dB

dB

乐鑫信息科技

35
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

乐
鑫
信
息
科
技

反
馈
文
档
意
见

3
6

E
S
P
3
2
-
S
3
-
W
R
O
O
M
-
2
技
术
规
格
书
v
1
.
7

8 模组原理图

模组内部元件的电路图。 ESP32-S3R8V 和 ESP32-S3R16V 芯片的 VDD_SPI 已经通过 eFuse VDD_SPI_TIEH 和 VDD_SPI_FORCE 设置为 1.8 V。

8

模
组
原
理
图

请注意，从 BOM v0.7 开始，ESP32-S3-WROOM-2 GPIO45 上的外部上拉电阻 R1 已改为不上件。详细信息请参考 ESP32-S3-WROOM-2 模组量产 BOM 变更。

图 8-1. 原理图

5544332211DDCCBBAAThe values of L3, C16, C11, L2 and C12vary with the actual PCB board.The values of C1 and C4 vary withthe selection of the crystal.The value of R4 varies with theactual PCB board. R4 could be aresistor or inductor, the initialvalue is suggested to be 24 nH.ESP32-S3-WROOM-2(pin-out)NC: No component.50 ohm Impedance ControlESP32-S3R16VESP32-S3R8VVDD_SPIVDD33GNDGNDGNDVDD33GNDGNDGNDGNDVDD33GNDGNDGNDGNDGNDGNDVDD33VDD33VDD33GNDGNDGNDGNDGNDGNDVDD_SPIVDD_SPIGNDGNDGNDGNDVDD33TitleSizePage NameRevDate:SheetofConfidential and Proprietary<02_ESP32-S3-WROOM-2>V1.3<ESP32-S3-WROOM-2>A422Monday, December 02, 2024TitleSizePage NameRevDate:SheetofConfidential and Proprietary<02_ESP32-S3-WROOM-2>V1.3<ESP32-S3-WROOM-2>A422Monday, December 02, 2024TitleSizePage NameRevDate:SheetofConfidential and Proprietary<02_ESP32-S3-WROOM-2>V1.3<ESP32-S3-WROOM-2>A422Monday, December 02, 2024C130.1uFR40C31uFESP32-S3-WROOM-2GND13V32EN3IO44IO55IO66IO77IO158IO169IO1710IO1811IO1913IO2014IO812GND40IO139IO238TXD037RXD036IO4235IO4134IO4033IO3932IO3831NC30NC29NC28IO027IO4616IO917IO1018IO1119IO1220IO1321IO1422IO2123IO4724IO4825IO315IO4526EPAD41R160L12.0nH(0.1nH)C4TBDR70U2FLASH_1V8CS#C2RESET#A4DQSC3NC3B1SCLKB2NC1A2NC2A3WP#C5NC4B5ECS#A5SI(IO0)D3SO(IO1)D2IO2C4IO3D4IO5E3IO7E1IO4D5IO6E2VCCB4VCCD1VCCE4VSSE5VSSC1VSSB3C90.1uFC1TBDC141uFANT1PCB_ANT12C80.1uFR60R90C71uFC610uFR140C100.1uFR150Y140MHz(±10ppm)XIN1GND2XOUT3GND4L3TBDR80R50L2TBDR110K(NC)C16TBDC210nFU1VDDA56LNA_IN1VDD3P32VDD3P33GPIO05GPIO16GPIO27GPIO38GPIO49GPIO510GPIO611GPIO712GPIO1015GPIO1116GPIO1217GPIO1318GPIO1419XTAL_32K_P21VDD3P3_RTC20XTAL_32K_N22GPIO1723GPIO1824GPIO1925GPIO2026VDD_SPI29SPIWP31SPICS032SPIQ34SPID35SPICLK33SPICLK_N36GND57SPICLK_P37GPIO3338GPIO3843GPIO4652XTAL_N53XTAL_P54MTMS48MTDO45U0TXD49VDD3P3_CPU46CHIP_PU4VDDA55MTDI47GPIO813GPIO914GPIO2127SPICS128SPIHD30GPIO3439GPIO3540GPIO3641U0RXD50GPIO4551GPIO3742MTCK44C12TBDR1210KD1ESDR1110KR100R3499R130C150.1uFC11TBDSPI_CS0LNA_INRF_ANTSPI_CLKSPI_QSPI_WPSPI_HDGPIO21GPIO45U0TXDGPIO46GPIO38GPIO40GPIO41GPIO42U0RXDGPIO39GPIO47GPIO48SPI_DGPIO0GPIO1GPIO2GPIO3GPIO4GPIO5GPIO6GPIO7GPIO8GPIO9CHIP_PUGPIO20GPIO19GPIO18GPIO17GPIO16GPIO15GPIO14GPIO13GPIO12GPIO11GPIO10CHIP_PUGPIO4GPIO5GPIO6GPIO7GPIO15GPIO16GPIO17GPIO18GPIO3GPIO21GPIO46GPIO9GPIO10GPIO11GPIO12GPIO13GPIO14GPIO45GPIO47GPIO48GPIO0GPIO38GPIO39GPIO40GPIO41GPIO42U0RXDU0TXDGPIO2GPIO1GPIO8GPIO19GPIO20SPI_CLKSPI_HDSPI_CS0SPI_DSPI_WPSPI_QSPI_IO4SPI_IO5SPI_IO6SPI_IO7SPI_DQSSPI_DQSSPI_IO4SPI_IO5SPI_IO6SPI_IO79 外围设计原理图

9 外围设计原理图

模组与外围器件（如电源、天线、复位按钮、JTAG 接口、UART 接口等）连接的应用电路图。

图 9-1. 外围设计原理图

• EPAD 可以不焊接到底板，但是焊接到底板的 GND 可以获得更好的散热特性。如果您想将 EPAD 焊接到底

板，请确保使用适量焊膏，避免过量焊膏造成模组与底板距离过大，影响管脚与底板之间的贴合。

• 为确保 ESP32-S3 芯片上电时的供电正常，EN 管脚处需要增加 RC 延迟电路。RC 通常建议为 R = 10 kΩ，
C = 1 µF，但具体数值仍需根据模组电源的上电时序和芯片的上电复位时序进行调整。ESP32-S3 芯片的
上电复位时序图可参考章节 4.5 芯片上电和复位。

乐鑫信息科技

37
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

5544332211DDCCBBAANC: No component.X1: ESR = Max. 70 K(cid:525)IO47/IO48 operates in the 1.8V voltage domain.ENIO42TMSIO41TDIIO38IO40TDOIO39TCKTXD0RXD0IO48IO47IO12IO13IO3IO6IO7IO9IO10IO11IO15IO16IO14IO21IO17IO18USB_D-USB_D+IO1IO2IO45IO4IO5IO0ENIO19IO20IO46IO8GNDGNDGNDVDD33GNDGNDGNDGNDGNDVDD33GNDGNDGNDGNDC412pF(NC)SW1JP4Boot Option1122C30.1uFU1ESP32-S3-WROOM-2GND13V32EN3IO44IO55IO66IO77IO158IO169IO1710IO1811IO1913IO2014IO812GND40IO139IO238TXD037RXD036IO4235IO4134IO4033IO3932IO3831NC30NC29NC28IO027IO4616IO917IO1018IO1119IO1220IO1321IO1422IO2123IO4724IO4825IO315IO4526EPAD41R40R70C2TBDX132.768KHz(NC)12R2NCC5TBDR1TBDR50(NC)JP1UART11223344R30(NC)C122uFC80.1uFR60JP3USB OTG1122JP2JTAG11223344C6TBDC712pF(NC)10 模组尺寸

10 模组尺寸

图 10-1. 模组尺寸

说明：

有关卷带、载盘和产品标签的信息，请参阅 《ESP32-S3 模组包装信息》。

乐鑫信息科技

38
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

25.5±0.21.51.2716.5140 x 0.940 x 0.93.1±0.15Top ViewSide ViewBottom View18±0.217.640 x 0.4511.050.840 x 0.850.544140 x Ø0.55ESP32-S3-WROOM-2U Dimensions61Unit: mm13.971.272.0151.51.2716.5140 x 0.9Top ViewBottom View18±0.240 x 0.4540 x 0.850.544111.515.817.61Side View40 x 0.919.2±0.240 x Ø0.550.811.052.462.491.273.2±0.15Unit: mm13.972.01513.212.667.64Ø0.515.8Ø0.57.6412.6611 PCB 布局建议

11 PCB 布局建议

11.1 PCB 封装图形

本章节提供以下资源供您参考：

• 推荐 PCB 封装图，标有 PCB 设计所需的全部尺寸。详见图 11-1 推荐 PCB 封装图。

• 推荐 PCB 封装图的源文件，用于测量图 11-1 中未标注的尺寸。您可用 Autodesk Viewer 查看

ESP32-S3-WROOM-2 的封装图源文件。

• ESP32-S3-WROOM-2 的 3D 模型。请确保下载的 3D 模型为.STEP 格式（注意，部分浏览器可能会加.txt

后缀）。

图 11-1. 推荐 PCB 封装图

乐鑫信息科技

39
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

Antenna Area11526401825.540 x1.540 x0.91.541147.641.2760.5Unit: mmCopperVia for thermal pad7.490.50.52.0152.0151.2717.512.6616.5111 PCB 布局建议

11.2 PCB 设计中的模组位置摆放

如产品采用模组进行 on-board 设计，则需注意考虑模组在底板的布局，应尽可能地减小底板对模组 PCB 天线
性能的影响。

关于 PCB 设计中模组位置摆放的更多信息，请参考 《ESP32-S3 硬件设计指南》 > 章节 基于模组的版图设计
通用要点。

乐鑫信息科技

40
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

12 产品处理

12 产品处理

12.1 存储条件

密封在防潮袋 (MBB) 中的产品应储存在 < 40 °C/90%RH 的非冷凝大气环境中。

模组的潮湿敏感度等级 MSL 为 3 级。

真空袋拆封后，在 25±5 °C、60%RH 下，必须在 168 小时内使用完毕，否则就需要烘烤后才能二次上线。

12.2 静电放电 (ESD)

• 人体放电模式 (HBM)：±2000 V

• 充电器件模式 (CDM)：±500 V

12.3 回流焊温度曲线

建议模组只过一次回流焊。

图 12-1. 回流焊温度曲线

乐鑫信息科技

41
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

50100015020025020010050150250   21725180230升温区25 – 150 °C60 – 90 s1 – 3 °C/s预热区150 – 200 °C60 – 120 s焊接区＞ 217 °C60 – 90 s冷却区＜ 180 °C–5 ~ –1 °C/s温度 (°C)时间 (s)峰值温度：235 – 250 °C峰值时间：30 – 70 s焊接时间：＞ 30 s焊料：锡银铜合⾦⽆铅焊料 (SAC305)12 产品处理

12.4 超声波振动

请避免将乐鑫模组暴露于超声波焊接机或超声波清洗机等超声波设备的振动中。超声波设备的振动可能与模组
内部的晶振产生共振，导致晶振故障甚至失灵，进而致使模组无法工作或性能退化。

乐鑫信息科技

42
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

技术规格书版本号管理

技术规格书版本号管理

技术规格书版本 状态

水印

定义

v0.1 ~ v0.5（不
包括 v0.5）

草稿

Confidential

v0.5 ~ v1.0（不
包括 v1.0）

初步

发布

v1.0 及更高版本

正式

发布

—

Preliminary

阶段，产品规格可能会在量产前变更，并记录在

该技术规格书正在完善。对应产品处于设计阶段，

产品规格如有变更，恕不另行通知。

该技术规格书正在积极更新。对应产品处于验证

技术规格书的修订历史中。

该技术规格书已公开发布。对应产品已量产，产

品规格已最终确定，重大变更将通过

产品变更通知 (PCN) 进行通知。

任意版本

任意版本

—

—

不推荐用于新设计 (NRND)1 该技术规格书更新频率较低，对应产品不推荐用

于新设计。

停产 (EOL)2

该技术规格书不再维护，对应产品已停产。

1 技术规格书涵盖的所有产品型号均不推荐用于新设计时，封面才会添加水印。
2 技术规格书涵盖的所有产品型号均停产时，封面才会添加水印。

乐鑫信息科技

43
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

相关文档和资源

相关文档和资源

相关文档

• 《ESP32-S3 技术规格书》 – 提供 ESP32-S3 芯片的硬件技术规格。
• 《ESP32-S3 技术参考手册》 – 提供 ESP32-S3 芯片的存储器和外设的详细使用说明。
• 《ESP32-S3 硬件设计指南》 – 提供基于 ESP32-S3 芯片的产品设计规范。
• 《ESP32-S3 系列芯片勘误表》 – 描述 ESP32-S3 系列芯片的已知错误。
• 证书

https://espressif.com/zh-hans/support/documents/certificates

• ESP32-S3 产品/工艺变更通知 (PCN)

https://espressif.com/zh-hans/support/documents/pcns?keys=ESP32-S3

• ESP32-S3 公告 – 提供有关安全、bug、兼容性、器件可靠性的信息

https://espressif.com/zh-hans/support/documents/advisories?keys=ESP32-S3

• 文档更新和订阅通知

https://espressif.com/zh-hans/support/download/documents

开发者社区

• 《ESP32-S3 ESP-IDF 编程指南》 – ESP-IDF 开发框架的文档中心。
• ESP-IDF 及 GitHub 上的其它开发框架

https://github.com/espressif

• ESP32 论坛 – 工程师对工程师 (E2E) 的社区，您可以在这里提出问题、解决问题、分享知识、探索观点。

https://esp32.com/

• ESP-FAQ – 由乐鑫官方推出的针对常见问题的总结。

https://espressif.com/projects/esp-faq/zh_CN/latest/index.html
• The ESP Journal – 分享乐鑫工程师的最佳实践、技术文章和工作随笔。

https://blog.espressif.com/

• SDK 和演示、App、工具、AT 等下载资源

https://espressif.com/zh-hans/support/download/sdks-demos

产品

• ESP32-S3 系列芯片 – ESP32-S3 全系列芯片。

https://espressif.com/zh-hans/products/socs?id=ESP32-S3

• ESP32-S3 系列模组 – ESP32-S3 全系列模组。

https://espressif.com/zh-hans/products/modules?id=ESP32-S3

• ESP32-S3 系列开发板 – ESP32-S3 全系列开发板。

https://espressif.com/zh-hans/products/devkits?id=ESP32-S3

• ESP Product Selector（乐鑫产品选型工具）– 通过筛选性能参数、进行产品对比快速定位您所需要的产品。

https://products.espressif.com/#/product-selector?language=zh

联系我们

• 商务问题、技术支持、电路原理图 & PCB 设计审阅、购买样品（线上商店）、成为供应商、意见与建议

https://espressif.com/zh-hans/contact-us/sales-questions

乐鑫信息科技

44
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

修订历史

修订历史

日期

版本

发布说明

2026-03-02

v1.7

2025-07-25

v1.6

• 将“订购代码”更新为“物料编号”
• 更新章节 5.2 外设描述 中每个小节的 管脚分配部分
• 在 5.2.1.9 SD/MMC 主机控制器 小节增加一条说明
• 更新表格 6-6 低功耗模式下的功耗

• 新增章节 4.5 芯片上电和复位
• 新增章节 6.5 存储器规格
• 新增章节 技术规格书版本号管理
• 其他微小改动

2025-06-10

v1.5

的注释

• 在章节 2 功能框图 中新增关于芯片与封装内 flash/PSRAM 管脚对应关系

2024-12-03

v1.4

• 新增模组型号 ESP32-S3-WROOM-2-N32R16V
• 将 模 组 型 号 ESP32-S3-WROOM-2-N16R8V 和 ESP32-S3-WROOM-2-

N32R8V 状态更新为停产

2024-11-14

v1.3

2023-11-24

v1.2

• 在章节 1.2 型号对比 的注释中新增对芯片修订信息的说明
• 更新章节 1.3 应用
• 更新章节 Strapping 管脚为章节 4 启动配置项
• 新增章节 5.2 外设描述
• 拆分章节 电气特性为章节 6 电气特性 和章节 7 射频特性 ，并更新格式和

措辞

• 拆分章节 模组尺寸和 PCB 封装图形为章节 10 模组尺寸 和 11 PCB 布局建

议，并新增章节 11.2 PCB 设计中的模组位置摆放

• 在章节 11.1 PCB 封装图形 中新增 ESP32-S3-WROOM-2 的 3D 模型链接
• 更新图 12-1 回流焊温度曲线
• 其他格式和措辞的次要更新

• 在表 1-1 ESP32-S3-WROOM-2 系列型号对比 中添加前两条表注
• 更新章节 4.1 芯片启动模式控制
• 修正了表 7-1 Wi-Fi 射频规格 中的工作信道中心频率范围
• 更新章节 8 模组原理图 中的模组原理图
• 更新章节 10 模组尺寸 中的模组尺寸图
• 其他微小改动

见下页

乐鑫信息科技

45
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

修订历史

日期

版本

发布说明

接上页

2023-03-07

v1.1

2022-11-01

v1.0

• 更新章节 Strapping 管脚
• 更新章节 6.4 功耗特性
• 将蓝牙最大射频发射功率从 21 dBm 更新为 20 dBm
• 更新章节 9 外围设计原理图 中的描述
• 在章节 11.1 PCB 封装图形 中增加描述
• 更新章节 12.4
• 其他微小改动

• 添加模组认证和测试信息
• 更新表 1-1 及表 6-6 并添加注释
• 更新表 3-1 中的注释
• 更新表 7-8 中的射频功率控制范围
• 其他微小改动

2022-05-09

2021-12-31

2021-07-13

v0.7

v0.6

v0.1

更新管脚定义表格

全面更新，针对芯片版本 revision 1

预发布，针对芯片版本 revision 0

乐鑫信息科技

46
反馈文档意见

ESP32-S3-WROOM-2 技术规格书 v1.7

免责声明和版权公告

本文档中的信息，包括供参考的 URL 地址，如有变更，恕不另行通知。

本文档可能引用了第三方的信息，所有引用的信息均为“按现状”提供，乐鑫不对信息的准确性、真实性做任何保证。

乐鑫不对本文档的内容做任何保证，包括内容的适销性、是否适用于特定用途，也不提供任何其他乐鑫提案、规格书或样
品在他处提到的任何保证。

乐鑫不对本文档是否侵犯第三方权利做任何保证，也不对使用本文档内信息导致的任何侵犯知识产权的行为负责。本文档
在此未以禁止反言或其他方式授予任何知识产权许可，不管是明示许可还是暗示许可。

Wi-Fi 联盟成员标志归 Wi-Fi 联盟所有。蓝牙标志是 Bluetooth SIG 的注册商标。

文档中提到的所有商标名称、商标和注册商标均属其各自所有者的财产，特此声明。

版权归 © 2026 乐鑫信息科技（上海）股份有限公司。保留所有权利。

www.espressif.com

