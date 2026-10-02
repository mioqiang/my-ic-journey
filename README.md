# my-ic-journey

电化学 → 数字 IC 后端 / 嵌入式的学习与项目记录（W1–W45）。

> 本仓库从 2026 W1 起持续提交，每周一份周志 + 一份交付物。

---

## 仓库结构

```text
my-ic-journey/
├── README.md              # 本文件（W17 里程碑前补全为可复现文档）
├── weekly-log/            # 每周复盘 + 自检表
│   ├── W01.md
│   └── ...
├── c/                     # C 语言练习（ring buffer / 状态机 / 链表 / 位操作）
├── tcl/                   # Tcl 脚本（时序报告处理、自动化）
├── verilog/               # Verilog RTL + testbench
├── backend/               # W11 起的后端项目
│   ├── reports/           # 综合/STA/DRC 报告
│   ├── scripts/           # SDC、Tcl 流程脚本
│   └── images/            # 版图截图、波形截图
└── docs/                  # 速查卡、简历素材、面试复盘
```

---

## 当前进度

| 周 | 主题 | 交付物 | 状态 |
|---|---|---|---|
| W01 | Linux 起步 + C 起步 | 5 个 C 小程序 + 本仓库首次提交 | 🚧 进行中 |
| W02 | Linux 文本处理 + C 控制流 | 电化学数据统计程序 | ⬜ 未开始 |

**平台进度**：HDLBits ___ 题 ｜ Bandit ___ 关 ｜ 后端流程 ___ 次跑通

---

## 项目：RTL-to-GDS（W17 · M3）

> 做到哪周填哪周，不要等 W17 才补。

### 一条复现命令

```bash
# TODO: 填入真正能跑通的命令，例如
# make DESIGN_CONFIG=./backend/scripts/config.mk
```

### 效果

| 项目 | 值 |
|---|---|
| 设计 | _（如 UART 发送机 / SPI 主控）_ |
| 工艺 | SkyWater Sky130 |
| 流程 | ORFS (OpenROAD-flow-scripts) |

### PPA 表格

| 指标 | 优化前 | 优化后 | 变化 |
|---|---|---|---|
| 频率 (MHz) | | | |
| 面积 (µm²) | | | |
| 功耗 (mW) | | | |
| WNS (ns) | | | |
| Cell 数 | | | |

### 架构图

<!-- TODO: 贴框图 -->

### 流程图

```text
综合 → floorplan → placement → CTS → routing → STA → DRC/LVS → GDS
```

### 版图截图

<!-- TODO: KLayout 打开的 GDS 截图 -->

---

## 硬件项目：恒电位仪（W19–W21）

| 项目 | 内容 |
|---|---|
| 电路 | TIA 恒电位仪（LTspice 仿真先行） |
| PCB | 2 层，嘉立创 EDA，保护环 + 模拟/数字分区 |
| 状态 | ⬜ 未开始 |
| 验证 | CV 阶梯波 + 安培 i-t |

---

## 联系

- GitHub: [@mioqiang]
- 方向：数字 IC 后端 / 嵌入式 / 半导体工艺
