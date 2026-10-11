# ESP32-S3-WROOM-2 关键规格与开发板设计信息

> 来源：`esp32-s3-wroom-2_datasheet_cn.pdf`，技术规格书 v1.7，2026-03-02。  
> 本文面向全功能开发板的原理图、PCB 和器件选型，页码均指该 PDF 页码。

## 1. 模组概览

| 项目 | 规格 |
|---|---|
| 主芯片 | ESP32-S3R8V 或 ESP32-S3R16V |
| CPU | Xtensa 32 位 LX7 双核，最高 240 MHz，支持单精度 FPU |
| 片上存储器 | 384 KB ROM、512 KB SRAM、16 KB RTC SRAM |
| Flash | 16 MB 或 32 MB Octal SPI；当前推荐型号为 32 MB |
| PSRAM | 8 MB 或 16 MB Octal SPI；当前推荐型号为 16 MB |
| 无线 | 2.4 GHz Wi-Fi 4（IEEE 802.11 b/g/n）+ Bluetooth LE 5 |
| 天线 | 板载 PCB 天线 |
| GPIO | 33 个，其中 4 个为 strapping 管脚 |
| 晶振 | 模组内置 40 MHz 晶振 |
| 模组管脚 | 41 个：40 个周边焊盘 + 1 个底部 EPAD |
| 模组尺寸 | 18.0 mm x 25.5 mm x 3.1 mm |
| 供电 | 3.0-3.6 V，典型 3.3 V |
| 工作环境温度 | -40 至 65 °C |

ESP32-S3 面向 AIoT，适合语音唤醒、语音识别、人脸检测、摄像头、智能控制面板、音频、USB 设备、工业控制及通用物联网应用。（第 2-3 页）

## 2. 型号选择

| 物料编号 | Flash | PSRAM | 状态 |
|---|---:|---:|---|
| ESP32-S3-WROOM-2-N32R16V | 32 MB Octal SPI | 16 MB Octal SPI | 推荐用于新设计 |
| ESP32-S3-WROOM-2-N16R8V | 16 MB Octal SPI | 8 MB Octal SPI | 停产 |
| ESP32-S3-WROOM-2-N32R8V | 32 MB Octal SPI | 8 MB Octal SPI | 停产 |

建议全功能开发板采用 **ESP32-S3-WROOM-2-N32R16V**，避免在新设计中使用已停产型号。若开启 PSRAM ECC，模组最大环境温度可提升至 85 °C，但 PSRAM 可用容量减少 1/16。（第 3 页）

注意：型号表脚注说明模组 SPI Flash 默认最大时钟频率为 120 MHz，且不支持自动暂停功能；第 28 页的存储器供应商通用规格表列出的 Flash/PSRAM 最低保证最大时钟频率为 80 MHz。实际配置应以模组、芯片版本和 ESP-IDF 支持为准。

## 3. 无线规格

### Wi-Fi

- IEEE 802.11 b/g/n，2.4 GHz；信道中心频率 2412-2484 MHz。
- 802.11n 最高数据速率 150 Mbps，支持 HT20/HT40、0.4 us 保护间隔及帧聚合。
- 典型发射功率：802.11b 1/11 Mbps 为 20.5 dBm；802.11g 54 Mbps 为 18.0 dBm；802.11n HT20 MCS7 为 17.5 dBm；HT40 MCS7 为 17.0 dBm。
- 典型接收灵敏度：802.11b 1 Mbps 为 -98.2 dBm；802.11g 54 Mbps 为 -76.2 dBm；802.11n HT20 MCS7 为 -74.2 dBm；HT40 MCS7 为 -71.2 dBm。（第 29-31 页）

### Bluetooth LE

- Bluetooth 5、Bluetooth Mesh。
- 支持 125 Kbps、500 Kbps、1 Mbps、2 Mbps。
- 支持广播扩展、多广播集和信道选择算法 #2。
- 信道中心频率 2402-2480 MHz，射频发射功率范围 -24 至 20 dBm。
- Wi-Fi 与 Bluetooth LE 共用板载天线。（第 2、31 页）

## 4. 电源与电气规格

### 电源设计依据

| 参数 | 最小值 | 典型值 | 最大值 |
|---|---:|---:|---:|
| 3V3 建议工作电压 | 3.0 V | 3.3 V | 3.6 V |
| 外部电源供电能力 | 0.5 A | - | - |
| 电源管脚绝对最大电压 | -0.3 V | - | 3.6 V |
| 工作环境温度 | -40 °C | - | 65 °C |
| 存储温度 | -40 °C | - | 105 °C |

规格书要求外部电源至少具备 500 mA 供电能力。Wi-Fi 最大发射峰值可达 355 mA，因此开发板的 3.3 V 稳压器应留出 USB 外设、传感器、显示屏及瞬态裕量；对于全功能板，工程上宜选择持续输出能力不低于 1 A、瞬态响应良好的电源方案，并在模组附近配置低 ESR 储能和去耦电容。后一句是基于规格的设计建议，并非规格书硬性最小值。（第 25-26 页）

### GPIO 直流特性（3.3 V、25 °C）

| 参数 | 规格 |
|---|---|
| 输入高电平 VIH | >= 0.75 x VDD |
| 输入低电平 VIL | <= 0.25 x VDD |
| 输出高电平 VOH | >= 0.8 x VDD（高阻负载测试） |
| 输出低电平 VOL | <= 0.1 x VDD（高阻负载测试） |
| 最大档位典型拉电流 | 40 mA（VOH >= 2.64 V） |
| 最大档位典型灌电流 | 28 mA（VOL = 0.495 V） |
| 内部弱上拉/下拉 | 典型 45 kOhm |

40 mA/28 mA 是特定测试条件下单管脚驱动能力，不应视为建议的长期工作电流，也不代表所有 GPIO 可同时输出该电流。（第 25 页）

### 典型功耗（3.3 V、25 °C）

| 模式 | 条件 | 电流 |
|---|---|---:|
| Wi-Fi TX | 802.11b，1 Mbps，20.5 dBm | 峰值 355 mA |
| Wi-Fi TX | 802.11g，54 Mbps，18 dBm | 峰值 297 mA |
| Wi-Fi TX | 802.11n HT20 MCS7，17.5 dBm | 峰值 286 mA |
| Wi-Fi RX | 802.11b/g/n HT20 | 峰值 95 mA |
| Wi-Fi RX | 802.11n HT40 | 峰值 97 mA |
| Light-sleep | VDD_SPI/Wi-Fi 掉电、GPIO 高阻 | 典型 240 uA，另加封装内 PSRAM 影响 |
| Deep-sleep | RTC 存储器上电、RTC 外设掉电 | 典型 7 uA |
| Deep-sleep | RTC 存储器与 RTC 外设上电 | 典型 8 uA |
| 关闭 | EN 拉低 | 典型 1 uA |

第 27 页说明：封装内有 PSRAM 时功耗可能略高；Light-sleep 还需叠加相应 PSRAM 功耗。

## 5. 完整引脚表

下表按模组顶视图编号整理。（第 9-11 页）

| 序号 | 名称 | 主要功能/注意事项 |
|---:|---|---|
| 1 | GND | 地 |
| 2 | 3V3 | 3.0-3.6 V 供电 |
| 3 | EN | 高电平使能，低电平关闭/复位；不可悬空 |
| 4 | IO4 | GPIO4、TOUCH4、ADC1_CH3 |
| 5 | IO5 | GPIO5、TOUCH5、ADC1_CH4 |
| 6 | IO6 | GPIO6、TOUCH6、ADC1_CH5 |
| 7 | IO7 | GPIO7、TOUCH7、ADC1_CH6 |
| 8 | IO15 | GPIO15、U0RTS、ADC2_CH4、XTAL_32K_P |
| 9 | IO16 | GPIO16、U0CTS、ADC2_CH5、XTAL_32K_N |
| 10 | IO17 | GPIO17、U1TXD、ADC2_CH6 |
| 11 | IO18 | GPIO18、U1RXD、ADC2_CH7、CLK_OUT3 |
| 12 | IO8 | GPIO8、TOUCH8、ADC1_CH7 |
| 13 | IO19 | GPIO19、ADC2_CH8、USB_D- |
| 14 | IO20 | GPIO20、ADC2_CH9、USB_D+ |
| 15 | IO3 | GPIO3、TOUCH3、ADC1_CH2；JTAG strapping |
| 16 | IO46 | GPIO46；启动/ROM 日志 strapping |
| 17 | IO9 | GPIO9、TOUCH9、ADC1_CH8、FSPIHD |
| 18 | IO10 | GPIO10、TOUCH10、ADC1_CH9、FSPICS0/FSPIIO4 |
| 19 | IO11 | GPIO11、TOUCH11、ADC2_CH0、FSPID/FSPIIO5 |
| 20 | IO12 | GPIO12、TOUCH12、ADC2_CH1、FSPICLK/FSPIIO6 |
| 21 | IO13 | GPIO13、TOUCH13、ADC2_CH2、FSPIQ/FSPIIO7 |
| 22 | IO14 | GPIO14、TOUCH14、ADC2_CH3、FSPIWP/FSPIDQS |
| 23 | IO21 | GPIO21 |
| 24 | IO47 | GPIO47、差分 SPI 时钟；**1.8 V 电源域** |
| 25 | IO48 | GPIO48、差分 SPI 时钟；**1.8 V 电源域** |
| 26 | IO45 | GPIO45；VDD_SPI strapping |
| 27 | IO0 | GPIO0；Boot strapping/下载键 |
| 28-30 | NC | 空管脚，不连接 |
| 31 | IO38 | GPIO38、FSPIWP |
| 32 | IO39 | GPIO39、MTCK、CLK_OUT3 |
| 33 | IO40 | GPIO40、MTDO、CLK_OUT2 |
| 34 | IO41 | GPIO41、MTDI、CLK_OUT1 |
| 35 | IO42 | GPIO42、MTMS |
| 36 | RXD0 | GPIO44、U0RXD、CLK_OUT2 |
| 37 | TXD0 | GPIO43、U0TXD、CLK_OUT1 |
| 38 | IO2 | GPIO2、TOUCH2、ADC1_CH1 |
| 39 | IO1 | GPIO1、TOUCH1、ADC1_CH0 |
| 40 | GND | 地 |
| 41 | EPAD | 底部接地焊盘；建议接地以改善散热 |

> **关键警告：GPIO47 和 GPIO48 的工作电压为 1.8 V。** 不可直接连接 3.3 V 推挽信号或按普通 3.3 V GPIO 设计；如需连接 3.3 V 外设，应使用合适的电平转换。（第 11、37 页）

## 6. 启动、下载、复位与调试

### Strapping 管脚

| GPIO | 内部默认状态 | 主要作用 | 开发板设计注意事项 |
|---|---|---|---|
| GPIO0 | 弱上拉，默认 1 | 启动模式 | BOOT 键按下接地；避免外设在复位时强拉低 |
| GPIO3 | 浮空 | JTAG 信号源 | 若用于 strapping，必须由非高阻外部电路确定电平 |
| GPIO45 | 弱下拉，默认 0 | VDD_SPI 电压 | 模组 VDD_SPI 已由 eFuse 固定为 1.8 V；避免复位期冲突 |
| GPIO46 | 弱下拉，默认 0 | 启动模式、ROM 日志 | GPIO46 需为 0 才能与 GPIO0=0 进入 Joint Download Boot |

- 正常 SPI Boot：GPIO0 = 1，GPIO46 任意。
- Joint Download Boot：GPIO0 = 0 且 GPIO46 = 0，可通过 USB Serial/JTAG、USB OTG 或 UART0 下载。
- Strapping 电平在复位时锁存；EN 拉高后至少 3 ms 内需保持有效。（第 12-14 页）

### EN 与复位

- EN 高电平使能，低电平关闭/复位，禁止悬空。
- 电源稳定至 EN 拉高的最短时间为 50 us。
- EN 低电平复位脉宽至少为 50 us。
- 官方外围电路建议 EN 使用约 **10 kOhm + 1 uF** RC 延时，具体值仍需结合电源上升时序调整。
- 建议设置 RESET 键，使 EN 按下接地。（第 15、37 页）

### 推荐下载与调试接口

- **原生 USB**：GPIO19 = USB_D-，GPIO20 = USB_D+；可用于 USB 2.0 OTG 全速及 USB Serial/JTAG 下载调试。
- **UART0**：TXD0/GPIO43、RXD0/GPIO44；可接 USB-UART 桥用于下载和日志。
- **外部 JTAG**：GPIO39/40/41/42 分别对应 MTCK/MTDO/MTDI/MTMS。
- ROM 日志默认同时输出到 UART0 和 USB Serial/JTAG。（第 14、20-21、37 页）

## 7. 可用外设资源

芯片包含以下主要外设，但具体信号需通过 GPIO Matrix 映射，且并非芯片所有信号均在模组上引出：（第 16-24 页）

- 3 x UART，最高 5 Mbps，支持 RS232/RS485/IrDA。
- 2 x I2C，支持主/从模式和标准/快速模式，SCL/SDA 可映射到任意 GPIO。
- 2 x I2S，支持标准、PDM 和 TDM。
- LCD 接口：8-16 位并行 RGB、8080/6800；Camera 接口：8-16 位 DVP。
- 通用 SPI、全速 USB 2.0 OTG、USB Serial/JTAG。
- SD/MMC 主机、LED PWM、MCPWM、RMT、PCNT。
- TWAI 控制器，兼容 ISO 11898-1（CAN 2.0），需外接 CAN 收发器。
- 2 x 12 位 SAR ADC，共 20 个通道；ADC1 为 GPIO1-10，ADC2 为 GPIO11-20。
- 14 路电容触摸传感器（GPIO1-14）。
- 片上温度传感器、定时器、看门狗和 GDMA。

## 8. PCB、天线与焊接要求

### 模组摆放与天线

- 板载 PCB 天线应尽量放在底板边缘，天线区域及其前方保持净空。
- 天线净空区内避免铺铜、走线、器件和金属结构；最终尺寸按第 39 页推荐封装图及《ESP32-S3 硬件设计指南》执行。
- 模组封装宽 18 mm，推荐底板封装长度约 25.5 mm；天线区域位于模组一端。
- 不要仅凭 PDF 中低分辨率示意图手工重画封装；量产 PCB 应优先采用乐鑫提供的官方封装源文件和 STEP 模型，并按第 38-39 页复核关键尺寸。

### 接地与 EPAD

- 1、40 和 41（EPAD）均为 GND。
- EPAD 可以不焊，但焊接到底板 GND 可改善散热。
- 焊接 EPAD 时控制钢网开口和焊膏量，避免模组被过量焊膏顶高而导致周边焊盘贴合不良。（第 37 页）

### 制造与储存

| 项目 | 要求 |
|---|---|
| 湿敏等级 | MSL 3 |
| 密封储存 | < 40 °C、< 90% RH、无凝露 |
| 开封后车间寿命 | 25 +/- 5 °C、60% RH 下 168 小时 |
| 回流次数 | 建议仅 1 次 |
| 回流峰值 | 235-250 °C，峰值时间 30-70 s |
| 焊料 | SAC305 无铅焊料 |
| ESD HBM | +/- 2000 V |
| ESD CDM | +/- 500 V |

避免使用超声波焊接或超声波清洗设备处理模组，以免与内部晶振共振并造成故障。（第 41-42 页）

## 9. 全功能开发板建议接口清单

以下是基于上述规格整理的开发板实现建议：

1. 3.3 V 高动态响应电源，持续能力建议 >= 1 A；模组近端布置储能与去耦。
2. USB-C 接口连接 GPIO19/20，加入适合 USB 2.0 FS 的 ESD 保护，并按 USB 规范处理 CC 电阻。
3. 独立 USB-UART 桥连接 UART0，支持自动下载电路或保留手动 BOOT/RESET。
4. BOOT 键接 GPIO0 至 GND，RESET 键接 EN 至 GND；保证 GPIO46 复位时不被拉高。
5. 引出 4 线 JTAG（GPIO39-42）及 3V3/GND。
6. 将 ADC1、ADC2、触摸、I2C、I2S、SPI、UART、PWM 等功能分组引出；复用冲突应在丝印和文档中注明。
7. GPIO47/48 若引出，明确标注 **1.8 V ONLY**，最好通过电平转换或保护电阻隔离。
8. 预留 32.768 kHz 晶振位置可使用 GPIO15/16，但会占用对应 GPIO/ADC2/UART0 流控功能。
9. TWAI 接口应外接 CAN 收发器；RS485 也需外接相应收发器。
10. 模组天线置于板边并严格保留净空；EPAD 接大面积地和散热过孔阵列。

## 10. 设计复核清单

- [ ] 使用 N32R16V，未选用已停产 N16R8V/N32R8V。
- [ ] 3V3 始终位于 3.0-3.6 V，电源能力和瞬态裕量充足。
- [ ] EN 不悬空，并有符合时序的 RC 与复位键。
- [ ] GPIO0/3/45/46 外接电路不会破坏启动 strapping。
- [ ] GPIO47/48 的所有外部连接均兼容 1.8 V。
- [ ] USB D-/D+ 分别连接 GPIO19/GPIO20，走线按差分对处理。
- [ ] BOOT、RESET、UART0、USB Serial/JTAG 至少保留一种可靠下载路径。
- [ ] 天线位于板边，净空区无铜、走线、器件和金属遮挡。
- [ ] 模组 GND 与 EPAD 接地良好，EPAD 焊膏量受控。
- [ ] NC 28-30 保持不连接。
- [ ] 原理图/PCB 封装与官方推荐封装、尺寸图和最新版硬件设计指南交叉复核。
- [ ] 量产前检查最新版规格书、勘误表、PCN、认证和射频法规要求。

## 11. 文档边界

本文仅汇总模组规格书中的关键内容。GPIO Matrix 的完整信号分配、ADC 限制、电源完整性、USB/射频布线、芯片版本勘误等细节，还应结合以下乐鑫官方资料完成设计：

- 《ESP32-S3 系列芯片技术规格书》
- 《ESP32-S3 技术参考手册》
- 《ESP32-S3 硬件设计指南》
- 《ESP32-S3 系列芯片勘误表》

