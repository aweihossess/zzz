## 功能描述

面向车辆动力域、ADAS域以及V2X域的应用功能开发者，提供了一套应用的快速开发与功能验证的开发套件。

## 目录结构

本文所提供USP 开发套件（ToolKit）内的文件夹结构为：

| 文件夹   | 描述与子文件夹内容                         | 系统依赖 |
| :------- | ----------------------------------------- | -------- |
| 📁 examples        | 前车碰撞检测（FCW）样例文件 <br />&emsp;📝scenes.zip - FCW使用的场景文件<br />&emsp;📝uapp.slx - FCW的simulink模型 <br />&emsp;📝uaes.tar.gz - FCW应用编译产物 | Windows |
| 📁 `gens`   | 基于前车碰撞检测（FCW）模型生成的代码，用户替换为自己模型的生成代码。 | Windows |
| 📁 `inc` | 编译依赖头文件 |  Linux  |
| 📁 `libs` | 编译依赖库文件 |  Linux  |
| 📁 `simulink_kits` | 应用开发所需Simulink依赖文件，须导入simulink使用：<br />📁 uapp - 应用开发的simulink模型模板相关<br />📁 ucore - USP服务lib库的simulink实现<br /> | Windows  |
| 📁 `src` | 应用框架代码 | Linux    |
| 📁 `tools` | 存放应用开发的工具集：<br />📁 scripts - 工程更新脚本，用户无需关心<br />📁ai_kits - AI相关的工具集，包含：<br />&emsp;📁onnx2c - onnx模型优化及c代码转换<br />&emsp;📁auto_DLML - 参数寻优工具 | Linux    |
| 📝 `build.sh` | 编译脚本，编译并打包./build/uaes.tar.gz，用于上传USPSim | Linux    |
| 📝 `version.json` | 当前toolkit的版本描述文件 |  |

## 修订版本

Version 1.0.0（2023年1月）

- demo 初版
- template 初版
- ucores 初版

Version 1.0.3（2023年8月）

- 调整目录结构

Version 1.0.2.2

- 2023.6.20更新，新增：1. 电机转速与转矩原子服务的实现；

Version 1.0.3.0

- 2023.7.26更新，新增：更好的兼容UBox软件与不同Matlab版本；

Version 1.0.4.0

- 2023.11.16更新，修复: 1.电机控制接口无法正常发送扭矩信息；

Version 1.0.4.1

- 2023.11.7更新，修复: 1.电机控制接口数据类型变更为有符号；

