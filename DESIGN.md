---
name: 宿舍增肌减脂计划
description: 学生的三大营养素与体重记录工具 —— 克制的纸面、唯一翡翠、1px 描边
colors:
  emerald: "#0f9d6e"
  emerald-night: "#2fbd86"
  emerald-fill: "#0b7a55"
  emerald-fill-night: "#2fbd86"
  emerald-text: "#0b7a55"
  emerald-text-night: "#4fd39f"
  on-emerald: "#ffffff"
  page: "#f7f7f5"
  page-night: "#0e0f0e"
  surface: "#ffffff"
  surface-night: "#171817"
  ink: "#1a1a1a"
  graphite: "#6b6b6b"
  hairline: "#e6e6e2"
  emerald-wash: "#e6f5ee"
  signal-error: "#c0392b"
  signal-error-night: "#e5736a"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "clamp(34px, 5.4vw, 58px)"
    fontWeight: 800
    lineHeight: 1.12
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "clamp(24px, 3.4vw, 34px)"
    fontWeight: 800
    lineHeight: 1.2
    letterSpacing: "-0.015em"
  stat:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "44px"
    fontWeight: 800
    lineHeight: 1
    letterSpacing: "-0.02em"
    fontFeature: "tnum"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "15px"
    fontWeight: 700
    lineHeight: 1.5
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, \"PingFang SC\", \"Microsoft YaHei\", \"Segoe UI\", sans-serif"
    fontSize: "12px"
    fontWeight: 700
    lineHeight: 1.5
    letterSpacing: "0.2em"
rounded:
  card: "16px"
  control: "12px"
  field: "10px"
  micro: "8px"
  capsule: "999px"
spacing:
  xs: "6px"
  sm: "12px"
  md: "20px"
  lg: "40px"
  xl: "72px"
components:
  button-primary:
    backgroundColor: "{colors.emerald-fill}"
    textColor: "{colors.on-emerald}"
    rounded: "{rounded.control}"
    padding: "13px 22px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "13px 22px"
  button-small:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "8px 14px"
  card-target:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "24px 26px"
  card-food:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "16px"
  panel:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "20px"
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.field}"
    padding: "9px 12px"
  chip-macro:
    backgroundColor: "{colors.page}"
    textColor: "{colors.graphite}"
    rounded: "{rounded.micro}"
    padding: "6px 4px"
  progress-track:
    backgroundColor: "{colors.page}"
    rounded: "{rounded.capsule}"
    height: "9px"
---

# Design System: 宿舍增肌减脂计划

## Overview

**Creative North Star: "清晨备餐台 The Morning Counter"**

这是一张每天清晨会被摊开的备餐台：干净的浅色纸面、一支笔、一台厨房秤。设计不表演，它只把当天要吃的三样东西（蛋白质、碳水、脂肪）清楚地摆出来，让你对一眼、记一笔、走人。整个系统的戏剧性只来自一处——那一点翡翠绿，像秤上跳动的合格读数，只出现在目标、进度和主按钮上。

**气质是"克制而精确"**：大量留白、低饱和中性色、数字干净。信息密度按日常工具来（中等偏低），不塞第二强调色、不摆装饰插画、不加投影。层级全部交给**留白 + 1px 描边 + 字重对比**三种手段，而不是颜色和阴影。

世界是**浅色优先**的，并跟随 `prefers-color-scheme` 提供暗色版本：浅色是晨光纸面（`#f7f7f5` / 纯白卡片），暗色是熄灯后的备餐台（`#0e0f0e` / `#171817`）。两个模式共享同一套结构与同一颗翡翠绿——白天用 `#0f9d6e`，夜里提亮为 `#2fbd86`。

**Key Characteristics:**
- 单一翡翠强调色，覆盖率极低，只服务目标/进度/主操作
- 描边即分层：1px 半透明柔线取代一切投影，整体近乎扁平
- 系统中文黑体栈，字重（800/700/400）承担全部层级，无 webfont
- 四档圆角 + 胶囊进度条，形状语言高度收敛
- 所有数量用等宽数字（tabular numerals），读数对齐不跳动

## Colors

一套"中性纸面 + 唯一翡翠"的低饱和系统：中性色负责结构与文字，翡翠负责"达标"这一件事。

### Primary
- **克制的翡翠 Restrained Emerald**：唯一强调色。它是"合格/达标"的视觉同义词——出现在哪，哪就是你当前该看的地方。同色相按对比度需要分三档取值：
  - **装饰翡翠 Emerald** (#0f9d6e；夜 #2fbd86)：非文字用途——进度条填充、食物卡 hover 描边、`accent-color`。它不与文字同框，无需过 AA。
  - **翡翠·填充 Emerald Fill** (#0b7a55；夜 #2fbd86)：白字所坐的实底——主按钮、"＋100g" hover 底、焦点外框。浅色下比装饰档压深一档，让白字达 AA。
  - **翡翠·文字 Emerald Text** (#0b7a55；夜 #4fd39f)：翡翠色的文字与标签——品牌点、Hero eyebrow、超额读数、"＋100g" 文字。夜里提亮到 #4fd39f，以在暗纸面上达标。

### Neutral
- **晨光纸 Page** (#f7f7f5)：页面底色（暗色模式 #0e0f0e）。比纯白低一档，让白色卡片能浮起来。
- **台面 Surface** (#ffffff；暗色模式 #171817)：卡片、面板、输入框的唯一浮起色。它是全系统唯一的纯白值，仅作面板使用，不做大面积背景铺陈。
- **墨 Ink** (#1a1a1a)：主文字、标题、数字。
- **石墨 Graphite** (#6b6b6b)：说明文字、标签、次级信息。
- **柔线 Hairline** (#e6e6e2)：1px 描边与分隔线，全系统深度的唯一来源。
- **翡翠洗 Emerald Wash** (#e6f5ee)：翡翠的极浅底，仅用于图片占位与暗色模式装饰面。
- **告警红 Signal Error** (#c0392b；夜 #e5736a)：表单校验失败的唯一点缀，除此之外不得出现第二个强调色。

### Named Rules
**翡翠三档律。** 翡翠只允许三种安全取值——装饰（#0f9d6e / #2fbd86）、填充（#0b7a55 / #2fbd86）、文字（#0b7a55 / #4fd39f）。文字用文字档，白字底用填充档，其余用装饰档；不得把装饰档直接当文字色或白字按钮底。
**翡翠稀有律。** 翡翠在任意一屏的覆盖不超过约 8%。它是秤上的合格读数，不是背景板——翡翠一多，"达标"的信号就失效。
**一色律。** 除翡翠外不引入任何彩色强调。告警红只用于错误文本，不得扩展成语义色板。
**墨不纯黑律。** 文字墨为 #1a1a1a，禁止 #000；纸面为 #f7f7f5，禁止大面积纯白铺底。

## Typography

**Display Font:** 系统中文黑体栈（PingFang SC → Microsoft YaHei → Segoe UI）
**Body Font:** 同上
**Label/Mono Font:** 无独立字体；标签复用人黑体，数字靠 `tabular-nums` 对齐

**Character:** 只有一套字。中文 webfont 动辄数 MB，系统栈是这个工具最诚实的选择。层级不靠换字体，只靠字重与字号——800 的标题与 400 的正文之间，隔着清晰的秩序感。

### Hierarchy
- **Display** (800, clamp(34px–58px), 1.12, -0.02em): 仅 Hero 主标题。
- **Headline** (800, clamp(24px–34px), 1.2): 各区块大标题。
- **Stat** (800, 44px, 1.0, `tabular-nums`): 三大目标大数字专用步长，只用于数据。
- **Title** (700, 15–22px): 卡片标题、食材名、合计金额。
- **Body** (400, 15–17px, 1.6): 正文与说明，说明文字用石墨色。
- **Label** (700, 11–13px, 0.2em 字距, 全大写): 仅 Hero 的英文小标（唯一一处 eyebrow）。

### Named Rules
**数字等宽律。** 凡克数、重量、金额、目标值一律 `font-variant-numeric: tabular-nums`。读数是这个世界的主角，绝不允许因数字变宽而抖动。
**系统字栈律。** 不引入任何 webfont。新页面沿用系统中文黑体栈，缺失字重由 CSS 回落承担。

## Layout

单列叙事流，容器最大 **1100px** 居中，左右内距 `clamp(16px, 4vw, 48px)`；区块垂直节奏 `clamp(40px, 6vw, 72px)`。钉在顶部的只有一个 **60px 导航条**（品牌在左，锚点在右）。

关键栅格与断点（既有实现，移动端一律塌成单列）：
- **Hero**：桌面 `1.15fr / 0.85fr` 双列（文案 / 备餐图），`≥860px` 以下塌为单列并取消满屏高度。
- **每日目标**：三列 `repeat(3, 1fr)`，`≤700px` 塌为单列。
- **今日搭配**：桌面 `1fr / 360px`（已选食材 / 总量对照），`≤900px` 塌为单列。
- **导航锚点**：`≤760px` 隐藏，保留品牌。
- **采购明细行**：`≤600px` 由四列压成两列。

桌面端优先使用 CSS Grid 而非 flex 百分比运算；全站可点击件（按钮、食物卡）在 `:active` 下沉 `scale(0.98)` 作为触感回执。

## Elevation & Depth

**扁平系统，零投影。** 深度完全由三种手段叠加：`#f7f7f5` 纸面 → `#ffffff` 台面的一档色阶、1px 柔线描边、以及字重对比。整个 CSS 里没有一条 `box-shadow`。

### Named Rules
**描边即分层律。** 需要区分层级时，用 1px `hairline` 描边或一道色阶，不得添加投影、模糊、玻璃拟态或渐变洗光。悬浮是纸的堆叠，不是物体的浮起。

## Shapes

形状语言收敛到四档圆角，**全站没有第二个体系**：
- 卡片 **16px**（目标卡、食物卡、弹窗）
- 控制件 **12px**（按钮、面板、窄屏行）
- 输入件 **10px**（日期、数字、文本、下拉）
- 微件 **8px**（宏观营养小格、步进按钮）

外加唯一例外：**进度条胶囊 999px**（`.bar` 的轨道与填充）——它是量尺的零件，不是召唤物，因此允许胶囊。

描边一律 1px `hairline`；聚焦态升级为 `2px` 实色翡翠 outline（`offset: 1–2px`）。

### Named Rules
**四档圆角律。** 除上面四档与进度条胶囊外，不得出现任何其它圆角值。混入胶囊按钮或直角卡片即为破形。

## Components

### Buttons
- **Shape:** 12px 圆角矩形（非胶囊），黑体 700，`transition: transform .12s`。
- **Primary:** 翡翠底 + 白字（`padding: 13px 22px`）；`:active` 下沉 `scale(0.98)`。
- **Ghost:** 透明底 + 1px 柔线边框 + 墨色字；hover 边框转石墨；同日用于"记录体重""添加一项"等次操作。
- **Small:** `padding: 8px 14px`，用于"修改资料"等行内次级动作。

### Cards / Containers
- **Corner Style:** 16px（卡片）/ 12px（面板）。
- **Background:** `#ffffff` 台面；无渐变、无洗光。
- **Border:** 1px `hairline`；食物卡 hover 时描边转翡翠并上浮 `translateY(-2px)`。
- **Internal Padding:** 卡片 16px、目标卡 24–26px、面板 20px。

### Chips（宏观营养小格）
- **Style:** `#f7f7f5` 底 + 1px 柔线 + 8px 圆角，三列等分；标签石墨色 12px，数值墨色 14px 加粗。
- **Usage:** 只在食物卡内表达"蛋白/碳水/脂肪"三读数。

### Inputs / Fields
- **Style:** 台面底 + 1px 柔线 + 10px 圆角，`padding: 9px 12px`。
- **Focus:** `2px` 翡翠 outline，`offset: 1px`，边框转翡翠。
- **Error:** 错误文案用告警红，紧贴字段下方。

### Navigation
- **Style:** 60px 高，`backdrop-filter: blur(10px)`，底色为 82% 不透明的纸色，底部 1px 柔线。品牌 17px/800，锚点 14px 石墨色，hover 转墨色；`≤760px` 锚点隐藏。

### Progress Bar（签名组件）
- **Character:** 全站唯一的胶囊形态，9px 高，用于"当日总量 vs 目标"。
- **Style:** 轨道 `#f7f7f5` + 1px 柔线，填充纯翡翠；填充量按摄入/目标比例，用 `transform: scaleX()`（`transform-origin: left`）表达，封顶 1。
- **Behavior:** 达标或超额时，数值行追加翡翠色"(已超额 Ng)"字样——这是全站最重要的达标反馈。填充动画 `transition: transform .25s`。

### Profile Modal（资料弹窗）
- **Character:** 首次进入与"修改资料"共用的浮层，负责采集性别/身高/体重并推算三大目标。
- **Style:** 半透明遮罩 `rgba(0,0,0,.55)` + 台面弹窗（16px 圆角，clamp 内距），字段纵向排列，动作区放单颗翡翠主按钮。

## Do's and Don'ts

### Do:
- **Do** 所有克数、体重、金额、目标值统一 `tabular-nums`（数字等宽律）。
- **Do** 用 1px `hairline` 描边和 `#f7f7f5 → #ffffff` 色阶制造层级（描边即分层律）。
- **Do** 把翡翠限制在目标数字、进度填充、主按钮、焦点外框上，覆盖率 ≤ 8%（翡翠稀有律）。
- **Do** 沿用系统中文黑体栈与四档圆角（16/12/10/8 + 进度条胶囊）。
- **Do** 每个动效都过 `prefers-reduced-motion` 闸门；本系统已有全局降级块。
- **Do** 暗色模式只切换 `:root` 变量值，结构与强调色保持一致（同一颗翡翠，夜里提亮）。

### Don't:
- **Don't** 引入第二个强调色；告警红只用于错误文本（一色律）。
- **Don't** 使用任何 `box-shadow`、模糊、玻璃拟态或渐变洗光（描边即分层律）。
- **Don't** 引入 webfont 或第三方图标库；现有界面用 "＋ / − / ×" 文本符号，保持无图标依赖。
- **Don't** 使用四档以外的圆角，或把按钮做成胶囊（唯一例外是进度条）。
- **Don't** 用纯黑 #000 或大面积纯白铺底（墨不纯黑律）。
- **Don't** 动画 `width`/`height`/`padding`/`margin`；新动效一律用 `transform` 与 `opacity`。
