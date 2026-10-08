# my-ic-journey

> **电化学 → 数字 IC 后端 / 嵌入式的转行学习规划**
> 集成电路科学与工程硕士在读 · 起点 2026.09.22 · 目标 2027.02（研一下）投递短期实习

本仓库记录我的转行学习路线：能力清单、阶段规划、学习平台与自我验收标准。

**当前处于规划阶段** —— 各项交付物（代码、脚本、时序报告、版图）将随进度逐步加入本仓库。

---

## 一、背景与定位

| 项 | 内容 |
|---|---|
| 专业 | 集成电路科学与工程（硕士在读） |
| 研究课题 | MOF 电化学传感（葡萄糖、多巴胺等电化学检测） |
| 起点 | 2026.09.22 |
| 目标 | 2027.02 起投递数字 IC 后端 / 嵌入式短期实习 |

**方向组合：**

| 优先级 | 方向 | 说明 |
|---|---|---|
| 主线 A | **数字 IC 后端** | 专业名直接对口。日常工作本质是「跑工具 → 看报告 → 修 violation → 写脚本自动化」，看重流程熟练度与脚本能力 |
| 主线 B | **嵌入式** | C / STM32 / RTOS / 硬件项目，与主线 A 共享 Linux 地基 |
| 延伸 | **半导体工艺** | 电化学背景直接对应 ECP 电镀、CMP、湿法工艺、电化学量测 |

> 电化学背景不是无关经历 —— 它对应半导体制造中的湿法工艺与电化学量测环节。

---

## 二、能力清单

### 主线 A · 数字 IC 后端

**核心能力：**

- Linux 命令行：文件 / 权限 / 进程 / `grep` / `sed` / `awk` / 管道 / 重定向 / `vim` / `ssh` / `rsync`
- Tcl 脚本：变量、列表、控制流、`proc`、字符串、正则、文件读写（ICC2 / Innovus 的脚本语言）
- 数字电路基础：组合 / 时序逻辑、触发器、状态机、时钟
- Verilog：读懂、编写模块、编写 testbench
- STA 时序：setup / hold、arrival / required、slack、时钟偏斜、SDC 约束
- 后端全流程概念：综合 → floorplan → placement → CTS → routing → 时序优化 → DRC/LVS → 签核
- 一个跑通的 RTL-to-GDS 项目（OpenROAD + Sky130 PDK）

**进阶目标：**

- 第二个更复杂的设计（UART / SPI 控制器、小型 RISC-V 核）
- 工具链：OpenSTA / Yosys / Magic / Netgen
- PPA 权衡、工艺角、多阈值电压、拥塞、IR drop、时钟树结构

### 主线 B · 嵌入式

- C 语言：指针、结构体、位操作、**环形缓冲区 / 状态机 / 链表**
- STM32：时钟树、中断 / NVIC、定时器、PWM、ADC + DMA、SPI / I2C / UART、低功耗模式
- FreeRTOS：任务、队列、信号量、互斥量、事件组
- 一个完整硬件项目：原理图 + PCB + 固件 + 上位机
- Linux：命令行、Makefile、交叉编译

---

## 三、阶段规划

| 阶段 | 周次 | 主题 | 终点交付物 |
|---|---|---|---|
| Phase 0 | W1–W4 | Linux + C 双地基 | Linux 熟练 + C 能写 ring buffer / 状态机 |
| Phase 1 | W5–W10 | Tcl + Verilog + 数字设计 + STM32 | Yosys 综合跑通 + Tcl 脚本 + STM32 外设 |
| Phase 2 | W11–W17 | STA + OpenROAD 后端全流程 | **RTL-to-GDS 全流程跑通 + PPA 报告** |
| Phase 3 | W18–W21 | 项目攻坚 + 硬件项目 + 简历 | 两个后端项目 + 嵌入式项目 |
| Phase 4 | W22+ | 投递与实习 | 一段真实实习经历 |

---

## 四、学习平台与工具

| 方向 | 平台 / 工具 |
|---|---|
| Linux | Ubuntu、OverTheWire Bandit、HackerRank Shell、MIT《Missing Semester》 |
| C | 翁恺《C 语言程序设计》、《C Primer Plus》、牛客 C 专项 |
| Tcl | Tcl 官方教程、Exercism Tcl track |
| Verilog | **HDLBits**（主练习场）、EDA Playground、iverilog + GTKWave |
| 数字后端 | **OpenROAD-flow-scripts**、OpenLane、Yosys、OpenSTA、SkyWater Sky130 PDK |
| 物理验证 | Magic（DRC）、Netgen（LVS）、KLayout（版图查看） |
| 嵌入式 | STM32（江科大 / 正点原子 / 野火）、FreeRTOS 官方文档 |
| 模拟 / PCB | LTspice、Falstad、嘉立创 EDA |
| 半导体 | 《半导体物理与器件》（Neamen）、《芯片制造》（Van Zant） |

> 说明：学校没有商业 EDA 工具（ICC2 / Innovus），因此使用**开源全流程**完成 RTL-to-GDS。
> 目标是把每一步真正跑通、理解它在做什么，而不是停留在概念层面。

---

## 五、自我验收标准

不用「我懂了」判断，只用三档：

| 档次 | 定义 | 判定方式 |
|---|---|---|
| **L1 自测合格** | 不给资料、不给答案，限时内独立完成 | 闭卷卷子 / 自写测试用例 / 一键复现 |
| **L2 表达合格** | 能对白板讲清「为什么这么做」并给出数字 | 录音讲 3 分钟，对方能复述 |
| **L3 市场合格** | 陌生人看了仓库或简历，愿意给面试 | 面试邀请 / 内推 |

**判定原则：每个阶段只有做出「交付物」才算通过。没有交付物 = 这一阶段白过。**

**关键里程碑：**

| 节点 | 验收内容 |
|---|---|
| W4 | 闭卷：Linux 管道 + bash + ring buffer + 状态机 + 链表 + 位操作 |
| W10 | Yosys 综合 + 解释综合报告 + 编写 SDC + FreeRTOS 三任务 + Tcl 脚本 |
| **W17** | **RTL-to-GDS 全流程跑通，产物可被他人按文档复现** |

---

## 六、计划产出的交付物

> 以下为按计划将陆续加入仓库的内容，**目前尚未产出**。

| 产物 | 内容 | 计划节点 |
|---|---|---|
| C 程序 | ring buffer、状态机、链表、位操作等 | W1–W4 |
| Tcl 脚本 | 时序报告解析、违例统计、自动化 | W5–W6 |
| Verilog RTL | UART / SPI / 计数器 + testbench | W7–W10 |
| 后端全流程 | OpenROAD RTL-to-GDS（Sky130），含 PPA 对比 | W11–W17 |
| 时序签核 | OpenSTA 的 WNS / TNS / 关键路径分析 | W14–W15 |
| 版图与验证 | GDSII、KLayout 截图、DRC / LVS clean | W14 |
| 硬件项目 | 恒电位仪（LTspice 仿真 → 2 层 PCB → 实测） | W18–W21 |

---

## 七、仓库结构

```text
my-ic-journey/
├── README.md     # 本文件：学习路线与验收标准
└── .gitignore
```

> 随着上方交付物逐项产出，会相应新增 `c/`、`tcl/`、`verilog/`、`backend/` 等目录。

---

## 八、联系

- GitHub：[@mioqiang](https://github.com/mioqiang)
- 方向：数字 IC 后端 / 嵌入式
