# OLED-UI-ASTRA-LITE 移植示例

这是 [OLED-UI-ASTRA-LITE](https://github.com/Varvarlen/oled-ui-astra-lite) 库移植到 STM32F411 平台的示例项目。

## 项目结构

- **Doc/** - 移植文档和使用指南
- **UI/** - UI 核心文件
  - **Core/** - 渲染引擎
  - **Components/** - UI 组件（按钮、菜单等）
  - **Fonts/** - 字体资源
  - **HAL/** - 硬件抽象层
  - **Config/** - 配置文件
- **Drivers/** - OLED 驱动程序
- **Examples/** - 示例应用

## 硬件要求

- STM32F411 开发板
- SSD1306/SH1106 OLED 显示屏（I2C 或 SPI 接口）

## 快速开始

1. 根据 `Doc/OLED_UI_Astra_Lite_移植指南.md` 进行硬件连接
2. 在 `UI/Config/ui_config.h` 中配置你的显示屏参数
3. 编译并烧录 `Examples/oled_demo.c` 示例程序

## 硬件连接

### I2C 接口

| STM32F411 | OLED 显示屏 |
|-----------|-------------|
| PB8       | SCL         |
| PB9       | SDA         |
| 3.3V      | VCC         |
| GND       | GND         |
| PA10      | RST (可选)  |

### SPI 接口

| STM32F411 | OLED 显示屏 |
|-----------|-------------|
| PA5       | SCK         |
| PA7       | MOSI/SDA    |
| PA8       | DC          |
| PA9       | CS          |
| PA10      | RST         |
| 3.3V      | VCC         |
| GND       | GND         |

## 配置选项

在 `UI/Config/ui_config.h` 中可以修改以下配置：

- 显示分辨率
- 接口类型 (I2C/SPI)
- OLED 控制器型号 (SSD1306/SH1106)
- 字体选择
- 缓冲区策略

## 更多信息

详细的移植文档请参考 `Doc/OLED_UI_Astra_Lite_移植指南.md`。

## 许可证

此移植示例项目基于原始库的许可证条款，详情请参考原始库仓库：
[https://github.com/Varvarlen/oled-ui-astra-lite](https://github.com/Varvarlen/oled-ui-astra-lite)
# oled-ui-astra-lite
